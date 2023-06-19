---
description: >-
  Helpful concepts and general terms to understand Jet's Leverage Swaps
  application.
---

# Leverage Swaps Concepts

_**Note** that both slippage and price impact are a result of how AMMs like Orca or Saber; both Orca and Saber are outside protocols that Jet does not control. When using Leverage Swaps, the assets are swapped on venues outside of Jet. Jet provides the collateral management and potential leverage for the trade, but the trades themselves are executed on an outside protocol._&#x20;

#### _General Leverage Swaps Terms_

**Slippage:** The user's chosen tolerance for slippage in included price quoted. If the price moves outside of the slippage range before the transaction is completed, the transaction will fail and no trade will take place. The default slippage for Jet leveraged swaps is 0.1%.

**Token Balances:** The token balances before and after the swap executes.&#x20;

**Risk Level:** The account risk level before and after the swap executes.&#x20;

**Price Impact:** The percentage of capital lost when placing a trade due to the liquidity of the tokens in the LP position pair being swapped. The lower liquidity in the AMM pool, the higher the price impact.&#x20;
