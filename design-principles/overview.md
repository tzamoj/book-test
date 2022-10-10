# Overview

## Moloch V2 Proposal Workflow

<figure><img src="../.gitbook/assets/proposals workflow.png" alt=""><figcaption></figcaption></figure>

Once a Proposal is submitted:

* DAO Members can vote for or against the Proposal during the Voting Period
* Once the Voting Period over, if the Proposal is approved by a majority of Voters, the Proposal enters a Grace Period
* During the Grace Period, Members who voted against the Proposal can exit the DAO (aka Ragequit)
* Once the Grace Period over, any DAO Member can process the Proposal (aka execute it) ; users are incentivized to process the Proposals as they get a fee in the _Payment Token_ of the DAO



## Moloch V2 Main Proposal Types

### Membership

Anyone can apply to the DAO Membership by submitting a proposal with :

* The desired number of _Shares_ of the DAO
* The _Tribute_ offered in exchange of the _Shares (_aka an amount of whitelisted Tokens)

To enter the Voting Period, this Proposal has to be sponsored by an existing member of the DAO who pays a fee in the _Payment Token_ of the DAO . If the Proposal is approved and processed, the Tribute is added to the DAO Bank and the Shares are minted and allocated to the new Member

### Whitelisting

At the setup of the DAO an ERC20 is defined as the Primary Token of the DAO ; this Token is the Payment Token of the DAO and any Tribute offered has to be paid with this ERC20. To allow the Tribute to be paid with another Token, and more generally to allow the Bank to manage other kinds of Tokens, a Whitelisting proposal has to be accepted and processed.

### Grant proposal

Any Member of the DAO can propose to transfer a quantity of Tokens held by the DAO Bank to an adress.

### Trade proposal

Any Member of the DAO can propose to swap an amount of X Tokens held by the DAO Bank with Y whitelisted Tokens.

### Guildkick

Any member of the DAO can propose to evict another Member from the DAO through a Guildkick Proposal. If this Guildkick Proposal is approved, the _Shares_ of this Member are converted into _Loots,_ aka _Shares_ without any voting right_._ Once all the Proposals approved by this Member are processed, the Member can redim his Loots through a Ragequit (this operation can also be triggered by any Member of the DAO through a RageKick).



## Moloch V2 Ragequit mecanism

Any Member can leave the DAO using the Ragequit functionnality













