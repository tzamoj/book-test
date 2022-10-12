# Moloch V2 Overview

Moloch V2 operates through submission and voting of proposals.&#x20;

Applications for membership are managed through a proposal, where the applicant proposes an amount of Tokens (the _Tribute_) in exchange of some _Shares_ of the DAO.

The DAO treasury (the _Bank_), which initially includes all the _Tributes_ paid by DAO members, can also be managed through proposals, as transfer proposals (for grants) or trade proposals (swap of assets held by the _Bank_ with other assets, for investment purpose).

A member can exit the DAO at any time, as he can burn his/her _Shares_ and withdraw the part of the assets in the Bank he/she owns according to his shareholding.

## Moloch V2 Proposal Workflow

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

* DAO members can submit a proposal <mark style="color:red;">TODO paiement</mark>. A non DAO member can also submit a proposal to apply for membership. To be submitted, this proposal has to be sponsored by an existing DAO member.
* DAO members can vote for or against the submitted proposal during the voting period
* Once the voting period is over, if the proposal is approved by a majority of voters, the proposal enters a grace period
* During the grace period, members who voted against the proposal can exit the DAO (aka Ragequit)
* Once the grace period is over, any DAO member can process the proposal (aka execute it) ; users are incentivized to do so as they get a reward in the DAO's _Payment Token._



## Moloch V2 Main Proposal Types

### Membership

Anyone can apply to the DAO membership by submitting a proposal with :

* The desired number of _Shares_ of the DAO
* The _Tribute_ offered in exchange of the _Shares_ (aka an amount of whitelisted Tokens)

To enter the voting period, this proposal has to be sponsored by an existing DAO member who pays a fee in the DAO's _Payment Token_. If the proposal is approved and processed, the _Tribute_ is added to the DAO _Bank_ while the _Shares_ are minted and are allocated to the new member.

### Whitelisting

At DAO's setup, an ERC20 is defined as the DAO's Primary Token ; this Token is the Payment Token  and any Tribute offered has to be paid with this ERC20. To allow the _Tribute_ to be paid with another Token, and more generally to allow the Bank to manage other kinds of Tokens, a Whitelisting proposal has to be accepted and processed.

### Grant proposal

Any Member can propose to transfer a quantity of Tokens held by the Bank to an address.

### Trade proposal

Any Member can propose to swap an amount of X Tokens held by the Bank with Y whitelisted Tokens.

### Guildkick

Any member can propose to evict another Member from the DAO through a Guildkick Proposal. If this Guildkick Proposal is approved, the evicted Member's _Shares_ are converted into _Loots,_ aka _Shares_ without any voting right_._ Once all the Proposals approved by this Member are processed, the Member can redeem his Loots through a Ragequit (this operation can also be triggered by any Member through a Ragekick).

## Moloch V2 Ragequit mecanism

Any Member can leave the DAO with the Ragequit functionnality:

* A Member is allowed to withdraw his/her part of the Tokens held by the Bank based on his/her shareholding
* &#x20;_Shares_ are burned

The Ragequit functionality is not only a way to exit the DAO and redeem his Assets. It is also a security feature to protect DAO Members from 51% attacks : during the grace period, Members who voted NO or did not vote can Ragequit, claiming their shares before the proposal is processed; Members who voted YES cannot Ragequit until the grace period is over and the Proposal is processed.
