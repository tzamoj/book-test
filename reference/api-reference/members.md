# Members

TODO: short module description

### Structs

<details>

<summary>MemberInfo</summary>

Structure containing basic information on a member

* address (felt): Member's account address
* delegatedKey (felt): Member's voting deleguate's address. The delegate is the one voting in the name of the member. It can be set to the member's address if delegation is unwanted.
* shares (felt): Number of shares the member has. Shares give both voting weight and financial weight.
* loot (felt): Number of loots the member has. Loot only give financial weight, but carries no voting rights.
* jailed (felt): Whether the member has been jailed, which can happen if guildkicked.
* lastProposalYesVote (felt): TODO (deprecated maybe...)

</details>

### Storage Variables

<details>

<summary>membersLength</summary>

Number of members in the DAO

_Arguments_: None

_Returns_: length (felt)

</details>

<details>

<summary>membersAddresses</summary>

List of the members' addresses

_Arguments_:

* index (felt): the positional index of the member

_Returns_:

* address (felt): the address of the member

</details>

<details>

<summary>membersInfo</summary>

Mapping of all members Info

_Arguments_:

* address (felt): member's address

_Returns_:

* member\_ (MemberInfo): member's info

</details>

### External Functions

<details>

<summary>addDelegatedKey</summary>

Allows a member to declare another member (possibly self) as a delegate

_Arguments_:

* delegateKey (felt): delegate's address

_Returns_:

* success (felt): whether the delegation was successful.

_Guards_:

* caller must be a member
* delegate must be a member

</details>

<details>

<summary>revokeDelegatedKey</summary>

TODO

</details>
