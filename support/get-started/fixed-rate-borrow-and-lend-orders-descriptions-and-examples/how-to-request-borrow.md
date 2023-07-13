---
description: How to interact with the borrowing side of Jet Fixed Term
---

# How To: Request Borrow

**Navigate to the "Borrow" Page of the Application UI**

To begin, enter the fixed term application on the borrowing side by clicking "**Fixed Borrow**" on the menu bar on top of the application. Then select "**Request Borrow**" in the order panel:

<figure><img src="../../../.gitbook/assets/Copia de Untitled (1) 2.png" alt=""><figcaption></figcaption></figure>

**Examine the Current State of the Orderbook**

For testing purposes, the 2 minute market tenor is the easiest to use. You can select it in the drop down box just above the order panel.

Now, you can examine the chart to see the current **borrow requests** on the market. Note that the chart will be different when you look at it because the market is real time and ever-changing with market activity.

The colored red shadow represents how much USDC are requested by borrowers and at which rate in the 2-minutes market. The "top" of the orderbook from the perspective of a borrower is on the righthand side, where borrowing rates are the most expensive. Lenders will prioritize filling the loans offered with the highest rate in order to achieve the highest returns accurately. As you move left on the chart, the displayed rate is the average rate for all of the liquidity from the top of the books up to that point.

If you take a closer look at the bottom of the orderbook on the rightmost side of the red shadow, you will see the most expensive borrow requests on the market. From this image here you can see that the highest rates are borrow requests with an average rate of 2%:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-05 a la(s) 14.27.54.png" alt="" width="563"><figcaption></figcaption></figure>

By hovering over the leftmost end of the chart, you will see on the y-axis that value of cumulative USDC is around 124,800 USDC, and a rate of 1.14%. This means that if someone was to come lend 124,800USDC right now, they would fill all of the borrow requests on the book at a total average interest rate of 1.14%.

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-05 a la(s) 14.32.10.png" alt="" width="563"><figcaption></figcaption></figure>

**Request Loan Order Setup**

In this use case, imagine you want to request a loan that will be at a cheaper rate, and don't mind waiting for it to fill. You want to borrow 5,000 USDC, and are willing to pay a rate of 0.5%.

Enter these parameters into the order panel to the left of the chart:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-05 a la(s) 16.36.11.png" alt="" width="375"><figcaption></figcaption></figure>

Note the information relayed in the green outlined box, which includes:

* The **repayment date,** which the borrower will need to repay by else the liquidator may repay the debt using their collateral (assuming autoroll is not on).
* The **posted repayment amount** equal to the principle plus interest.
* The **posted interest,** rounded down to 0.00 USDC to maintain two decimals, when in actuality there is a small amount of interest required that just isn't shown because the 2 minute tenor is such a short interval; this tenor is specifically made for easier testing.
* The **matched repayment amount** - If there were any existing lend offers on the book that would match with the borrow parameters, the amount would be displayed here (and would be subtracted from the "posted payment amount").
* The **matched interest** - The interest on any orders that will match immediately after approving this transaction.
* The current and projected **risk indicator** - The projected risk level after the transaction completes.&#x20;

The "**autoroll**" option allows a borrower to renew the loan indefinitely as long as their account remains sufficiently collateralized.

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

**After Placing the Order**

Once satisfied with the order setup, you can go on to approve the transaction. You will see the loan offer displayed in the **Borrow Requests** **table** just below the chart. This amount includes interest and fees. Note that you can also **cancel** the order here, and that if part of the order already matched with an existing lan request on the book, the matched part would be found in the **Open Borrows table**:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-05 a la(s) 16.46.25.png" alt=""><figcaption></figcaption></figure>

You can also see the effect that the borrow request has on the chart. If you hover over the leftmost part of the chart, it is apparent that 5,000 USDC (Previously 124k vs Now 129k) has been added to the books, and the average rate there has been driven down to 1.11%:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-05 a la(s) 16.49.30.png" alt="" width="563"><figcaption></figcaption></figure>

That's a **loan request** order! Try out placing orders at different rates and amounts, and see what happens when you match part or all of your order with a loan offer that already exists on the books!&#x20;

If you find bugs, have UX/UI suggestions, general questions, etc, please visit the forum at [https://forum.jetprotocol.io/](https://forum.jetprotocol.io/)
