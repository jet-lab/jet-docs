---
description: Information and documentation on how to interact with Jet Protocol
---

# ✈ Protocol

Jet Protocol is best conceived as a constellation of products centered around the margin program.

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

Jet Protocol core infrastructure includes:

* **Margin Accounts:** The Margin Account is similar to wallet, it allows user to margin their positions across all assets, products from the protocol.
* [**Margin Pools**](https://app.jetprotocol.io/)**:** The Margin Pools are traditional DeFi lending pools, engineered to lean on the Margin Accounts for collateral management.
* [**Fixed-Rate Markets**](https://app.jetprotocol.io/fixed-lend)**:** The Fixed-Term Markets provide users fixed-term and fixed-rate lending and borrowing on-chain.

Other products are supported by connecting external protocols to the margin program:

* [**Leverage Swaps**](https://app.jetprotocol.io/swaps)**:** Jet Swap program routes order to trading venue with most advantageous execution for the user.
  * Note that Orca, Saber, and Openbook are **external** protocols that Jet does not have any control over. Jet Margin program allows user's Margin Account to interface with these protocols for the purpose of swapping tokens.

In the following subsections, there are more details regarding margin accounting, interest rates, and fees:

{% content-ref url="jet-products/pooled-variable-lending-interest-rates-design.md" %}
[pooled-variable-lending-interest-rates-design.md](jet-products/pooled-variable-lending-interest-rates-design.md)
{% endcontent-ref %}

{% content-ref url="jet-products/margin-accounts-and-collateralization-accounting.md" %}
[margin-accounts-and-collateralization-accounting.md](jet-products/margin-accounts-and-collateralization-accounting.md)
{% endcontent-ref %}

{% content-ref url="jet-products/fixed-rate.md" %}
[fixed-rate.md](jet-products/fixed-rate.md)
{% endcontent-ref %}

This technical documentation will be evolving with the code over the coming months. If you have specific questions left unanswered, post on the forum here: [https://forum.jetprotocol.io/c/support/13](https://forum.jetprotocol.io/c/support/13)&#x20;
