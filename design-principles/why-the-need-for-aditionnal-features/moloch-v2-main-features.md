# Moloch V2 main features

Moloch V2 operates through submission and voting of proposals.&#x20;

Membership applications are managed through proposals, where applicants propose an amount of Tokens (the _Tribute_) in exchange of _Shares_ of the DAO.

The treasury (the _Bank_), which initially includes all the _Tributes_ paid by DAO members, can also be managed through proposals. Such proposals include (i) transfers, used for grants (ii) trades for investment purposes, such as swaps of _Bank's_ assets.

A member can exit the DAO anytime he/she wishes so. Exiting is done in a 2 steps process: the member burns his/her _Shares_ against ownership of the part of the DAO's assets represented by those shares, then withdraw the assets from the _Bank_.

## Moloch V2 Proposal Workflow

<figure><img src="../../.gitbook/assets/image (8) (2).png" alt=""><figcaption></figcaption></figure>

* DAO members can submit a proposal against a fee in the DAO's _Payment Token._ A non-member can also submit a proposal to apply for membership. To be submitted, this proposal has to be sponsored by an existing DAO member
* DAO members can vote for or against a submitted proposal during its voting period
* Once its voting period is over, if approved by a majority of voters, the proposal enters its grace period
* During its grace period, members who haven't approved the proposal can exit the DAO (aka Ragequit)
* Once its grace period is over, any DAO member can process the proposal (aka execute it). Members are incentivized to do so by a reward in the DAO's _Payment Token_

## Moloch V2 Main Proposal Types

### Membership

Anyone can apply for membership by submitting a proposal with:

* The desired number of _Shares_ of the DAO
* The _Tribute_ offered in exchange of the _Shares_ (aka an amount of whitelisted Tokens)

To enter its voting period, the proposal has to be sponsored by an existing DAO member against a fee in the DAO's _Payment Token_. If the proposal is approved and processed, the _Tribute_ is added to the _Bank_ while the _Shares_ are minted and allocated to the new member.

DAO members can also submit a membership proposal on behalf an external applicant.

### Whitelisting

At DAO's setup, an ERC20 is defined as the DAO's _Primary Token_ ; this Token is the _Payment Token_ and any _Tribute_ offered has to be paid with this ERC20. To allow the _Tribute_ to be paid with another Token, and more generally to allow the _Bank_ to manage other kinds of Tokens, a whitelisting proposal has to be accepted and processed.

### Grant proposal

Any member can propose to transfer a quantity of Tokens held by the _Bank_ to an external address.

### Trade proposal

Any member can propose to swap an amount of X Tokens held by the _Bank_ with Y whitelisted Tokens.

### Guildkick

Any member can propose to evict another member from the DAO through a Guildkick proposal. If a Guildkick proposal is approved, the evicted member's _Shares_ are converted into _Loots,_ aka _Shares_ without any voting right_._ Once all the proposals approved by this member are processed, the member can redeem his _Loots_ through a Ragequit (this operation can also be triggered by any member through a Ragekick).

## Moloch V2 Ragequit mecanism

Any member can leave the DAO with the Ragequit functionnality:

* A member is allowed to withdraw his/her part of the Tokens held by the _Bank_ based on his/her shareholding
* &#x20;His/her _Shares_ are burned

The Ragequit functionality is not only a way to exit the DAO and redeem your assets. It is also a security feature to protect DAO members from 51% attacks: during the grace period, members who voted NO or did not vote can Ragequit, claiming their _Shares_ before the proposal is processed; Members who voted YES cannot Ragequit until the grace period is over and the proposal is processed.
