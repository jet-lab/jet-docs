---
description: Helpful concepts and general terms to understand Jet's Fixed Rate application.
---

# Fixed Rate Concepts

**See also: More information on the fixed rate application and how it works:**

{% content-ref url="../../protocol/jet-products/fixed-rate.md" %}
[fixed-rate.md](../../protocol/jet-products/fixed-rate.md)
{% endcontent-ref %}

#### _General Fixed Rate Terms_

**Tenor:** The time duration of a loan.

**Rate:** The annualized interest rate of a loan.

**Market:** In the context of the fixed rate application, the market is the combined token being lent along with the tenor. For example, there is a 1 day USDC market and a 30 day USDC market.

**Autoroll:** A feature of the fixed rate application that when enabled allows lenders to lend their capital continuously and borrowers to borrow continuously. [For more details, see the fixed rate page.](../../protocol/jet-products/fixed-rate.md)



_**Order Types**_

**Offer Loan:** Post a loan offer to the orderbook by specifying an amount to lend and the minimum rate you would lend it out at. See [See offer loan example](../../support/get-started/devnet-fixed-rate-application-guide/examples-of-borrow-and-lend-orders/how-to-offer-a-loan.md).

**Lend Now:** Choose a token amount to lend out and it will be lent immediately at the best (highest) available rates on the orderbook (assumes there is sufficient available collateral). [See lend now example.](../../support/get-started/devnet-fixed-rate-application-guide/examples-of-borrow-and-lend-orders/how-to-lend-now.md)

**Borrow Request:** Post a borrow request to the orderbook by specifying an amount to lend and the minimum rate you would lend it out at. [See borrow request example](../../support/get-started/devnet-fixed-rate-application-guide/examples-of-borrow-and-lend-orders/how-to-borrow-now.md).

**Borrow Now:** Choose an amount to borrow and it will be borrowed immediately at the best (lowest) available rates on the orderbook (assumes there is sufficient available collateral) . [See borrow now example.](../../support/get-started/devnet-fixed-rate-application-guide/examples-of-borrow-and-lend-orders/how-to-borrow-now.md)



_**Posted**_ _**versus**_ _**Matched Orders**_

An orderbook is like a marketplace with buyers and sellers shouting prices at each other from their stalls, but nobody will compromise on their prices until someone comes along and places a **taker** order, taking the best price available to buy or sell. **Makers** put orders on the orderbook and specify how much they would like to lend or borrow, and and what rate they are willing to lend or borrow at.

**Maker:** A maker order is the side of thee market that  **makes** liquidity on the orderbook and waits for another party to take it. For example, with a limit order like 'offer loan' or 'borrow request'.

**Taker:** A taker order is one that **takes** liquidity from the orderbook by using a market order like 'borrow now' or 'lend now'.&#x20;



#### _Order Panel:_

**Fill:** The amount of an order that has already matched (filled) with the counterparty.

**Repayment Date:** The date and time that a loan is due.

**Posted Repayment Amount:** The total amount of a loan necessary to be repaid including interest and fees. Posted indicates that this part of the order will be posted to the orderbook.&#x20;

**Posted Interest:** The total amount of interest on the loan necessary to be paid. Posted indicates that this part of the order will be posted to the orderbook.&#x20;

**Posted Rate:** The rate chosen by the lender or borrower at which their capital may be lent or borrowed.  Posted indicates that this part of the order will be posted to the orderbook.&#x20;

**Matched Repayment Amount:** The total amount of a loan necessary to be repaid including interest and fees. Matched indicates that this part of the order will be immediately matched with a preexisting order on the orderbook.

**Matched Interest:** The total amount of interest on the loan necessary to be paid. Matched indicates that this part of the order will be immediately matched with a preexisting order on the orderbook.

**Matched Effective Rate:** The average rate of the loans or borrows comprising the order, if it is executed.&#x20;

**Risk Level:** The ratio of liabilities and required collateral to the (weight-adjusted) collateral in your account.
