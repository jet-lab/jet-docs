# Fees

The protocol does not currently charge any fees. Subject to change.

### User's Costs When Using Jet Protocol:

**Solana Rent Fee**

When you open your account on Jet, rent is charged by Solana which can be fully refunded in the future when you close all your account obligations on Jet. This is true for all protocols which allocate space per user on-chain.

**Solana Transaction Fees**

Currently there is no extra Jet originated fee added to your transactions. Only the minimal transaction fees on the Solana network are required to handle your transactions on Jet.. The Solana transaction fees are debited from your wallet when your transaction is processed.

**Liquidation Fees**

When your C-ratio drops below the 125% threshold, a portion of the collateral position is liquidated to return your C-ratio to at least 125%. A 3% liquidation fee is applied to the portion of your collateral that was liquidated.

If you have more than one collateral type in your deposit, the current version of liquidator picks a random collateral type to partially liquidate to bring your c-ratio to healthy status.

**Interest Accrual**

For collateral and loan accounts, interest accrues and gets continuously compounded to your respective accounts.

\
