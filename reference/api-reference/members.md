# Members

The module is mainly used internally for DAO members' management. It keeps track of basic information on members (see MemberInfo struct), and implements create, read, update, delete operations on them.&#x20;

## Stored Onchain

The DAO registers basic information on its members for its internal usage. A member's info are kept in the following structure:

<details>

<summary>MemberInfo (struct)</summary>

Structure containing basic information on a member

_Members_:

* address (felt): Member's account address
* delegatedKey (felt): Member's voting deleguate's address. The delegate is the one voting in the name of the member. It can be set to the member's address if delegation is unwanted. See [#delegation](members.md#delegation "mention").
* shares (felt): Number of shares the member has. Shares give both voting weight and financial weight.
* loot (felt): Number of loots the member has. Loot only give financial weight, but carries no voting rights.
* jailed (felt): Whether the member has been jailed, which can happen if guildkicked. Jailed members cannot vote nor submit proposals.
* lastProposalYesVote (felt): TODO (deprecated maybe...)

</details>

The DAO stores a list of its members' addresses along with a mapping between those addresses and the member's info. Internally, this is accomplished with the following 3 storage variables:

<details>

<summary>membersLength (storage_var)</summary>

Number of members in the DAO

_Arguments_: None

_Returns_: length (felt)

</details>

<details>

<summary>membersAddresses (storage_var)</summary>

List of the members' addresses

_Arguments_:

* index (felt): the positional index of the member

_Returns_:

* address (felt): the address of the member

</details>

<details>

<summary>membersInfo (storage_var)</summary>

Mapping of all members Info

_Arguments_:

* address (felt): member's address

_Returns_:

* member\_ (MemberInfo): member's info

</details>

There are events triggered when there is a change to the stored members, that it be the addition of a new member, or any of the possible events modifying the info of an existing member (delegation, ragequit, guildkick, Yes vote, ...):

<details>

<summary>MemberAdded (event)</summary>

Triggered when a new member is added to the DAO.

_Parameters_:

* memberAddress (felt): the new member's address
* shares (felt): the new member's number of shares
* loot (felt): the new member's number of loot

</details>

<details>

<summary>MemberUpdated (event)</summary>

Triggered when an existing member's info are modified.

_Parameters_:

* memberInfo (MemberInfo): the member's new info.

</details>

## Delegation

Each member also has the possibility to delegate his/her vote to another address through the delegatedKey mechanism. The delegateKey is fully managed by the owner, but the delegate has to be a member of the DAO. By default, the delegate and the member are the same, meaning in effect no delegation.

The following external functions are available for delegate management:

<details>

<summary>delegateVote (external func)</summary>

Allows a member to declare another member (possibly self) as a delegate

_Arguments_:

* delegatedKey (felt): delegate's address

_Returns_:

* success (felt): whether the delegation was successful.

_Guards_:

* caller must be a member
* delegate must be a member

</details>

<details>

<summary>revokeDelegate (external func)</summary>

The caller revokes his/her delegate. This is a convenience function for calling addDelegatdKey with his/her own address as a delegate.

_Returns_:

* success (felt): whether the function succeeded.

_Guards_:

* caller must be a member.

</details>
