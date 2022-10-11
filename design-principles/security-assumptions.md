# Security Assumptions

The Cairo version will allow to fully customize Roles and Proposal parameters. If it will be possible to implement the Moloch V2 features as they stand, it will be also possible to introduce some mecanisms that bypass DAO Members rights. For example:

* Some actions on Proposals can be restricted to some Roles (e.g. submission restricted to Admins)
* The voting phase can be skipped
* Some Roles can veto a Proposal

If this flexibility leads to a much wider range of misbehaviors towards DAO Members than in Moloch V2 (mainly 51% attacks), the protection of the DAO Members relies in the abiity to Ragequt and exit the DAO. That being said this possbility:

* Can be ineffective, if the DAO parameters are not correctly set (e.g. non consistent grace periods)
* Relies on the assumption that the Assets under management are liquid and hence can be withdrawned in case of exit. This cannot be the case for Claims or could be complicated to implement - &#x20;

