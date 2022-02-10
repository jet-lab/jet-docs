# Interest Rates on Jet

**Utilization Ratio Determines Interest Rates**

The interest rates for each asset is dynamic (always changing) and determined as a function of the **utilization ratio** of each asset. For example, if 1000 USDC total has been supplied to the platform and 500 USDC is currently being borrowed, the utilization ratio for USDC at that moment would be 50%.

As the utilization ratio increases, the interest rate also increases. The interest rate curve on JET was designed with three segments, in order to improve upon and and add flexibility to the two segment curve typically used in borrowing and lending apps.&#x20;

![Jet Protocol's interest rate curve, expressed in both APR and APY terms](<../.gitbook/assets/image (8).png>)

****

**Tighter Interest Rate Spreads - Jet's Competitive Advantage**

**T**he Jet interest rate curve was designed with competition from other Solana-based protocols in mind. The **interest rate spread** is the difference between the lending and borrowing rates for a single asset, at a particular point in time. For example, if at this moment the USDC borrow rate was 11% and the lending rate was 24%, the spread for the USDC interest rate at that time is 13%.

The Jet interest rate curve was designed at a higher utilization ratio than the other protocols when the average market rates are less than approximately 45%. As a result, Jet offers the tightest interest rate spreads.

**On average, the platform with tighter spreads offers better lending and borrowing rates. This is what Jet wants to provide -- All users of the protocol are at their happiest with the tightest spreads, since the borrowers are paying less in interest, and the lenders are receiving more!**

The two below graphs compare the interest rate midpoints of Jet with other protocols on Solana, assuming that arbitrage and other market activity drives the midpoints of the same markets across different platforms to be approximately equal (As cryptocurrency markets continue to mature, this becomes even more true).



![](<../.gitbook/assets/image (7).png>)



![](<../.gitbook/assets/image (4).png>)



**How Jet Combats Liquidity Risk**

As the utilization ratio of an asset approaches 100%, **liquidity risk** increases, meaning that not all lenders will necessarily be able to withdraw fully at the same time (since at a high utilization, most of the deposited assets in that pool have been lent out and are under the control of the borrowers). Note that this issue is not unique to Jet and that it is common to all crypto applications that use the pooled lending model (such as AAVE and Compound on Ethereum, or Solend and Port Finance on Solana).&#x20;

To combat liquidity risk, Jet added a third segment to the interest rate curve. This third segment steepens dramatically at high utilization rates, enticing savvy lenders to deposit on the platform quickly and take advantage of the high interest rates paid (and thus combatting liquidity risk).



