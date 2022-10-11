# Security Assumptions

Moloch on Starknet  will allow to fully customize roles and proposal parameters. If it will be possible to implement the Moloch V2 features as they stand, it will be also possible to introduce some mecanisms that bypass DAO members rights. For example:

* Some actions on proposals can be restricted to some roles (e.g. submission restricted to Admins)
* The voting phase can be skipped
* Some roles can veto a proposal

This flexibility leads to a much wider range of misbehaviors towards DAO members than in Moloch V2 (mainly 51% attacks) ;as in Moloch V2 the protection of the DAO members relies in the abiity to Ragequit and exit the DAO. That being said this possibility:

* Can be ineffective, if the DAO parameters are not correctly set (e.g. non consistent grace periods)
* Relies on the assumption that the assets under management are liquid, can be fully withdrawned and redeemed in case of exit. This cannot be the case for Claims (as of the Metacartel definition) or can be complicated to implement (e.g. NFTs).

