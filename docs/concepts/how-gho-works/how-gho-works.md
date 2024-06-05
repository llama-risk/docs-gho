# How GHO Works

GHO is a flexible, decentralized, overcollateralized stablecoin on the Ethereum Mainnet. It is available in the form of an ERC20 token that is designed to maintain a stable rate, pegged to the U.S. dollar, despite market volatility. GHO natively fits into the existing Aave Protocol as a new asset, meaning that interacting with the protocol to borrow GHO is similar to interacting with other assets in the Aave Pool:

![GHO_Architecture Diagram](../../assets/GHO_Architecture_dark.png#gh-dark-mode-only)
![GHO_Architecture Diagram](../../assets/GHO_Architecture.png#gh-light-mode-only)

**Supply Collateral –> Borrow GHO –> Repay GHO Debt**

GHO is created (“minted”) or repaid (“burned”) by Facilitators. GHO is minted upon the supply of assets more than the value of GHO to be minted. GHO is designed to accrue interest when it is borrowed, and this interest rate is determined by [Aave Governance](https://governance.aave.com/).

The following pages and [technical paper](https://github.com/aave/gho-core/blob/main/techpaper/GHO_Technical_Paper.pdf) describe the fundamental characteristics and smart contract design of GHO.

### GHO Implementation

While interacting with GHO is similar to interacting with other assets within the Aave Protocol, the [implementation](gho-implementation.md) of and user interaction with GHO as an asset in the Aave pool is quite different. The way that GHO is configured has differences that help it to maintain price stability.

### Interest and Discount Rates

The interest rate is the cornerstone of GHO stability, and, as in all decentralized protocols, it is built into the code. GHO smart contracts do not follow the usual supply and demand dynamics that often impact interest rates. Both the [interest rate and the discount rate](interest-rate-discount-model.md) are configurable by Aave Governance. The implementation of GHO includes a Discount Strategy mechanism, allowing Safety Module participants (i.e., stkAAVE holders) to access a discount on the GHO borrow rate.

### Facilitators

GHO introduces the concept of [Facilitators](gho-facilitators.md). A Facilitator can trustlessly mint and burn GHO tokens through various strategies. Different entities can implement these strategies and may employ varying strategies to integrate GHO (each entity is a facilitator). The Aave DAO assigns each Facilitator a Bucket with a specified capacity, where a Bucket represents the upward limit of GHO that a specific Facilitator can mint. Aave Governance defines this limit.

### Governance

The Aave Protocol is a fully decentralized, community-governed protocol managed by AAVE (and stkAAVE) token holders. Token holders collectively discuss, propose, and vote on upgrades to the Aave Protocol through Aave [Governance](gho-governance.md). AAVE and stkAAVE token holders (Ethereum network only) can vote on new proposals or delegate their voting power to an address of choice.

### Risk Management and Mitigations

As is typical with all smart contracts built by the Aave Companies, there has been a focus on [risk management and mitigation](./risk-man-mitigations.md) for GHO.

## Fundamental Concepts

These pages show the different mechanisms involved with GHO, such as how to [borrow](../fundamental-concepts/borrow-gho.md) and [repay](../fundamental-concepts/repay-liquidate-gho.md) GHO, how [staking benefits](../fundamental-concepts/gho-discount-strategy.md) users, [arbitrage](../fundamental-concepts/arbitrage.md), and how to [FlashMint](../fundamental-concepts/flashmint.md).

## Smart Contracts

These pages dive into the GHO smart contracts to [explore GHO at a technical level](../../developer-docs/developer-docs-overview.md). The code design includes software-based mechanisms for the emission and destruction of GHO, for controlling the stability of GHO, and for the role of Aave Governance and Facilitators in managing and maintaining GHO.

## Resources

For [more information](../../resources/resources.md), please see the GHO Glossary, which includes audits and community resources.
