---
description: >-
  Don't follow this example exactly - rather, use it as a starting guide. Get
  creative, try different combinations of actions and amounts; interact with
  your orders from separate margin accounts, etc.
---

# How To: Borrow Now

**Navigate to the "Borrow Now" Section of the Application**

To begin, enter the fixed term application on the lending side by clicking "Fixed Borrow" on the menu bar on top of the application. Then select the "Borrow Now" function in the order panel.&#x20;

<figure><img src="../../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

**Examine the Current State of the Orderbook**

For testing purposes, the 2 minute market tenor is the easiest to use. You can select it in the drop down box just above the order panel.

Imagine you want to borrow 125,000 USDC as soon as possible, at any rate available. Begin by navigating to the "Borrow Now" tab, where you will see this chart:

<figure><img src="../../../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

Now, hover over the chart at a value of 125,000 cumulative USDC requests on the x-axis and you will see that the overall average interest for a borrow of this size this should be around 1.43%. A "borrow now" order will always take the loans offers on the book with the lowest rate first. The leftmost part of the chart with the lower rates is the "top of the orderbook."

<figure><img src="../../../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

**Borrow Setup**

Type in 125,000 in the "Borrow Now" order panel. You will see some corresponding information about our borrow before submitting the transaction, including:

* The **repayment date**, which the borrower will need to repay by else the liquidator may repay the debt using their collateral (this assumes that autoroll is not on; note that autoroll is disabled for the initial application release).
* The **total repayment amount** equal to the principle plus interest.
* The **total interest,** rounded down to two decimal places (understandably low since this is a 2 minute loan).
* The **interest rate** of the loan (which may differ slightly from what was seen in the chart above because of rounding on the chart; this is the exact figure rounded to 3 decimal places).
* The margin account's projected **risk indicator** after the transaction completes and the 125,000 USDC is borrowed.

<figure><img src="../../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

**After Placing the Order**

Once satisfied with the order setup, go on to approve the transaction. You can see our borrow in the "Open Borrows" table just below the chart, along with the time of creation, the time of maturity, the total balance, and the rate:&#x20;

<figure><img src="../../../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

You can also observe the chart to see the effect that taking the 125,000 loan had on the orderbook. 125,000 USDC has been removed from the x-axis, and the "borrow now" transaction borrowed from the leftmost, cheapest, top of the orderbook; leaving the loan offers to the right of the order; the deeper part of the orderbook.&#x20;

After the borrow is complete, the cheapest loan offers on the book are now offering a rate of 2.5% and there appears to be approximately 350,000 USDC worth of liquidity offered at that rate, as observed on the horizontal section of the line up to the inflection point at 350k on the x-axis:

<figure><img src="../../../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

**Repaying the Loan**

Once you borrow, a repayment option appears above the chart, highlighted in the screenshot below. You may pay the balance due at any point after the borrow. If you do not repay by the time that the loan has matured, your collateral will be liquidated to repay the loan as close to the maturity date as possible.&#x20;

In the future, an "autoroll" option will be available, allowing a borrower to renew the loan indefinitely as long as their account remains sufficiently collateralized.&#x20;

When repaying the loan, you may click on the underlined value that is needed for repayment in order to easily load it into the input box. Then just click the "repay now" button and approve the transaction.

<figure><img src="../../../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

That's an borrow now order! Try placing orders for different amounts when the orderbook has different loan offers available. You can even change the state of the lend offers on the market yourself by creating loan offers from a different margin account.

If you find bugs, have UX/UI suggestions, general questions, etc, please visit the forum at [https://forum.jetprotocol.io/](https://forum.jetprotocol.io/)
