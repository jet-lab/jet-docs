# 🛫 Fees

At some point after the JetGovern application is released, protocol feeds will be turned on. These fees may become become a source of revenue for the DAO in the future, to directly bolster the staking returns and long-term benefit of those JET holders staked and participating in governance.

Note that these parameters are not static, and can be changed via governance as the protocol’s performance and health is evaluated on a rolling basis. The initial fees, once turned on, will be as follows:

* 20% of interest earned by depositors will be earmarked specifically for the Jet DAO treasury
* No origination fees on borrowers.

Initially, these fees will accumulate in the Jet Protocol treasury. In upcoming releases the protocol will disburse revenue directly to ecosystem stakeholders and participants. This budget will be controlled via governance, and the initial perpetual reward program will likely see protocol revenue distributed as follows:

* 10% used for Jet buybacks. These JET tokens will be returned to the DAO treasury and can be administered by DAO governance.
* 10% returned to the treasury in the same asset it was collected in.
* 40% distributed to JET stakers.
* 40% distributed to borrowers.

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
