---
sidebar_position: 1
---

# GHO Implementation

While interacting with GHO is similar to interacting with other assets within the Aave Protocol, the implementation of and user interaction with GHO as an asset in the Aave pool is quite different. The way that GHO is configured has differences that help it to maintain price stability.

GHO is minted and burned by the smart contracts on demand when a user borrows and repays, respectively. GHO is not supplied to the Aave pool.

### Other Assets

All other assets must be supplied to the Aave Protocol by users, and only once supplied can they be borrowed from the reserve. For example, if a user deposits USDC and would like to borrow LINK, another user must have supplied LINK for the user to borrow it later.

This is not required for GHO.

### GHO

If a user supplies USDC and would like to borrow GHO, there is no requirement for a user to have supplied GHO. Instead, the Aave Protocol calls the GHO contract and mints GHO on demand. When repaying GHO debt, GHO is burned via smart contracts when the amount repaid exceeds the interest to pay, rather than going back to the suppliers.

This provides more flexibility than regular assets in the pool. GHO is minted on demand, so the user does not have to rely on the supplied assets.

## The GHO Oracle Price is Fixed at One U.S. Dollar

Regardless of market price, the Aave Protocol will always value 1 GHO at the equivalent value of 1 USD, regardless of market price. This helps to maintain stability.

As the price is fixed, it creates immediate opportunities to help GHO maintain its peg.

For example, when the GHO price is above the peg, users can mint 1 GHO for $1 worth of debt. If the price of GHO is above $1 in the market, users can sell GHO for more than $1. This increases the supply of GHO while decreasing the asset price. The minter can later repay their debt at $1 while keeping the difference of what they sold GHO for.

When the price of GHO is below the peg, minters can acquire 1 GHO on the market for less than $1 and pay off $1 worth of debt. This action shrinks the supply of GHO while increasing the asset price.

GHO is an over-collateralized asset, where every GHO is backed by more than $1 of collateral. This model has proved its resilience in the DeFi ecosystem for years.

## Borrow Interest Rates are Defined by Aave Governance

GHO borrows interest, and the Aave DAO sets discount rates. Aave Governance can periodically set the interest rates to help maintain stability with supply and demand.

### Other Assets

Interest rates are based on the utilization of a normal reserve within the Aave Protocol. For example, if 10% of the supplied assets are borrowed, there will be a low interest rate. If 90% of the supplied assets are borrowed, there will be a high interest rate.

With GHO, there are no suppliers, so interest rates work differently.

### GHO

The interest rate is stable and adapted periodically by Aave Governance depending on market conditions to help control price stability. If the price of GHO increases, the interest rate should decrease to encourage the creation of GHO (i.e., GHO supply expands -> GHO rebalances down). If the GHO price decreases, the interest rate should increase to incentivize repayment (i.e., GHO supply contracts -> GHO prices rebalance up).

For more information, please see the [Interest and Discount Rates](interest-rate-discount-model.md) page.

## Repaid Interest is Re-directed to the Aave DAO Rather Than to Suppliers

### Other Assets

Normally, most of the interest earned on borrowed crypto assets is directed to the users that supplied the corresponding asset, and a small amount of this is directed to the Aave DAO.

### GHO

If GHO is not supplied, there are no suppliers to pay, so GHO does not have a reserve. All the interest accrued on positions will be paid to the Aave DAO.

## Facilitators

A [Facilitator](./gho-facilitators.md) can trustlessly mint and burn GHO tokens through various strategies. Different entities can implement these strategies and may employ varying strategies to integrate GHO (each entity is a facilitator). The Aave DAO assigns each Facilitator a Bucket with a specified Capacity, the upward limit of GHO that a specific Facilitator can mint.

## Minting

Similarly to the borrowing of other assets on Aave, a user must supply collateral (at a specific collateral ratio) to be able to mint (borrow) GHO. As GHO is minted on demand, the user does not have to rely on supplied assets - GHO does not need to be supplied.

## Burning

When a user repays a borrow position (or is liquidated) where GHO is the asset being borrowed, GHO tokens are returned to the Aave pool and burned. All the interest payments accrued by minters of GHO go directly to the Aave DAO treasury (in contrast to the standard reserve factor collected when users borrow other assets). Collateral is freed up and can be used to open a new borrow position or withdraw.

## Borrow cap

The total amount of GHO that can be minted is limited by a borrow cap that can be and is regularly adjusted by Aave's Governance. Borrow cap and other GHO metrics can be monitored in TokenLogic [GHO analytics dashboard](https://aave.tokenlogic.xyz/gho).

## Isolation Mode

[Isolation mode](https://docs.aave.com/developers/whats-new/isolation-mode) on V3 Aave Governance can limit exposure to the amount of GHO that can be minted based on collateral from riskier assets. If the community determines that a specific asset weight in GHO collateral is 'too high,' limits can be changed by a governance vote as Aave Governance sees fit. In this example, isolation mode reduces risk and keeps GHO collateralized.

## Bridges

Bridging support and logic will be dependent upon bridges that will support GHO.
