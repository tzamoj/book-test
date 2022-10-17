# 🛡 Security Assumptions

Our MVP will allow to fully customize roles and proposal parameters. If it will be possible to implement the Moloch V2 features as they stand, it will be also possible to **introduce some mecanisms that bypass DAO members' rights**. For example:

* Some actions on proposals can be restricted to specific roles (e.g. submission restricted to Admins)
* The voting period can be skipped altogether (e.g. an Admin whitelisting a token)
* Some roles can veto a proposal

This flexibility leads to **a wider range of misbehaviors towards DAO members than in Moloch V2** (where the main risk is 51% attacks). As in Moloch V2, members' **protection relies in the ability to Ragequit** and exit the DAO. However, this mecanism:

* Can be ineffective, if the DAO's parameters are not correctly set (e.g. non consistent grace periods)
* Relies on the assumption that the assets under management are liquid, can be fully withdrawned and redeemed in case of exit. This cannot be the case for Claims (as of the Metacartel definition) or can be complicated to implement (e.g. NFTs).

