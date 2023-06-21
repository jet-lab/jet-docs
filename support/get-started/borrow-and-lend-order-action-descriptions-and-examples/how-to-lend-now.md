---
description: How to interact with the lending side of Jet Fixed Term
---

# How To: Lend Now

**Navigate to the "Lend Now" Section of the Application**

To begin, enter the fixed term application on the lending side by clicking "Fixed Lend" on the menu bar on top of the application. Then select the "Lend Now" function in the order panel.&#x20;

<figure><img src="../../../../.gitbook/assets/image (4) (3).png" alt=""><figcaption></figcaption></figure>

**Examine the Current State of the Orderbook**

For testing purposes, the 2 minute market tenor is the easiest to use. You can select it in the drop down box just above the order panel.&#x20;

Imagine you want to lend out 72,000 USDC as soon as possible, at any rate you can get. Begin by navigating to the "Lend Now" tab, where you will see this chart:

<figure><img src="../../../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

As a lender, you want to fulfill the borrow requests with the highest rates you can get. The leftmost part of the chart with the highest rates on the book is the "top of the orderbook" from the perspective of a lender. A "lend now" order will always take the loan offers on the top of the orderbook first.

Now, hover over the chart at a value of 72,000 cumulative USDC requests on the x-axis. When you lend out that much USDC, you will fulfill a variety of borrow requests at various rates. The average interest rate for your lend across all the fulfilled borrow orders for a borrow of this size this would be 1.06%:

<figure><img src="../../../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

**Lend Now Order Setup**

Type in 72,000 in the "Lend Now" order panel. You will see some corresponding information about the borrow before submitting the transaction, including:

* The **repayment date**, which the borrower will need to repay by else the liquidator may repay the debt using their collateral (this assumes that autoroll is not on; note that autoroll is disabled for the initial application release).
* The **total repayment amount** equal to the principle plus interest.
* The **total interest,** rounded down to two decimal places (understandably low since this is a 2 minute loan).
* The **interest rate** of the loan (which may differ slightly from what was seen in the chart above because of rounding on the chart; this is the exact figure rounded to 3 decimal places).
* The margin account's projected **risk indicator** after the transaction completes and the 125,000 USDC is borrowed.

<figure><img src="../../../../.gitbook/assets/image (5) (3).png" alt=""><figcaption></figcaption></figure>

**After Placing the Order**

Once satisfied with the order setup, go on to approve the transaction. You can see our active lend in the "Open Deposits" table just below the chart, along with the time of creation, time of maturity,  total balance, and rate:&#x20;

<figure><img src="../../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

You can also observe the chart afterwards to see the effect that lending the 72,000 USDC out to borrow requesters had on the orderbook. 72,000 USDC has been removed from the x-axis. The "lend now" transaction lent to the highest rates on top of the orderbook / the left of the chart; leaving the lower-rate borrow requests to the right of the order in the deeper part of the orderbook (which is now higher in the books if another lender came along with a "lend now" order).

After the lend order is complete, the borrow requests still on the book are now requesting a rate of 0.1% as indicated by a horizontal line, and there are around 8,000 cumulative USDC requests remaining at that rate.

<figure><img src="../../../../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

**After the Loan is Repaid**

After the borrower has repaid (or the loan has matured, and the liquidator liquidated their collateral for the amount of USDC due), a claim option appears above the chart, highlighted in the screenshot below. Simply click the claim button and approve the transaction, and the loan principle plus interest will deposited in your margin account after account settlement (see next step).

In the future, an "autoroll" option will be available, allowing a the loan to be renewed by a lender indefinitely as long as there is demand for all or part of that loan.

<figure><img src="../../../../.gitbook/assets/image (12) (2).png" alt=""><figcaption></figcaption></figure>

**Account Settlement**

After lending, your account must be settled before the lent tokens and interest will be deposited into your margin account. There are no fees for doing so, aside from the (very low) SOL cost to approve the settlement transaction.&#x20;

When your account needs to be settled, a prompt will appear above the chart in the same location as the claim button. Click the button and approve the transaction.

<figure><img src="../../../../.gitbook/assets/image (6) (2).png" alt=""><figcaption></figcaption></figure>

That's an lend now order! Try placing orders for different amounts when the orderbook has different loan offers available. You can even change the state of the borrow requests on the market yourself by creating borrow request orders from a different margin account.

If you find bugs, have UX/UI suggestions, general questions, etc, please visit the forum at [https://forum.jetprotocol.io/](https://forum.jetprotocol.io/)
