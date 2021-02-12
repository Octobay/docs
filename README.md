# Docs

0. [Overview](#Overview)
1. [Registration](https://octobay.github.io/docs/REGISTRATION.html)

## Overview

OctoBay is a decentralized bounty and promotion platform for open source projects, using the following technologies:

- Smart Contract and Token
- Chainlink Oracles
- The Graph
- Uniswap
- Gas Station Network

### Main Use Cases

#### Bounty

Funds are deposited in the smart contract for an issue on GitHub. Once the issue is closed, the author/contributor can request a withdrawal on which the Chainlink oracles check if the required conditions are met.

![image](https://user-images.githubusercontent.com/6792578/107638409-d6739200-6c6f-11eb-9833-ff94dedb57bc.png)

Possible conditions:

- A pull request got **merged into the default branch**, closing the issue **automatically**. (Default behavior if not specified otherwise by the maintainer of the issue's repository.)
- A pull request, mentioning the issue (in its description or a commit message ) with a close command (e.g. `closes #12`), got merged into a branch specified by the maintainer and the issue is closed.
- The maintainer comments on the issue in the form: `@OctoBay release to @user`. (Overrides previous conditions.)

OctoBay integrates Uniswap, to enable withdrawals in any currency, regardless of the deposits.

#### Tipping/Inviting

Any Ethereum account can send funds to any GitHub user. If the user is new to OctoBay, one of our oracles will send an email invitation or mention the user on GitHub (and Twitter, if available). The user creates a wallet and can withdraw the deposit via a gasless meta transaction, that is prepaid by the deposit and handled by our Gas Station Network relayer.

![image](https://user-images.githubusercontent.com/6792578/107783457-903f3100-6d4a-11eb-8ad2-87f680a8424b.png)

This process also works for issue bounties or repository funds. Those can also be accessed via gasless transactions for new users. User that already registered their GitHub account on OctoBay, can receive funds directly in their Ethereum wallet.
