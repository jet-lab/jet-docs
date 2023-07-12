---
description: How to interact with the borrowing side of Jet Fixed Term
---

# How To: Borrow Now

**Navigate to the "Borrow Now" Section of the Application**

To begin, enter the fixed term application on the borrowing side by clicking "**Fixed Borrow**" on the menu bar on top of the application. Then select the "**Borrow Now**" function in the order panel.&#x20;

**Examine the Current State of the Orderbook**

For testing purposes, the 2 minute market tenor is the easiest to use. You can select it in the drop down box just above the order panel.

Imagine you want to borrow 120,500 USDC as soon as possible, at any rate available. Begin by navigating to the "**Borrow Now**" tab, where you will see a chart similar to the following:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-05 a la(s) 17.02.46.png" alt=""><figcaption></figcaption></figure>

As a borrower, you want to borrow at the lowest rates you can get. The leftmost part of the colored blue shadow with the lowest rates on the book is the "top of the orderbook" from the perspective of a borrower. A "**borrow now**" order will always take the cheap loan offers on the top of the orderbook first.

Now, hover over the chart at a value of 120,500 USDC on the y-axis. When you borrow that much USDC, you will fulfill a variety of lend offers requests at various rates. The average interest rate for your borrow would be 4,84%:

<figure><img src="../../../.gitbook/assets/borrow 120k.png" alt=""><figcaption></figcaption></figure>

**Borrow Now Order Setup**

Type in 120,500 in the "**Borrow Now"** order panel. You will see some corresponding information about the borrow before submitting the transaction, including:

* The **repayment date**, which the borrower will need to repay by else the liquidator may repay the debt using their collateral (this assumes that autoroll is not on).
* The **total repayment amount** equal to the principle plus interest.
* The **total interest,** rounded down to two decimal places (understandably low since this is a 2 minute loan).
* The **interest rate** of the loan (which may differ slightly from what was seen in the chart above because of rounding on the chart; this is the exact figure rounded to 3 decimal places).
*   The margin account's projected **risk indicator** after the transaction completes and the 120,500 USDC is borrowed.

    <figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-05 a la(s) 17.11.27.png" alt="" width="375"><figcaption></figcaption></figure>

The "**autoroll**" option allows a borrower to renew the loan indefinitely as long as their account remains sufficiently collateralized.&#x20;

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-06 a la(s) 12.34.40.png" alt="" width="375"><figcaption></figcaption></figure>

**After Placing the Order**

Once satisfied with the order setup, go on to approve the transaction. You can see your borrow in the "**Open Borrows**" table just below the chart, along with the time of creation, time of maturity, total balance, and rate:&#x20;

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-05 a la(s) 17.12.16.png" alt=""><figcaption></figcaption></figure>

You can also observe the chart afterwards to see the effect that borrowing 120,500 USDC had on the orderbook. 120,500 USDC has been removed from the y-axis, and the "**Borrow Now**" transaction borrowed from the lowest rates on top of the orderbook / the colored blue shadow; leaving the lower-rate loan offers to the left of the offers on top of the orderbook (Which are now lower in the books and closer to being borrowed if another borrower come along with a "**Borrow now**" order ) Before our "**Borrow Now**" order, the lower-rate offer was 4.5% and now the rates is 5%.

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-05 a la(s) 17.14.15.png" alt=""><figcaption></figcaption></figure>

After the borrow order is complete, the loan offers still on the book are now offering around 250,000 USDC starting at a rate of 5% as indicated by the colored blue shadow, with additional offers at higher rates as indicated by the chart.&#x20;

**Repaying the Loan**

Once you borrow, a repayment option appears above the chart, as shown in the screenshot below. You may pay the balance due at any point after the borrow. If you do not repay by the time that the loan has matured, your collateral will be liquidated to repay the loan.

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-06 a la(s) 12.25.19.png" alt=""><figcaption></figcaption></figure>

When repaying the loan, you may click on the underlined value that is needed for repayment in order to easily load it into the input box. Then just click the "**repay now**" button and approve the transaction.

That's a borrow now order! Try placing orders for different amounts when the orderbook has different loan offers available. You can even change the state of the lend offers on the market yourself by creating loan offers from a different margin account.

If you find bugs, have UX/UI suggestions, general questions, etc, please visit the forum at [https://forum.jetprotocol.io/](https://forum.jetprotocol.io/)
