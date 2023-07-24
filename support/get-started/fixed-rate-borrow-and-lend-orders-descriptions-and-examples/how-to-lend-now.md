---
description: How to interact with the lending side of Jet Fixed Term
---

# How To: Lend Now

**Navigate to the "Lend Now" Section of the Application**

To begin, enter the fixed term application on the lending side by clicking "**Fixed Lend**" on the menu bar on top of the application. Then select the "**Lend Now"** function in the order panel.

<figure><img src="../../../.gitbook/assets/Fixed Lend - Lend now.png" alt=""><figcaption></figcaption></figure>

**Examine the Current State of the Orderbook**

For testing purposes, the 2 minute market tenor is the easiest to use. You can select it in the drop down box just above the order panel.

Imagine you want to lend out 10,500 USDC as soon as possible, at any rate you can get. Begin by navigating to the "**Lend Now**" tab, where you will see a chart similar to the following:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-11 a la(s) 18.22.56.png" alt=""><figcaption></figcaption></figure>

As a lender, you want to fulfill the borrow requests with the highest rates you can get. The colored red shadow part of the chart with the highest rates on the book is the "top of the orderbook" from the perspective of a lender. A "**lend now**" order will always take the borrow requests on the top of the orderbook first.

Now, hover over the chart at a value of 10,500 USDC amount requests on the y-axis. When you lend out that much USDC, you will fulfill a variety of borrow requests at various rates. The average interest rate for your lend across all the fulfilled borrow orders for a borrow of this size this would be 3,38%:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-11 a la(s) 18.23.14.png" alt=""><figcaption></figcaption></figure>

**Lend Now Order Setup**

Type in 10,500 in the "**Lend Now"** order panel. You will see some corresponding information about the borrow before submitting the transaction, including:

![](<../../../.gitbook/assets/Captura de pantalla 2023-07-11 a la(s) 18.24.15.png>)

* The **repayment date**, which the borrower will need to repay by else the liquidator may repay the debt using their collateral (this assumes that autoroll is not on).
* The **total repayment amount** equal to the principle plus interest.
* The **total interest,** rounded down to two decimal places (understandably low since this is a 2-minute loan).
* The **interest rate** of the loan (which may differ slightly from what was seen in the chart above because of rounding on the chart; this is the exact figure rounded to 3 decimal places).
* The margin account's projected **risk indicator** after the transaction completes (Keep in mind that in this case it is 0 since it is an illustrative example. However, always remember to maintain your risk factor < 1, otherwise your account may face potential liquidation).

The "**autoroll**" option allows a borrower to renew the loan indefinitely as long as their account remains sufficiently collateralized.

<figure><img src="../../../.gitbook/assets/image (49).png" alt="" width="375"><figcaption></figcaption></figure>



**After Placing the Order**

Once satisfied with the order setup, go on to approve the transaction. You can see our active lend in the "**Open Lends**" table just below the chart, along with the time of creation, time of maturity,  interest, and rate:&#x20;

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-11 a la(s) 18.26.48.png" alt=""><figcaption></figcaption></figure>

You can also observe the chart afterwards to see the effect that lending the 10,500 USDC out to borrow requesters had on the orderbook. 10,500 USDC has been removed from the y-axis. The "**lend now**" transaction lent to the highest rates on top of the orderbook / the right side of the colored red shadow leaving the lower-rate borrow requests to the left of the order in the deeper part of the orderbook.

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-11 a la(s) 18.30.52.png" alt=""><figcaption></figcaption></figure>

After the lend order is complete, the borrow requests still on the book are now requesting a rate of 4% as indicated by a horizontal line, and there are around 55,000 cumulative USDC requests remaining at that rate.

**After the Loan is Repaid**

After the borrower has repaid (or the loan has matured, and![](<../../../.gitbook/assets/Captura de pantalla 2023-07-11 a la(s) 19.33.44.png>) the liquidator liquidated their collateral for the amount of USDC due), a **claim** option appears above the chart, highlighted in the screenshot below. Simply click the **claim** button and approve the transaction, and the loan principle plus interest will deposited in your margin account after account settlement (see next step).

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-11 a la(s) 18.43.02.png" alt=""><figcaption></figcaption></figure>

The "autoroll" option is available, allowing the loan to be renewed by a lender indefinitely as long as there is demand for all or part of that loan.

**Account Settlement**

After lending, your account must be settled before the lent tokens and interest will be deposited into your margin account. There are no fees for doing so, aside from the (very low) SOL cost to approve the settlement transaction.

When your account needs to be settled, a prompt will appear above the chart in the same location as the claim button. Click the button and approve the transaction.



That's an **lend now** order! Try placing orders for different amounts when the orderbook has different loan offers available. You can even change the state of the borrow requests on the market yourself by creating borrow request orders from a different margin account.

If you find bugs, have UX/UI suggestions, general questions, etc, please visit the forum at [https://forum.jetprotocol.io/](https://forum.jetprotocol.io/)
