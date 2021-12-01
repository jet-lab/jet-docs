# Understanding C-Ratio & Liquidation

So, what is the best way not to be liquidated, let’s explore the following together.

**What is a C-ratio?**

Jet’s C-ratio is the collateral-to-loan ratio. This C-ratio can be calculated using the following formula:

_C-ratio = collateral value / borrowed value_

A good way to think about the C-ratio is when you deposit $200 worth of Bitcoin as collateral, and then borrow $100 worth of USDC, the current C-ratio would be 200%.

**What is the liquidation threshold?**

Currently the liquidation threshold on Jet Protocol is 125%. A portion of your collateral will be liquidated to maintain a healthy C-ratio when it drops below 125%.

When you try to process a borrow or withdraw transaction that would bring your current c-ratio below 150%, the co-pilot system message will alert you that this is an unhealthy C-ratio.

**How can I avoid liquidation?**&#x20;

When the market is volatile, you are at a lower risk of getting your account liquidated when your c-ratio is at 500% compared to when your C-ratio is at 200%. Your C-ratio can drop much faster than you expect in highly volatile environments, so it’s best to always check where your ratio is at and be prepared to either add more funds to top it off or repay and close your position.
