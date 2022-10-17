# Aditionnal features needed

The scope of our MVP implies to develop some additional functionalites on top Moloch V2:

* As **membership is restricted** to Quadratic's Employees, membership proposals cannot be voted by the DAO members but have to be enforced by an Admin who has the full view of the payroll
* As the firm can be accountable for the consequences of some processed proposals, **dedicated voting rights** have to be defined on some proposals (e.g. whitelisting, grants) or a right of veto can be introduced

Hence we developed :

* A **role based membership system** to make a distinction between Users and Admins in charge of actions (i) when accountability of the firm is at stake (ii) when the information to trigger an event is detained by the firm
* The ability to **adjust settings proposal per proposal** to grant each roles with the proper set of rights

## Role-based membership system <a href="#markdown-header-members" id="markdown-header-members"></a>

Our MVP uses a role-based membership system. Members are assigned roles, hence a different set of rights per type of proposal.

As of today, it includes 2 roles :

* **Administrator**: responsible for onboarding new members and whitelisting assets
* **Governor**: responsible for the governance of the assets.

We will further introduce the possbility to define any set of roles.

## Proposal custom settings

The MVP allows to customize any kind of proposal with a set of parameters:

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
* **Proposal vetoing:**
  * Which role(s) can veto a proposal (if not specified, no vetoing allowed)
