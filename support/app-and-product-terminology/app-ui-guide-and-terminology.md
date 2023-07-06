---
description: >-
  This page serves as a glossary for all terms used across Jet Protocol UI
  applications, grouped by the application in which they appear and the part of
  the app.
---

# App UI Guide and Terminology

### General Terms Shared Between Applications:

The account snapshot section of the UI is marked below. This snapshot remains on-screen regardless of which part of the application you are in.

Below, the various terms in the **account snapshot** are defined. These definitions are also available within the application by hovering above a term with the mouse.

**Note** that values shown throughout the application UI are approximated and rounded from the actual values, which can be viewed in a block explorer and typically have many decimals.

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

_**Account Snapshot Terms:**_

**Account Balance:** The value of your equity in this margin account, assets minus liabilities.

**Assets:** The USD value of tokens and positions that you own in your margin account.

**Liabilities:** The USD value of tokens and positions that you owe in your margin account.

**Available Collateral:** The difference between your effective collateral and required collateral, quoted in USD. This represents the collateral available for setting up new positions, or your buffer against liquidation. When available collateral reaches zero, your margin account is subject to liquidation.

**Effective Collateral:** The total collateral less the total value of debt positions.

**Required Collateral:** The USD value that a margin account is required to maintain in order to avoid liquidations.

**Account Leverage:** The ratio of assets to equity in your account.

**Risk Level:** The ratio of liabilities and required collateral to the (weight-adjusted) collateral in your account.



_**Margin Account Creation Terms:**_

Additionally, included are terms used in the hovering modal when first creating a margin account:

![](<../../.gitbook/assets/image (13).png>)

**Rent Fee:** When you open your account on Jet, rent is charged by the Solana blockchain for the storage of that data. The rent fee can be fully refunded in the future when you close all your account obligations on Jet. This is true for all protocols which allocate space per user on-chain.



**Lookup Table:** An on-chain account that stores commonly used addresses to enable transactions with a large number of instructions.

A lookup table is implemented in order to provide users the best experience when using the Jet suite of applications. Users will be prompted to set up their lookup table when they create their margin account:

![](<../../.gitbook/assets/image (10).png>)

### Pools Application:

Below, the UI of the fixed rate has elements of the application marked and labeled, followed by definitions for the terms in those areas of the app.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

**Pools Terms:**

#### _Asset Panel Terms_

**Token:** The type of token that can be lent or borrowed.&#x20;

**Utilization Rate:** The fraction of a pool’s assets that have been borrowed, which determines the deposit and borrow rates. See [the margin pool interest rates page](../../protocol/jet-products/pooled-variable-lending-interest-rates-design.md) for more details.

**Total Borrowed:** The total amount of tokens currently borrowed from the pool.

**Available Liquidity:** The total amount of tokens currently in the pool.

**Deposit Rate:** The current annualized deposit rate for each token.

**Borrow Rate:** The current annualized borrow rate for each token.

#### _Pool Detail Terms_

**Current Price:** The current price of the token based on [that token's Pyth oracle that Jet uses.](https://docs.jetprotocol.io/jet-protocol/integrations/pyth-oracle)

**Collateral Weight:** The collateral weight of the token. See [the margin accounts accounting page](../../protocol/jet-products/margin-accounts-and-collateralization-accounting.md).

**Required Collateral Factor:** The required collateral factor of the token. See [the margin accounts accounting page](../../protocol/jet-products/margin-accounts-and-collateralization-accounting.md).

**Pool Size:** The total amount of tokens in the pool plus currently borrowed tokens.

**Utilization Rate:** The fraction of a pool’s assets that have been borrowed, which determines the deposit and borrow rates. See [the margin pool interest rates page](../../protocol/jet-products/pooled-variable-lending-interest-rates-design.md) for more details.

**Available Liquidity:** The total amount of tokens currently in the pool.

**Total Borrowed:** The total amount of tokens currently borrowed from the pool.

**Pool Address:** The pubkey of the pool.

**Token Address:** The token address of the token.

### Fixed Rate Application:

Below, the UI of the fixed rate has the various elements of the application marked and labeled, followed by definitions for the terms in those areas of the app.

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (6) (3).png" alt=""><figcaption></figcaption></figure>

**Fixed Rate Terms:**

#### _Order Panel_

**Repayment Date:** The date and time that a loan is due.

**Posted Repayment Amount:** The total amount of a loan necessary to be repaid including interest and fees. Posted indicates that this part of the order will be posted to the orderbook.

**Posted Interest:** The total amount of interest on the loan necessary to be paid.Posted indicates that this part of the order will be posted to the orderbook.

**Posted Rate:** The rate chosen by the lender or borrower at which their capital may be lent or borrowed. Posted indicates that this part of the order will be posted to the orderbook.

**Matched Repayment Amount:** The total amount of a loan necessary to be repaid including interest and fees. Matched indicates that this part of the order will be immediately matched with a preexisting order on the orderbook.

**Matched Interest:** The total amount of interest on the loan necessary to be paid. Matched indicates that this part of the order will be immediately matched with a preexisting order on the orderbook.

**Matched Effective Rate:** The average rate of the loans or borrows comprising the order, if it is executed. Matched indicates that this part of the order will be immediately matched with a preexisting order on the orderbook.

**Risk Indicator:** The ratio of liabilities and required collateral to the (weight-adjusted) collateral in your account.

#### _Open Orders and Positions Table_

**Loan Offers:** Currently open (limit) loan offer orders including partial fills.

**Open Lends:** Filled and current loans.

**Borrow Requests:** Currently open (limit) borrow request orders including partial fills.

**Open Borrows:** Filled and current borrows.

#### _Pool Balances Table_

The balances table allows users a quick glance at the tokens they have deposited or borrowed in their margin accounts, the USD value of those assets, and the current variable pooled lending deposit and borrow rates.

#### _Misc_

Liquidation: The process of selling some of a borrower’s collateral to a third party, called a liquidator. The liquidator pays for the collateral using the token in which the debt is denominated, thereby (partially) repaying the borrower’s debt. The sale price is determined by an oracle, and is intended to be a fair market price. If the risk level of a margin account goes above 1.0, it will be available to be liquidated and a 3% fee will charged. [See more details on the liquidation page.](https://docs.jetprotocol.io/jet-protocol/protocol/liquidation)

