# API Reference

Dive into the specifics of each API endpoint by checking out our complete documentation.

### Proposals

Proposals all follow the following minimum interface, where functions are allowed to have more arguments than default ones if necessary:

#### Structs

<details>

<summary>ProposalParams</summary>

*

</details>

{% hint style="info" %}
Example hint (remove)
{% endhint %}

```
// Example code
```

> Example quote

#### Storage variables

<details>

<summary>proposalParams</summary>

_Arguments_

* proposalKind (felt): the proposal kind to which the parameters apply

_Returns_

* ProposalParams

</details>

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

#### GuildKick



{% content-ref url="pets.md" %}
[pets.md](pets.md)
{% endcontent-ref %}

## Users

Everything related to users:

{% content-ref url="users.md" %}
[users.md](users.md)
{% endcontent-ref %}

{% hint style="info" %}
**Good to know:** Using the 'Page Link' block lets you link directly to a page. If this page's name, URL or parent location changes, the reference will be kept up to date. You can also mention a page – like [pets.md](pets.md "mention") – if you don't want a block-level link.
{% endhint %}
