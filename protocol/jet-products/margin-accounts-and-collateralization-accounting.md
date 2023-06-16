# Margin Accounts and Collateralization Accounting

**See also: Margin Accounting Concepts and Terms:**

{% content-ref url="../../faq/glossary/margin-accounting-concepts.md" %}
[margin-accounting-concepts.md](../../faq/glossary/margin-accounting-concepts.md)
{% endcontent-ref %}

{% content-ref url="../../faq/glossary/pools-variable-lending-concepts.md" %}
[pools-variable-lending-concepts.md](../../faq/glossary/pools-variable-lending-concepts.md)
{% endcontent-ref %}

A margin account a ledger within a ledger, keeping track of assets and liabilities that the user has accrued through their interaction with integrated products. It is via the margin account that a user's deposits as construed as collateral against which the user can borrow or take other risk positions. Margin accounts keep the protocol safe by providing a liquidation mechanism to cover debts when necessary.

A particular user, identified by a public key, may have multiple margin accounts. These can be named for easy reference. The app allows seamless switching between margin accounts and for transferring assets between margin accounts. From a risk perspective all margin accounts are completely isolated. Liquidations only affect a particular unhealthy account, even if the user being liquidated also owns other margin accounts.

## Accounting

From an accounting perspective, a particular margin account can be viewed as a list of assets $${\cal A}$$ and a list of liabilities $${\cal L}$$. Margin accounting proceeds in terms of the USD value of these positions.

The **assets** $$A$$ and **liabilities** $$L$$ of the margin account are given by

$$
A = \sum_{a \in \cal{A}} P_a
$$

$$
L = \sum_{l \in \cal{L}} P_l
$$

where​ $$P_a \geq 0$$​ and $$P_l \geq 0$$​ are the USD values of the corresponding positions. The **equity** or **account value** is given by

$$
E = A - L
$$

​A margin account is required to have a minimum amount of equity in order to be considered healthy. The amount depends on the composition of assets and liabilities. **Collateral weights**, denoted $$w_a$$, influence the contribution of assets to **weighted collateral**, which is given by

$$
K_w = \sum_{a \in \cal{A}} w_a P_a
$$

Liabilities imply a certain amount of **required collateral** that depends on the size of the liability and the **required collateral factor**, denoted $$f_l$$​. The required collateral is given by

$$
K_r = \sum_{l \in \cal{L}} { P_l \over f_l }
$$

​The minimum equity condition is captured implicitly through the relationship between these quantities. A margin account is said to be **healthy** if the collateral-weight-adjusted-equity equals or exceeds the required collateral. That is, healthy accounts satisfy

$$
K_w - L \geq K_r
$$

​Otherwise the account is considered **unhealthy** and therefore **subject to liquidation**.

The following metrics are also used throughout the app and SDK to shed light on the state of a margin account:

**Leverage** is defined as

$$
{\rm leverage} = { A \over  A - L }
$$

​Although a useful quantity when considering a portfolio, it does not connect directly with account health. A related quantity that does is the **adjusted leverage**, given by

$$
{\rm adjusted\ leverage} = { K_w \over K_w - (L + K_r) }
$$

{% hint style="info" %}
The adjusted leverage is defined to be zero when $$K_w$$​ is zero and there are no liabilities, and to be infinity when $$K_w \leq L + K_r$$.​
{% endhint %}

The adjusted leverage is equal to one when an account has assets but no liabilities, and increases to infinity at the liquidation threshold.

The **account risk indicator** is displayed prominently in the app. Account risk is defined to be

$$
\rho = { L + K_r \over K_w }
$$

{% hint style="info" %}
If $$K_w$$​ is zero the account risk is zero if there are no liabilities, or infinity if there are.
{% endhint %}

The account risk indicator is zero for an account with no liabilities, and increases to **one at the liquidation threshold**.

The app will not allow a user to put their margin account into an unhealthy state or into a state very close to liquidation. This guard is called the **setup check**. The app only allows a user to take an action that increases the risk indicator for their account if the account would still be healthy with double the required collateral after the action is completed.

This risk indicator has a direct connection to the change in value of collateral assets that would bring an account to the liquidation threshold. Let $$r_a$$​ denote the return on collateral asset $$a$$. We can define the **collateral-weighted return** as:

$$
R=\sum_{a \in \cal {A}} {w_a P_a \over K_w} r_a
$$

​If the risk indicator is $$\rho$$​ then the collateral-weighted return that would bring the account to the liquidation threshold is:

$$
R = \rho - 1
$$

For example, suppose that a user has a USD loan backed by mSOL collateral. If the account risk indicator is $$0.9$$​, then a $$10\%$$ decreased in the price of mSOL will bring the account to the liquidation threshold.

The amount of adjusted equity in excess of required collateral is called **available collateral**:

$$
{\rm available\ collateral} = (K_w - L) - K_r
$$

​Available collateral is a USD quantity that expresses how close to liquidation a margin account is. The liquidation threshold lies at zero available collateral. [See the liquidation page for further details](../liquidation.md).
