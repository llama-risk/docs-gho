---
sidebar_position: 1
---

# Why GHO?

Stablecoins play an important role in the DeFi ecosystem, offering a fast, efficient, and borderless way to transfer stable value. With many alternatives already in circulation, why develop yet another stablecoin?

### Market Demand

Based on the current state of the market, more adoption of decentralized stablecoins and room for growth still need to be made. Furthermore, recent regulatory scrutiny and operational challenges faced by centralized stablecoins have highlighted the need for truly decentralized options that can offer greater transparency and resistance to censorship. This has created a significant demand for decentralized stablecoins that are robust and secure and capable of maintaining stability independently of centralized control. GHO aims to fill this gap by providing a reliable, community-governed alternative addressing these market needs.

### Aave Protocol Infrastructure

The integration of GHO within the Aave ecosystem leverages Aave's established infrastructure and user base, enhancing GHO's credibility and accessibility. Aave's platform, known for its robust lending and borrowing services, provides a fertile ground for GHO's utilization. It allows users to mint GHO by depositing various types of collateral into Aave's lending pool. This over-collateralization ensures that GHO maintains its value stability, even during periods of market turbulence.

Moreover, Aave's governance entities and risk management providers actively monitor and support GHO's stability. The dynamic adjustment of collateral requirements, interest rates, and other key parameters by Aave Governance ensures that GHO can adapt to changing market conditions while safeguarding against risks.

The Aave Protocol, as a community-approved [Facilitator](./how-gho-works/gho-facilitators.md) (see below), can trustlessly mint and burn GHO tokens. Currently, there are multiple facilitators for GHO, and each is discussed in depth in the [Facilitators](./how-gho-works/gho-facilitators.md) section.

# How is GHO Different?

Significant demand exists for a stablecoin that is decentralized, over-collateralized, and configurable. How does GHO address these needs?

### Decentralized vs. Centralized Stablecoins

| Decentralized Stablecoins                                                                                                  | Centralized Stablecoins                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Enables a new level of transparency and censorship resistance, reinforcing the privacy and decentralization ethos. | Require users to trust the issuer of the stablecoin. Centralized stablecoins can be blacklisted at any time, and their backing may be opaque. |

Decentralized stablecoins, like GHO, provide censorship resistance and, most importantly, user transparency.

GHO is decentralized and intentionally does not have one single concentrated control point. GHO is controlled by Aave Governance and the Aave Protocol's community. With Aave Governance making all decisions relating to GHO, this asset has increased transparency compared to other stablecoins in the market.

In addition, all [GHO code](https://github.com/aave/gho-core) is open source and has been [audited](../resources/resources.md#audit-round-1) extensively by security firms before launch. All protocol upgrades and updates to interest rates/risk parameters are public and must be agreed upon by Aave Governance before execution.

### Multi-Collateral Positions

Traditionally, in the DeFi ecosystem, users mint decentralized stablecoins via single asset-backed vaults. GHO is multi-collateralized, meaning users can mint GHO based on their supplied collateral assets across the Aave Protocol. As a result, GHO will be backed by various types of assets.

While there are key differences concerning the implementation of GHO (please see the "[How GHO Works](./how-gho-works/how-gho-works.md)" page for a more detailed explanation), the process of interacting with the Aave Protocol and borrowing GHO is similar to that of other assets (i.e., a user will supply assets into the Aave Protocol and enable them to be used as collateral, and these assets can then be used to mint GHO, opening a multi-collateral backed borrowing position).

Using multiple different assets within the same borrowing position creates more flexibility for a user and allows for greater control over exposure to price fluctuations. This flexibility is beneficial for users in cases where they want to increase their health factor. Having multi-collateral positions means that a user would not have to balance multiple positions and health factors and would not have to swap between assets to fund a position.

### Interest-Earning Collateral

When a user supplies collateral to the Aave Protocol, other users borrow the supplied assets. Interest is earned on the supplied collateral, effectively reducing the interest a user is paying on their borrowed positions.

In the context of GHO, this dynamic is particularly advantageous. When a user supplies collateral to mint GHO, not only does the collateral secure the stablecoin's value, but it also generates interest. This interest accrual happens in real time as other users borrow the supplied assets—consequently, the user who minted GHO benefits from an additional income stream generated by their collateral.

### Trustless Minting

Trust is an essential component of a stablecoin. GHO introduces the concept of Facilitators. A Facilitator (e.g., a protocol or an entity) can trustlessly mint and burn GHO tokens. The Aave DAO must approve facilitators and can apply different strategies to their generation of GHO.

As a community-approved [Facilitator](./how-gho-works/gho-facilitators.md), the Aave Protocol can trustlessly mint and burn GHO tokens. 

Currently, there are multiple Facilitators for GHO, and each is discussed in depth in the [Facilitators](./how-gho-works/gho-facilitators.md) section.

### Interest and Discount Rate Models

For GHO, there are no suppliers, so interest rates work differently. GHO borrow interest rate is set by the Aave DAO. Aave Governance can periodically change the interest rates to help maintain stability with supply and demand.

Users who participate in staking their AAVE tokens in the Safety Module benefit by having access to a discount on the borrowing rate of GHO. Therefore, holders of AAVE are incentivized to stake it while helping to secure the AAVE Protocol as AAVE flows into the protocol's Safety Module.

For more information, please see the [Interest and Discount Rate Models](./how-gho-works/interest-rate-discount-model) page.

# What is The Future of GHO?

Stablecoins are tied to the wider adoption of the crypto ecosystem by making stablecoins the currency of web3. What is GHO going to look like in the future?

### Aave Roadmap

Synergies with the Aave Protocol ecosystem, future products, and deployments make GHO critical for the Aave Protocol's future roadmap.

### L2 Deployment

The current accessibility of GHO, primarily through minting on the Ethereum mainnet or via secondary markets, significantly limits its potential reach and utility within the DeFi landscape. Transitioning to a cross-chain model will enhance GHO's accessibility and liquidity, appeal to a broader user base, and provide the benefit of lower transaction costs.

### Additional Facilitators

In the future, Aave Governance may vote to add additional Facilitators. Once a new facilitator is approved, it can mint GHO.

### DeFi Ecosystem

The usage of stablecoins will likely grow as more people are onboarded into crypto and the number of blockchain transactions increases. This will contribute to the growing supply and circulation of GHO stablecoin, allowing it to be utilized in different market venues.
