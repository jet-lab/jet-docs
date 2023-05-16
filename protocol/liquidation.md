# Liquidation

**\*UNDER CONSTRUCTION -- MORE DETAILS TO COME\***

The liquidator is a bot that keeps the protocol safe for all users. When the risk indicator goes above 1.0, that account is subject to liquidation. The liquidator will attempt to liquidate an account's most risk positions first, deemed by those positions that are contributing the most to the current risk level.&#x20;

In the event of liquidation, a 3% fee is charged by the liquidator. [See fees page](fees.md).

In the event of borrower liquidation, the liquidator will attempt to pay back the borrowed funds with funds of the same token type in the borrower's margin account. If the assets are available to pay down the debt at this time, the liquidator will NOT charge any fees to the user for this convenience.&#x20;
