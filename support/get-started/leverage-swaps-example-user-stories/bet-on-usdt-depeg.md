# Bet on USDT Depeg

* Amelia thinks that USDT is going to depeg from $1 in the short to medium term and decides to use Jet’s leverage swaps to short USDT.
* By using Jet’s leveraged swaps to swap from USDT to USDC on margin, she can hold a short position for as long as she likes. Her cost over time is limited to the interest rate for USDT borrows on Jet (in addition to any costs for the cost of the swap; swaps are routed through Orca at this time)
* Note that another potential risk in this scenario is if USDC depegged while Amelia’s position is open – but she is confident that it will not do so.
* She deposits USDC into the Jet V2 application, which immediately begins earning interest.
*   Using her USDC as collateral, she sets up a leverage swap from USDT to USDC, which will borrow USDT and swap it for USDC in the same transaction. She is now short USDT/USDC.

    She’s also happy to continue earning interest on the USDC that she swapped for while her position is open – depending on the rates, this might even cover a big chunk of the interest she will pay on the USDT borrows!
* She clicks the “max leverage” button and executes the swap.
* It turns out that Amelia was correct! In this timeline, USDT depegs and rapidly approaches $0.
* Amelia decides to take profit and close out the position.
* Amelia makes sure not to swap back any more USDC than she needs to in order to repay the loan, since USDT now has essentially zero value.
* So, she makes certain to only swap as much USDC as she needs to repay the debt.
* She checks exactly how much USDT she borrowed by looking at the handy table beneath the swap operations panel.
* Next, she reverses the order of the swap so that it will swap USDC to USDT.
* This time, she inputs the amount of USDT that she needs to repay in the “for” input box; the second box that is being swapped into. The amount of USDC needed to pay off the loan is then calculated bt the app and loaded into the first “swap” input box. This amount will be a tiny fraction of the USDC in her account and may even be negligible depending on how close to $0 USDT has depegged to.
* She also clicks the toggle button labeled “repay USDT loan” on the order panel so that her USDT debt will be repaid in the same transaction as the swap.
* She will be left with only USDC in her account, the original amount + profits.
* She successfully shorted USDT with respect to USDC, paying only the interest on the borrows, and earned a profit!

\
