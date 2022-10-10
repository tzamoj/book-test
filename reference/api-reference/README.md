# API Reference

## Modules



## Proposals

#### Structs

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

#### Storage variables

<details>

<summary>proposalParams</summary>

_Arguments_

* proposalKind (felt): the proposal kind to which the parameters apply

_Returns_

* ProposalParams

</details>

#### Functions

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

### GuildKick

Description

<details>

<summary>submit</summary>

_Arguments_

* memberAddress (felt): member to guildkick
* description (felt):&#x20;

_Returns_

* success (felt):&#x20;

</details>

## Users

Everything related to users:

{% content-ref url="proposals/onboard.md" %}
[onboard.md](proposals/onboard.md)
{% endcontent-ref %}

{% hint style="info" %}
**Good to know:** Using the 'Page Link' block lets you link directly to a page. If this page's name, URL or parent location changes, the reference will be kept up to date. You can also mention a page – like [guildkick.md](proposals/proposals/guildkick.md "mention") – if you don't want a block-level link.
{% endhint %}
