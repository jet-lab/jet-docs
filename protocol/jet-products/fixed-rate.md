# Fixed Rate

**See also: Fixed Rate Concepts and Terms**

{% content-ref url="../../support/app-and-product-terminology/fixed-rate-concepts.md" %}
[fixed-rate-concepts.md](../../support/app-and-product-terminology/fixed-rate-concepts.md)
{% endcontent-ref %}

### In Search Of Term Structure - The Fix&#x20;

Jet's Fixed Term application allows users to lend and borrow assets with a fixed agreement in terms of interest rate and duration of a loan/borrow.&#x20;

With the innovation of a CLOB to negotiate rates, users are empowered to post maker orders for lends or borrows at the rates they would like to lend out or borrow, or, alternatively they may post taker orders. This familar structure for debt as used in traditional markets has advantages that the "pooled lending" model currently employed by DeFi lending applications.

### Jet Protocol’s Solution&#x20;

Jet's Fixed Term application addresses the shortcomings of lending pools and current fixed debt market models would include at least:

* Secured loans with defined terms,
* A facility for lenders and borrowers to negotiate rates, and
* A liquidation channel to enforce repayment of overdue loans.

### Mechanics

Prospective fixed rate users must [create a margin account](https://docs.jetprotocol.io/jet-protocol/support/get-started/using-jet-protocol) on Jet Protocol in order to participate. The margin account is responsible for ensuring that no transactions are allowed that would violate the constraints by which the protocol defines risk.

Fixed rate lenders and borrowers are presented with a choice of markets for different token and loan term pairs, for example 1-day SOL or 30-day USDC. Within each market lenders and borrowers go about their business as **makers** or **takers** of liquidity:

* **Lenders who offer loans at particular rates act as makers.** Those loan offers sit in the orderbook until borrowers looking to borrow immediately come along as takers, and take up some of the loans on offer.
* **Borrowers can also act as makers by requesting loans at particular rates.** These requests sit in the orderbook until lenders come along looking to lend immediately by filling some of the requested loans.

Offers and requests behave just like bids and asks on a standard orderbook. They are processed in rate and time-in-book order – borrower maker orders take the lowest rates available, and lender taker orders take the highest rates available (orders with equal rates will be processed in the order that they were placed in the orderbook). As orders are partially filled the remaining size decreases and, when completely filled, they are removed from the book. They can be cancelled at any time.

Fixed rate loans are fully secured. All lender and borrower actions are subject to [margin account health checks](https://docs.jetprotocol.io/jet-protocol/protocol/jet-products/margin-accounts-accounting) and transactions are aborted that would reduce the equity of a user's margin account below the required minimum.

When a loan request or offer is filled, a number of things happen atomically:

* A **term deposit** is created in the lender's margin account that records the number of tokens lent, the number of tokens to be repaid to the lender, and the **maturity date** on which the latter tokens may be claimed.
* A **term loan** is created in the borrower's margin account that records the number of tokens borrowed, the number of tokens to be repaid by the borrower, and the **maturity date** by which these loans must be repaid.
* The borrowed tokens are **delivered** to the borrower, subject to an **origination fee** applied to the new debt. Whether borrowing immediately or requesting a loan, the origination fee is added to the principal amount. Each filled amount is then regarded as a pro-rata portion of the principal and associated origination fee. The principal part is delivered to the borrower, and the fee part is retained by the protocol.

The timely **repayment** of term loans is enforced by the margin program and **liquidator**. Term loans with maturity dates in the past are subject to liquidation regardless of the health of the associated margin account. If appropriate tokens are available in the account to repay the loan directly, the liquidator repays on the user's behalf with no fee. Otherwise, the liquidator applies a fee and sells collateral from the account to cover the debt.

Prior to maturity, term loans are treated as liabilities of their margin account in the normal way, and the usual account [health and liquidation rules apply.](https://docs.jetprotocol.io/jet-protocol/protocol/jet-products/margin-accounts-accounting) Term deposits are also treated like other collateral assets in that a weight applied to their USD value determines their contribution to an account’s collateral balance. For an initial period after launch this weight will be zero and term deposits will not contribute to collateral at all. As the fixed rate markets mature and the capacity to liquidate term deposits increases, their collateral weight will be increased appropriately through protocol governance.

\
To support long-term lenders and borrowers the fixed rate program provides a facility to have term loans and deposits **rolled over automatically**. If activated, matured term deposits are redeemed and the funds used to place new loans offers at a configurable minimum rate. Matured term loans are repaid by automatically borrowing the amount due at a configurable maximum rate, subject to account health checks.



**Fees**

* An **origination fee** of 50 basis points annualized is added to the amount borrowed.
* In the event of borrower liquidation, the liquidator will attempt to pay back the borrowed funds with funds of the same token type in the borrower's margin account. If the assets are available to pay down the debt at this time, the liquidator will NOT charge any fees to the user for this convenience. [See the Liquidation page for more details](../liquidation.md).



**Autoroll**

The optional "autoroll" feature allows lenders to loan out their cash over multiple terms totally hands-off without needing any intervention. Similarly, borrowers may elect to continuously borrow across terms. If a borrower account lacks the required collateral at any point during a term, it will be subject to liquidation as normal.



**Term Deposits Contribution Towards Available Collateral:**

Terms deposits are treated like other collateral assets in that a weight applied to their USD value determines their contribution to your collateral balance.&#x20;

For an initial period after launch this weight will be zero - term deposits will not contribute to collateral at all. As the fixed rate markets mature and the capacity to liquidate term deposits increases, their collateral weight will be increased appropriately through protocol governance.

