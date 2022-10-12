# Proposals

This is a library module on which proposal submodules are based on.

_Proposal_ _Kind_ : Each proposal made is of a certain kind. For example, it can be a member onboarding, or a financial swap. Proposal's logic are implemented in submodules, one for each kind.

_Parameters:_ A proposal have parametrisable rules governing its lifecycle. These parameters apply on a proposal kind basis as different kinds of proposals may have different needs.

{% hint style="danger" %}
Misparametrisation of proposal kinds can lead to security issues. For example, setting the graceDuration to zero effectively disables the grace period, bypassing ragequit security mecanism for proposals of this kind.
{% endhint %}

### Structs

<details>

<summary>ProposalParams</summary>

Parameters pertaining to proposals' lifecycle.

_Members_:

* majority (felt): reject proposal if the percentage of YES votes among eligible votes is lower than majority.
* quorum (felt): reject proposal if the percentage of casted votes among eligible votes is lower than quorum.
* votingDuration (felt): duration of the voting period in block numbers.
* graceDuration (felt): duration of the grace period in block numbers.

</details>

<details>

<summary>ProposalInfo</summary>

Basic information saved per submitted proposal.

* id (felt): An incremental identifier for the proposal.
* kind (felt): The proposal's kind as a short-string.&#x20;
* submittedBy (felt): Address of the submiter.
* submittedAt (felt): Number of the block which includes the proposal's submission.
* status (felt): The actual state of the proposal in its lifecycle.
* description (felt): A short string describing the proposal's content.

</details>

### Storage Variables

<details>

<summary>proposalParams</summary>

_Arguments_

* proposalKind (felt): the proposal kind to which the parameters apply

_Returns_

* ProposalParams

</details>

<details>

<summary>proposalsLength</summary>



</details>

### Functions

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

## Submodules

{% content-ref url="proposals/guildkick.md" %}
[guildkick.md](proposals/guildkick.md)
{% endcontent-ref %}

{% content-ref url="onboard.md" %}
[onboard.md](onboard.md)
{% endcontent-ref %}
