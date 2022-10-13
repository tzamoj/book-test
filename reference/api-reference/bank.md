# Bank

The bank serves as (i) a safe for the DAO's assets (ii) a ledger to keep accounting entries.&#x20;

## Accounts

Accounts keep track of assets owned by users of the DAO. However, they are only for accounting purposes, as the assets are in reality owned by the DAO and stored in their respective ERC20 contracts under the DAO's contract address.

All members have an account with the bank, allowing them to interact financially with the DAO.&#x20;

Also, there are 3 reserved special accounts:

* guild: the mutual fund, holding assets shared by members.
* escrow: a temporary account used to lock assets while waiting for proposals to be closed.
* total: the sum of guild and escrow.

Accounts information are stored onchain in the following storage var:

<details>

<summary>userTokenBalances (storage_var)</summary>

_Arguments_:

* userAddress (felt): the user's address. The guild has a special reserved address, as well as the escrow and the total.
* tokenAddress (felt): the token address.

_Returns_:

* amount (felt): the number of token owned by the user.

</details>

## Whitelisting Tokens

The bank can accept only whitelisted token addresses. This regulation measure provides members' security against infected tokens.

Tokens can be whitelisted through a proposal. The DAO stores a list of whitelisted tokens:

<details>

<summary>whitelistedTokensLength (storage_var)</summary>

_Returns_: (felt) the number of whitelisted tokens

</details>

<details>

<summary>whitelistedTokensIndexes (storage_var)</summary>

The list of whitelisted tokens' address

_Arguments_:

* index (felt): positional index of the token

_Returns_:

* tokenAddress (felt)

</details>

For convenience, it also stores a mapping of addresses to boolean.&#x20;

<details>

<summary>whitelistedTokens (storage_var)</summary>

Whether a given address has been whitelisted

_Arguments_:

* tokenAddress (felt)

_Returns_:

* whitelisted (felt): whether the token is whitelisted

</details>

## Transactions

A member can deposit/withdraw tokens to his/her account at any time through the following external functions:

<details>

<summary>deposit (external function)</summary>

Transfer ERC20 tokens from the caller's address to the bank's address

_Arguments_:

* tokenAddress (felt)
* amount (felt)

_Returns_:

* success (felt): whether the transfert was successful

</details>

<details>

<summary>withdraw (external function)</summary>

Transfer tokens from the bank's address to the caller's address.

_Arguments_:

* tokenAddress (felt)
* amount (felt)

_Returns_:

* sucess (felt):  whether the transfer was successful

</details>
