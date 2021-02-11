# Docs

Documentation for the OctoBay project

For now this repository is just a collection of things worth writing down.

1. [Registration](https://octobay.github.io/docs/REGISTRATION.html)

# Overview

OctoBay is a decentralized bounty platform, with governance and promotional features, using the following technologies:

- Smart Contract and Token
- Chainlink Oracles
- The Graph
- Uniswap
- Gas Station Network


## Main Use Case

![image](https://user-images.githubusercontent.com/6792578/107627018-f3539980-6c5e-11eb-8d6c-ab42c19f0f87.png)

Funds are deposited in the smart contract for an issue on GitHub. Once the issue is closed, the author/contributor can request a withdrawal on which the Chainlink oracles check if the required conditions are met.

Possible conditions:

- A pull request got **merged into the default branch**, closing the issue **automatically**. (Default behavior if not specified otherwise by the maintainer of the issue's repository.)
- A pull request, mentioning the issue (in its description or a commit message ) with a close command (e.g. `closes #12`), got merged into a branch specified by the maintainer and the issue is closed.
- The maintainer comments on the issue in the form: `@OctoBay release to @user`. (Overrides previous conditions.)
