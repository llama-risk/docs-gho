---
sidebar_position: 3
---

# Governance

The Aave Protocol is a fully decentralized, community-governed protocol, managed by AAVE (and stkAAVE) token holders. Token holders collectively discuss, propose, and vote on upgrades to the Aave Protocol through [Aave Governance](https://governance.aave.com/). AAVE and stkAAVE token holders (Ethereum network only) can either vote on new proposals or delegate their voting power to an address of choice.

As GHO is decentralized, it does not have a single concentrated point of control. Instead, GHO is controlled by Aave Governance. The Aave Companies do not have any control over GHO.

## Governance Resources

The Aave Companies [introduced GHO](https://governance.aave.com/t/introducing-gho/8730) to the Aave DAO on July 7, 2022.

Following a period of discussion, the community voted to greenlight GHO via [Snapshot](https://snapshot.org/#/aave.eth/proposal/0xb17b3294dcb08316cb623c717add7f82df54948d558992f886be59d0958e9b24).

The first [GHO Development Update](https://governance.aave.com/t/gho-development-update/10267) was published on October 14, 2022.

The second [GHO Development Update (Testnet Release)](https://governance.aave.com/t/gho-development-update-testnet-release/11631) was published on February 9, 2023.

GHO was launched in July, 2023 after Aave's governance passed the [GHO Launch proposal](https://governance.aave.com/t/arfc-gho-mainnet-launch/13574).

## Governance Role

Aave Governance has the right to determine GHO Facilitators and parameters and to propose changes to the current implementation. Frameworks and processes for Facilitators, caps, and rates are open to community discussion. Aave's Governance has also created and/or assigned multiple entities to supervise GHO stablecoin and help maintain its stability.

### Facilitators

Aave Governance has control over the entities that are added and removed as [Facilitators](./gho-facilitators.md). Every Facilitator is carefully audited and reviewed by Aave Governance before receiving mint permissions. In addition, each Facilitator has a governance-defined limit on how much GHO it can mint.

By carefully approving each Facilitator, Aave Governance can manage exposure to different [strategies](./gho-facilitators.md#facilitator-strategies). Aave Governance may want to attract varied Facilitators in several different ways. This could also include strategies for non-Aave users. If non-Aave Protocol Facilitators are approved by Aave Governance, the possibilities and use cases could be endless (e.g., use within payment applications and e-commerce solutions, purchases of GHO on decentralized exchanges, and use as a store of value during market volatility).

## Aave (GHO) Liquidity Committee

The GHO Liquidity Committee (GLC) was created in October 2023 to focus solely on the liquidity of the GHO stablecoin. The committee was formed through a [governance proposal](https://governance-v2.aave.com/governance/proposal/343/) and consisted of a small team. After a successful initial 3-month period it was integrated into Aave Liquidity Committee (ALC).

The ALC's main responsibilities regarding GHO include:
* Providing analytics and modeling of the liquidity strategy
* Liaising with teams that support the protocols hosting GHO liquidity
* Leading and coordinating the committee's weekly activities
* Providing critical feedback and helping refine the strategy
* Verifying and signing transactions
    
The ALC's performance measures and liquidity targets for GHO can be found on the [GHO Analytics platform](https://aave.tokenlogic.xyz/liquidity-committee) provided by TokenLogic.

As of May 2024, the members of the committee are:

- Figue (Paladin)
- Marc Zeller (ACI)
- Emilio (Avara)
- sisyphos (Kpk)
- Matt (Tokenlogic)

More information regarding the role of GHO Liquidity Committee can be found in [Aave's Governance forum](https://governance.aave.com/t/temp-check-treasury-management-create-and-fund-gho-liquidity-committee/14800).

## GHO Stewards

GHO Stewards is an additional entity that was created in April 2024 to more flexibly manage GHO market parameters enabling GHO to be scaled in accordance with prevailing market conditions.

The GHO Stewards determine if and how much to adjust the following, subject to pre-defined and Governance accepted thresholds:

- GHO Borrow Cap
- GHO Borrow Rate
- GSM Exposure Cap
- GSM Bucket Capacity
- GSM Price Strategy
- GSM Fee Strategy
- GSM Price Range (Freeze, Unfreeze)

With many liquidity pools to be created and rewards distributed across, it is important the DAO can swiftly increase the GHO Borrow Cap to mitigate GHO trading above $1. The GHO Stewards will be able to increase the GHO Borrow Cap swiftly to mitigate GHO trading above peg. The GHO Stewards can increase the GHO Borrow Cap up to a threshold of 50M units to a total borrow cap of 100M.

The Borrow Rate is to be adjusted gradually to enable the ecosystem to expand in a safe way. If the trailing 30 day average price of GHO stays outside a $0.995 - $1.005 price range, the GHO Stewards are able adjust the Borrow Rate no more than 500bps per 2 day period, up to a maximum 25% APR.

GHO Stewards consists of members from Growth (ACI), Risk (ChaosLabs) and Finance (TokenLogic + karpatkey) Service Providers and utilise a 3 of 4 multi-sig.

## Impact on Aave's DAO

With the GHO model, 100% of interest paid on borrowed GHO goes to the Aave DAO. Depending on the demand for GHO, this could result in substantial revenue for the Aave DAO. Alongside this, the [FlashMint](../fundamental-concepts/flashmint.md) module generates revenue through the fees from the transaction. As mentioned above, there may be various strategies implemented for future Facilitators. It is possible that future Facilitators may also redirect some revenue to the DAO.
