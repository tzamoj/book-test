# Proposals

Proposals are implemented through a collection of submodules under proposals: 1 library module containing the core interface and implementation, and 1 submodule per proposal kind.

## Stored Information

A proposal is submitted with at least the following information kept in a struct:

<details>

<summary>ProposalInfo (struct)</summary>

Basic information saved per submitted proposal.

* id (felt): An incremental identifier for the proposal.
* kind (felt): The proposal's kind as a short-string.&#x20;
* submittedBy (felt): Address of the submiter.
* submittedAt (felt): Number of the block which includes the proposal's submission.
* status (felt): The actual state of the proposal in its lifecycle.
* description (felt): A short string describing the proposal's content.

</details>

Additional information can be included that depends on the proposal's kind. In that case, it is handled by the kind's submodule directly, so that no further assumption is needed.

The DAO records the list of all proposals that were ever submitted onchain through the following 2 storage variables:

<details>

<summary>proposalsLength (storage_var)</summary>

The number of proposals ever submitted to the DAO.

_Returns_:

* length (felt)

</details>

<details>

<summary>proposals (storage_var)</summary>

The list of all proposals' info.

_Arguments_:

* id (felt): the positional index of the proposal, which is also its proposalId

_Returns_:

* proposal (ProposalInfo)

</details>

## Lifecycle

A proposal goes through a few phases in its lifecycle. A proposal's status records which phase it is in, one from the following enum:

<details>

<summary>Proposal (namespace):</summary>

* SUBMITTED = 'submitted' : in voting period
* ACCEPTED = 'accepted' : accepted and in grace period
* REJECTED = 'rejected' : rejected
* FORCED = 'forced' : sent directly to grace period

The following status are final, meaning the proposal has been closed:

* ABORTED = 'aborted' : did not go completely through voting
* EXECUTED = 'executed' : Execution is finalised and successful&#x20;
* FAILED = 'failed' : execution failed

</details>

## Parametrisation

Proposals can be parametrised on a per kind basis (e.g.: member onboarding, or swaps), as each kind can have different needs. The parameters govern all proposals' lifecycle of its kind. All parameters are kept in the following structure:

<details>

<summary>ProposalParams</summary>

Parameters pertaining to proposals' lifecycle.

_Members_:

* majority (felt): reject proposal if the percentage of YES votes among eligible votes is lower than majority.
* quorum (felt): reject proposal if the percentage of casted votes among eligible votes is lower than quorum.
* votingDuration (felt): duration of the voting period in block numbers.
* graceDuration (felt): duration of the grace period in block numbers.

</details>

The DAO keeps the current parametrisation in a mapping between proposal kind and parameters:

<details>

<summary>proposalParams</summary>

_Arguments_

* proposalKind (felt): the proposal kind to which the parameters apply

_Returns_

* ProposalParams

</details>

{% hint style="danger" %}
Misparametrisation of proposal kinds can lead to security issues. For example, setting the graceDuration to zero effectively disables the grace period, bypassing ragequit security mecanism for proposals of this kind.
{% endhint %}

## Implementing proposals &#x20;

All proposals follow the following minimum interface, where functions are allowed to have more arguments than default ones if necessary:

<details>

<summary>submit</summary>

_Arguments_

* description: felt
* more if needed

_Returns_

* success: felt

</details>

<details>

<summary>execute</summary>

_Arguments_

* proposalId: felt

_Returns_

* success: felt

</details>
