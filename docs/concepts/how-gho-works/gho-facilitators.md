# Facilitators

## What is a Facilitator?

GHO introduces the concept of Facilitators. A Facilitator can trustlessly mint and burn GHO tokens through various strategies. Different entities can implement these strategies and may employ varying strategies to integrate GHO (each entity is a facilitator). The Aave DAO assigns each Facilitator a Bucket with a specified Capacity, the upward limit of GHO that a specific Facilitator can mint. This limit is defined and can be changed by the Aave DAO.

![Facilitator Diagram](../../assets/facilitator_dark.png#gh-dark-mode-only)
![Facilitator Diagram](../../assets/facilitator.png#gh-light-mode-only)

## Current Facilitators

Currently, multiple facilitators have been approved by Aave's Governance. Each Facilitator's mechanism serves a different purpose for GHO stablecoin and helps to support its stability.

### Aave V3 Ethereum Pool

The Aave V3 Ethereum Pool was accepted by the Aave DAO to serve as one of the initial Facilitators on the Ethereum Mainnet due to the risk-reducing features of this version of the protocol, including [Efficiency Mode](https://docs.aave.com/developers/whats-new/efficiency-mode-emode) (“E-Mode”), [Isolation Mode](https://docs.aave.com/developers/whats-new/isolation-mode), [Siloed Borrowing](https://docs.aave.com/developers/whats-new/siloed-borrowing), and [Supply/Borrow Caps](https://docs.aave.com/developers/whats-new/supply-borrow-caps). Therefore, Aave's Ethereum pool can mint and burn GHO in a decentralized and permissionless fashion, subject to Borrow Cap limitations set up by Aave's Governance.

The [Aave Protocol](https://aave.com/) is a liquidity protocol available on Ethereum and other L1 and L2 networks. Aave allows users to supply and borrow against a range of assets while simultaneously earning yield and participating in liquidations. The Aave Protocol operates on an overcollateralized model. Accordingly, GHO is overcollateralized as well.

### FlashMinter

The FlashMinter Facilitator is an entity that enables [FlashMinting](../fundamental-concepts/flashmint.md). FlashMinting is especially important for GHO as it helps to facilitate arbitrage, provide instant liquidity, and facilitate liquidation of unhealthy borrow positions.

As FlashMinting provides the same functionality as the current [flashloan](https://docs.aave.com/developers/guides/flash-loans) standard, it works very much the same (e.g., everything must be returned, and there will be a fee).

### GHO Stability Module

A Peg Stability Module (PSM) is a contract that enables the seamless conversion of two tokens at a predetermined ratio. This mechanism has proven effective for numerous stablecoin projects, helping preserve exchange rate stability. Using this model as inspiration, the Stability Module for GHO (GSM) leverages the benefits of existing models while innovating upon them in several ways to help further maintain GHO’s peg.

The GSM Facilitator introduces the concept of Price Strategies, which provide the ability to adjust the pricing ratio between GHO and the exogenous asset based on different strategies. Pricing strategies oversee the calculation of the price ratio and:
- Can be fixed.
- Can be dynamic, based on price oracles and markets, linear curves, stableswap curves, etc.

Currently, GSM is implementing a fixed pricing strategy where USDT and USDC can be used to mint GHO. Aave's Governance can change GSM market parameters. GHO Stability Module's interface is supervised by TokenLogic, an Aave DAO Service Provider, and can be accessed on a [dedicated website](https://app.gsm.tokenlogic.xyz/). 

## Become a Facilitator

Each Facilitator must be approved by [Aave Governance](https://governance.aave.com/). Before approval, Aave Governance must determine and assign a Facilitator a specific Bucket capacity to bootstrap GHO liquidity and the GHO market.

The framework for applying to become a Facilitator is described in [Aave's Governance Forum](https://governance.aave.com/t/arfc-gho-facilitator-onboarding-process-and-application/12929).

## Facilitator Strategies

GHO is minted through various strategies. Facilitators can apply different strategies to their generation of GHO. This allows Aave Governance to manage its exposure to different strategies across the ecosystem, with most strategies also helping GHO maintain its peg.

As it is up to Facilitators to decide their minting strategies, we expect to see exciting creativity in this area. For example, the Aave V3 Pool, one of the proposed initial Facilitators of GHO, operates on an overcollateralized model. As a result, GHO is overcollateralized.

Aave Governance may attract varied Facilitators in different ways. If Aave Governance approves new and additional Facilitators, the possibilities are endless.

## Facilitator Technical Fundamentals

A Facilitator ($F$) can trustlessly generate and burn GHO tokens. Each Facilitator is assigned a Bucket ($B$) with a specified Capacity ($C$). The Capacity ($C$) represents the upward limit of GHO that a specific Facilitator can generate. The amount of GHO tokens generated per each Facilitator is called Level ($L$). Fundamentally, all Facilitators must adhere to the following equation:

Given a set of Facilitators $F_0, F_1, ...F_{N − 1}$ each of which is associated with a certain Bucket with capacity ($CB_t$) and a current Bucket level at a given time ($LB_t$). The Available Supply ($AS_{GHO_t}$), is the maximum amount of GHO available to be minted through all the Facilitators at a given time ($t$), defined as follows:

$$
AS_{GHO_t} = \sum_{n=0}^{N-1} max(0, CB(n)_{t} - LB(n)_{t})
$$

:::info

It is important to note the exception to this preliminary equation. As the Aave DAO can change the Bucket Capacity, a Facilitator could have more GHO minted than its initial Capacity. This may occur if the Aave DAO has lowered the Bucket’s Capacity.

:::

Facilitators can be different in technical nature. As stablecoins can differ depending on the stabilization mechanisms they employ, with GHO, the idea is to use multiple stabilization mechanisms in a controlled fashion via the Aave DAO by properly balancing each Bucket capacity not to compromise overall system collateralization and stability.
