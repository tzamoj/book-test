# Architecture overview

## Technical Stack

* Front-end : Client-only Webapp - Astro<img src="../.gitbook/assets/astro.png" alt="" data-size="line">
* Back-end : Hosted, read-only, relies on indexing : Apibara <img src="../.gitbook/assets/apibara (1).png" alt="" data-size="line">, MongoDB <img src="../.gitbook/assets/mongo.png" alt="" data-size="line">, GraphQL<img src="../.gitbook/assets/GraphQL.png" alt="" data-size="line">
* Smart Contrats : Cairo <img src="../.gitbook/assets/cairo.svg" alt="" data-size="line"> Starknet <img src="../.gitbook/assets/image (2).png" alt="" data-size="line">

## Smart Contracts&#x20;

Like Moloch V2, the DAO is deployed as a single contract. Although not strictly necessary, it can deployed as an upgradeable contract through a proxy.

The DAO's contract follows a modular design that allows to (i) incorporate only the modules that are needed (ii) extend existing functionalities with new modules (implementing a minimal interface). This departure from Moloch V2 gives the DAO extra flexibility allowing to personalise its functionalities while keeping a simple maintainable design.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Unlike Moloch V2, every type of proposal has its own module separatedly implementing submiting and processing logic. One of the reasons to do so is to make their lifecycle more configurable, especially regarding role-based autorisation on a per type basis. For example in Alpha version, only Admins are allowed to onboard a new member, as other members are not legally accountable for that action.
