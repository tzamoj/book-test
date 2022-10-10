# Proposals

TODO: short module description

### Structs

<details>

<summary>ProposalParams</summary>

Description...

* majority (felt):
* quorum (felt):
* votingDuration (felt):
* graceDuration (felt):

</details>

<details>

<summary>ProposalInfo</summary>

Description

* id (felt):
* type (felt):&#x20;
* submittedBy (felt):&#x20;
* submittedAt (felt):
* status (felt):
* description (felt):

</details>

### Storage Variables

<details>

<summary>proposalParams</summary>

_Arguments_

* proposalKind (felt): the proposal kind to which the parameters apply

_Returns_

* ProposalParams

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

_Description_

</details>

<details>

<summary>execute</summary>

_Arguments_

* proposalId: felt

_Returns_

* success: felt

_Description_

</details>

## Submodules

{% content-ref url="proposals/guildkick.md" %}
[guildkick.md](proposals/guildkick.md)
{% endcontent-ref %}

{% content-ref url="onboard.md" %}
[onboard.md](onboard.md)
{% endcontent-ref %}
