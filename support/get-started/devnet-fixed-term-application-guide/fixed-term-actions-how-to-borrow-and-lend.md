---
description: Actions in which you can interact with the Fixed Term market
---

# Fixed Term Actions - How to Borrow and Lend

### **Maker/Taker Actions**

**Offer Loan** - Post an amount of tokens that you are willing to lend out, and the minimum interest rate you will accept for that loan. This is a “maker” order and can be accessed from the “Lend” tab.&#x20;



**Lend Now** - Lend out a chosen amount of tokens immediately, based on what is already posted to the order book. This is a “taker” order and can be accessed from the “Lend” tab.\


**Borrow Request** - Post an amount of tokens that you would like to borrow, and the maximum interest rate you would want to pay for that loan. This is a “maker” order and can be accessed from the “Borrow” tab.\


**Borrow Now** - Borrow a chosen amount of tokens immediately, based on what is already posted to the order book. This is a “taker” order and can be accessed from the “Borrow” tab.\


**Note:** Maker orders (offer loan / borrow request) are “maker” orders by default, but if there is  existing liquidity on the books that meet the conditions of the posting, then part of all of the order will actually be a “taker” order for the parts that intersect.

****

**Also Note:** For the purposes of testing, if you want to match your own order, you will need to be sure to post the maker order to the top of the orderbook; or to take enough liquidity from the book that you reach your order in the taker order. For example, if you post a borrow request for 100,000 USDC at a minimum of 5%, when you go to “lend now” in a separate margin account with 100,000 USDC, that “lend now” order will by default take the lowest interest rates on the book.&#x20;

\
This means that if there were borrow requests of, say 100,000 USDC at 4%, your “lend now” action will take the 100,000 USDC at 4% since it is at a lower rate (thus cheaper and higher in the orderbook) than the 100,000 USDC you posted at 5%. If instead of posting at 5%, you posted the borrow request at 3% and that was the best available rate on the book, your “lend now” order from a second margin account would match the borrow request from your first margin account.





<figure><img src="../../../.gitbook/assets/Screen Shot 2023-03-03 at 7.43.31 AM.png" alt=""><figcaption><p>Fixed Term Lending Actions on Lend View</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/Screen Shot 2023-03-03 at 7.36.40 AM.png" alt=""><figcaption><p>Fixed Term Borrowing Actions on Borrow View</p></figcaption></figure>

### Fixed Term Action

Choose Market by selecting the tenor. This action is available on both "Lend" and "Borrow" tabs.

<figure><img src="../../../.gitbook/assets/Screen Shot 2023-03-03 at 7.49.53 AM.png" alt=""><figcaption><p>Fixed term market tenor selection</p></figcaption></figure>

### Auto-Roll Action - future release

This service allows you to continue to lend or borrow once your first position has reached maturity. You may choose to have this service on or off.&#x20;
