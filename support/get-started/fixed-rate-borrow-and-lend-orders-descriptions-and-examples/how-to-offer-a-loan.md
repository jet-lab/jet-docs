---
description: How to interact with the lending side of Jet Fixed Term
---

# How To: Offer a Loan

**Navigate to the "Offer Loan" Section of the Application**

To begin, enter the fixed term application on the lending side by clicking **"Fixed Lend"** on the menu bar on top of the application. Then select the **"Offer Loan"** function in the order panel:

<figure><img src="../../../.gitbook/assets/Offer Loan - Fixed Lend.png" alt=""><figcaption></figcaption></figure>

**Examine the Current State of the Orderbook**

For testing purposes, the 2 minute market tenor is the easiest to use. You can select it in the drop down box just above the order panel.

Now, you can examine the chart to see the current loan offers on the market. Note that the chart will be different when you look at it because the market is real time and ever-changing with market activity.

The colored blue shadow represent how much USDC liquidity is available at each rate. The "top" of the orderbook from the perspective of a lender[^1] is where the x-axis marks 5%, where the rates are cheapest, and these loans will be taken first by a borrower. The rates displayed as you move right on the chart is the average rate for all of the liquidity from the top of the books up to that point.

By hovering over the rightmost end of the chart, you will see on the x-axis that value of cumulative USDC offers is around 169,800 USDC, at a rate of 6.17%. This means that if someone was to come borrow 169,800 USDC right now at whatever rate is available, they would borrow the entire amount at a total average interest rate of 6.17%.

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-04 a la(s) 15.21.36.png" alt=""><figcaption></figcaption></figure>

If you take a closer look where the blue-shadow begins, on the middle of the chart, you will see the current cheapest loan offers on the market. From this image here you can see that the lowest loan offer on the book has a rate of 4,98%.

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-04 a la(s) 15.21.21.png" alt=""><figcaption></figcaption></figure>

**Offer Loan Order Setup**

In this use case, imagine you want to undercut the current lowest lender so that our loan will be taken first by borrowers (though at a lower rate). If you had 35,000 USDC, you could lend it with a rate of 4.3%.

Enter these parameters into the order panel to the left of the chart:

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-04 a la(s) 15.21.11.png" alt="" width="375"><figcaption></figcaption></figure>

Note the information relayed in the green outlined box, which includes:

* The **repayment date,** which the borrower will need to repay by else the liquidator may repay the debt using their collateral.
* The **posted repayment amount** equal to the principle plus interest.
* The **posted interest** (rounded down to 0.00 USDC to maintain two decimals, when in actuality there is a small amount of interest required that just isn't shown because the 2 minute tenor is such a short interval; this tenor is specifically made for easier testing).
* The **matched repayment amount** - If there were any existing borrow request orders on the book that would match with our lend parameters, the amount would be displayed here (and would be subtracted from the "posted payment amount").
* The **matched interest** - The interest on any orders that will match immediately after approving this transaction.
* The current and projected **risk indicator** - The projected risk level after the transaction completes.

The "**autoroll**" option allows a borrower to renew the loan indefinitely as long as their account remains sufficiently collateralized.

<figure><img src="../../../.gitbook/assets/image (2) (2).png" alt="" width="375"><figcaption></figcaption></figure>

**After Placing the Order**

Once satisfied with the order setup, you can go on to approve the transaction. You will see the loan offer displayed in the "**Loan Offers**" table just below the chart. Note that you can also **cancel** the order here, and that if part of the order already matched with an existing borrow request on the book, then some of the "**Total qty**" would be in the "**Filled qty**" column. Additionally, the matched part would be found in the "**Open Lends**" tab.

<figure><img src="../../../.gitbook/assets/Loan Offer 35.png" alt=""><figcaption></figcaption></figure>

You can also see the effect that our loan offer has on the chart. On the left side of the shaded blue area, a segment has been added, precisely between our new Loan Offer at 4.3% and the previous cheapest rate at 5%. You can hover over the line to examine the values:

<figure><img src="../../../.gitbook/assets/Chart after new loan offer.png" alt=""><figcaption></figcaption></figure>

Finally, you can observe the effect of the order on the bottom of the orderbook by hovering over the rightmost part of the chart. When you do so, you will see that when compared to the first chart before the order, an additional 35,000 USDC has been added, and that if an entity was to come and borrow the entire 169,800 USDC on the books, their effective rate would by 5,46% instead of 6,17% as it was before the last order was placed. This is because the offer of 35,000 USDC at 4,3% drove down the average rate.

<figure><img src="../../../.gitbook/assets/New offer chart effect.png" alt=""><figcaption></figcaption></figure>

**After the Loan is Repaid**

After the borrower has repaid (or the loan has matured, and the liquidator liquidated their collateral for the amount of USDC due), a **Claim** option appears above the chart, as shown in the screenshot below. Simply click the **Claim** button and approve the transaction, and the loan principle plus interest will be deposited in your margin account after account settlement (see next step).

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-04 a la(s) 16.52.07.png" alt=""><figcaption></figcaption></figure>

**Account Settlement**

After claiming back your tokens, you should **Settle** your account in order to visualize your tokens plus interest in your margin account. There are **no fees charged by Jet** for doing so, aside from the $0.00025 per transaction for using Solana Blockchain.

When your account needs to be **Settled**, a prompt will appear above the chart in the same location as the **Claim** button. Click the button and approve the transaction.

<figure><img src="../../../.gitbook/assets/Captura de pantalla 2023-07-04 a la(s) 16.42.42.png" alt=""><figcaption></figcaption></figure>

That's an Offer Loan order! Try out placing orders at different rates and amounts, and see what happens when you match part or all of your order with a borrow request that already exists on the books!&#x20;

If you find bugs, have UX/UI suggestions, general questions, etc, please visit the forum at [https://forum.jetprotocol.io/](https://forum.jetprotocol.io/)

[^1]: 
