# Aditionnal features

The initial Use Case that motivated the development of the Alpha version (setup of Quadratic Employees profit sharing fund) implied to develop some additional functionalites on top Moloch V2:

*

## Role-based membership system <a href="#markdown-header-members" id="markdown-header-members"></a>

Moloch on Starknet uses a role-based membership system. Members are assigned roles, hence a different set of rights per type of proposal.

Alpha version includes 2 roles :

1. Administrator: responsible for onboarding new members and whitelisting assets
2. Governor: responsible for the governance of the assets.

The Beta version will allow to define any set of roles.

## Proposal custom settings

Each proposal type can be customized with a set of parameters:

* **Proposal time limits:**
  * Voting period
  * Grace period
* **Proposal submission:**
  * Which role(s) can submit a proposal
  * Bypass voting period (Y/N)
* **Proposal sponsoring:**
  * Which role(s) can sponsor a proposal (if not specified, no sponsoring needed)
* **Proposal voting:**&#x20;
  * Which role(s) can vote on a proposal
  * Quorum needed
  * Majority needed
* **Proposal vetoing;**
  * Which role(s) can veto a proposal (if null, no vetoing allowed)
