---
description: Helpful concepts and general terms to understand Jet's Margin application.
---

# Margin Accounting Concepts

#### See also: Product documentation page describing Jet's margin account design:

{% content-ref url="../../protocol/jet-products/margin-accounts-and-collateralization-accounting.md" %}
[margin-accounts-and-collateralization-accounting.md](../../protocol/jet-products/margin-accounts-and-collateralization-accounting.md)
{% endcontent-ref %}



#### _General Margin Accounting Terms_

**Account:** A margin account. Users may use multiple isolated margin accounts controlled by one wallet pubkey.

**Assets:** The USD value of tokens and positions that you own in your margin account.

**Liabilities:** The USD value of tokens and positions that you owe in your margin account.

**Equity:** The difference between assets and liabilities.

**Claim(s):** A synonym for debts/liabilities.

**Account Leverage:** The ratio of assets to equity in your account.

**Exposure:** The sum of claim values on an account.

**Collateral Weight:** A multiplier that adjusts the contribution of an asset's value to account collateral.

**Required Collateral Factor:** A constant assigned to each asset that is used to determine the required collateral for a liability of that asset. Analogous to the maximum leverage for a particular asset. For further information, see the 'Margin accounts' page in the Gitbook documentation.

**Effective Collateral:** The total value of available collateral available minus the value of all debt positions.

**Required Collateral:** The USD value that a margin account is required to maintain in order to avoid liquidations.

**Required Setup Collateral:** The USD value that a margin account is required to maintain to open a new position.

**Available Setup Collateral:** The effective collateral less the required setup collateral for existing exposure positions.

**Available Collateral:** The difference between your effective collateral and required collateral, quoted in USD. This represents the collateral available for setting up new positions, or your buffer against liquidation. When available collateral reaches zero, your margin account is subject to liquidation.

**Effective Collateral:** The total collateral less the total value of debt positions.

**Risk Level:** The ratio of liabilities and required collateral to the (weight-adjusted) collateral in your account.

**Liquidation:** The process of selling some of a borrower’s collateral to a third party, called a liquidator. The liquidator pays for the collateral using the token in which the debt is denominated, thereby (partially) repaying the borrower’s debt. The sale price is determined by an oracle, and is intended to be a fair market price. If the risk level of a margin account goes above 1.0, it will be available to be liquidated and a 3% fee will charged. [See more details on the liquidation page.](https://docs.jetprotocol.io/jet-protocol/protocol/liquidation)
