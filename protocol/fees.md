# 🛫 Fees

As always, fee parameters are not static, and can be changed via governance as the protocol’s performance and health is evaluated on a rolling basis.&#x20;

### User's Costs When Using Jet Protocol:

**Solana Rent Fee**

When you open your account on Jet, rent is charged by Solana which can be fully refunded in the future when you close all your account obligations on Jet. This is true for all protocols which allocate space per user on-chain.

**Solana Transaction Fee**

Currently there is no extra Jet originated fee added to your transactions. Only the minimal transaction fees on the Solana network are required to handle your transactions on Jet. The Solana transaction fees are debited from your wallet when your transaction is processed.

**Liquidation Fee**

A 3% liquidation fee is applied to the portion of collateral that was liquidated. This occurs when your risk indicator (see [terminology page](https://docs.jetprotocol.io/jet-protocol/faq/terminology) for the definition on risk indicator or the [margin accounts page](https://docs.jetprotocol.io/jet-protocol/protocol/jet-products/margin-accounts-accounting) for further details) goes above 1.0, a portion of your collateral position is marked for liquidation, in order to return your risk indicator back to be below 1.0. If you have more than one collateral type in your deposit, the current version of liquidator picks a random collateral type to partially liquidate to bring your risk factor to healthy status.

**Interest Accrual Fee**

For collateral and loan accounts earning interest from pools, interest accrues and gets continuously compounded to your respective accounts. 20% of interest earned is redirected to the DAO.

\
