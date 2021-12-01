---
description: The summary of Jet Protocol's vision for decentralized borrowing and lending
---

# 📄 Whitepaper

**JET PROTOCOL**\
****

**PROTOCOL WHITEPAPER**\
****\
****

![](https://lh3.googleusercontent.com/XJYkw05nBhavoltDn68VfUN82E77db2tulN8Fwq2mHsy-zk\_gDFUR2IjgWou0KfeQFfjorfUNYEzXw1XUJRltdyXOafOzwBDvJrHgoCrQyPGCfuWg1KPFCczoZG84sLdqaOvnzk)

**Version: 1.0**

**July 2021**\
****

**Authors: Wil Barnes and James Moreau**

**info@jetprotocol.io**

**Abstract:**

**This paper introduces Jet Protocol, a decentralized protocol for borrowing and lending on the Solana Blockchain. History, definitions, and design are covered.**

## **1. Introduction**&#x20;

Jet Protocol will launch as an open source, non-custodial, borrowing and lending protocol on the Solana Blockchain (“the Protocol” and “Jet Protocol”). The Protocol will allow users to deposit supported tokens to the Protocol. They will receive interest back to incentivize participation. Those deposits will sit in a pool that is also used for users looking to take out a loan in supported tokens. Because of this, individual users are not matched, and the Protocol can create rules to govern ratios, supported tokens, and a variety of other needs.

We believe that borrowing and lending protocols are necessary to any decentralized finance (“DeFi”) ecosystem. They have been largely successful to date. In developing Jet Protocol we paid close attention to prior efforts on other Blockchains, whether from our own experience or from projects we watched and used. The decision to build on Solana is largely based on Solana’s unmatched speed and lower fees. This will allow us to push the limits of on-chain decentralized finance lending. We anticipate broader interest in more efficient trading than other chains, with tighter collateral ratios (“cRatios”), enhanced oracle data, and more efficient centralized exchange like liquidations.

Jet will innovate on battle tested governance models from existing protocols, skewing towards community ownership and engagement. The most important aspect of this governance-first approach is to build an inclusive community to research, design, and implement useful lending products.&#x20;

A Jet user can borrow against over-collateralized debt positions, and may incur debt up to governance mandated debt ratios. If the value of a user’s deposited collateral falls under the specified ratio, their position may be liquidated by external actors, such as traders, or any users who can call the smart contract. In addition to lending, Jet will introduce interest rate product, secondary markets on Serum, and facilitate ongoing, community-driven lending product research & development.

From the outset, Jet will launch with a dedicated governance system that leverages our founding team’s unique and extensive experience on protocol governance. The goal of this governance-oriented approach is to work with the community to set a clear precedent and vision in how the protocol will be governed.

## **2. Solana Layer 1**

Solana has emerged as a prominent, decentralized finance focused chain. Solana’s market infrastructure is becoming more sophisticated and robust by the day. Solana has a central limit order book (Serum), an automated market maker (Raydium), and a growing list of innovative projects (Mango, PsyOptions, among others). Solana is ripe for integration. What’s missing is a borrowing and lending protocol leveraging Solana’s innate tech stack, speed, and extremely low transaction fees to allow market participants to borrow against their Solana assets.

Above all, Solana scales without the need for L2s or sharding, preserving atomic composability with other protocols. Rapid, sub-second blocktimes allow for better liquidity management, more innovative dynamic pricing from higher market data ingestion, and the ability to handle liquidations more gracefully via sequencing and confidence analysis of available liquidity during times of stress. All of which are infeasible on Ethereum.

Collateralization ratios of lending protocols are typically fixed, and can be quite high. For example, MakerDAO’s “ETH-A” collateral type requires 150% collateralization. And the liquidation systems of these protocols have broken down and resulted in substantial loss of user funds. Jet will combine Solana’s raw computational power with innovative and fast oracle solutions to introduce dynamic collateralization ratio pricing, allowing ratios to be adjusted based on the level of volatility in the system.

To put it plainly, because of Solana’s throughput the protocol can ingest data more quickly. This allows for rendering price and interest updates more frequently during times of market volatility, and thus propagating actionable data across the network to all market participants in seconds. And inversely, during periods of inactivity, the protocol relaxes.

Rust is the general-purpose language of the Solana blockchain, a language more sophisticated with a much larger developer base than that of Ethereum’s Solidity. Rust’s memory and type safety significantly reduces the cognitive overhead required of developers to write more secure contracts. While Solana is not yet on comparable terms with Ethereum in developer tooling maturity, we feel that trading system developers with Rust/C/C++ and systems engineering experience will be able to more easily adapt to the Solana codebase.

Our team is ecstatic about the opportunities made possible with Solana as our Layer 1. We feel strongly that the level of developer activity and ongoing investments in projects built on Solana, and the community supporting them, are incredibly healthy and show no signs of slowing.

## **3. Why Jet?**

On the topic of markets, we avoid altogether the platitude of “re-inventing” things that have existed forever. Instead the focus is to use our experience as traders, DeFi power-users, and governance participants to create better markets.

We’ve arrived at building this protocol on Solana because we know the existing Ethereum infrastructure likely isn’t going to foster wider adoption. We know what users want: capital efficiency, lower costs, and flexibility with their digital assets. Solana’s technology removes constraints surrounding limitations such as high gas costs and enables financial innovation at a fundamental level not possible on the existing, widely used Layer-1’s. We believe Jet will make the DeFi borrowing and lending experience much better.

### **3.1. Core Lending Protocol**

Jet’s core borrowing and lending function will build on the token-lending program found in the Solana Program Library repository as well as the applicable cross-margin pull request for the initial mainnet launch. From there our development team will carry forward the iterative improvement and maintenance of the protocol. \
****

## **3.2 Lending Products**

Beginning with the launch of the cross-margined lending protocol, extendable via APIs to traders, market-makers, and liquidity providers, the following features are introduced over the next two quarters in roughly the following sequence:

* Liquidity mining program to bootstrap liquidity.
* Implementation of interest-bearing tokens.
* Cross-chain modules for equalization of interest rates.

The product in this MVP state provides Solana market participants a place to deposit and borrow against their assets, manage their debt positions, and take positions on the interest rate differences among other layer 1’s such as Ethereum, Terra, and others. Further, the release of the above product gives way to more complex structured risk products:

* Leveraged borrowing automated position management
* Secondary markets for interest rate speculation
* Liquidity provisioning for senior and junior debt positions

These additional products will be developed on a strategic basis to capture opportunities before they emerge in the rapidly evolving DeFi capital markets ecosystem as the Jet Protocol base-layer products are adopted.\
****

#### **3.2.1 Liquidity mining to bootstrap liquidity**

Jet will run a longer duration liquidity mining program to bootstrap and keep liquidity on the protocol, naturally rewarding early liquidity providers with attractive yields. In turn, we provide token holders the avenue to vote on new collateral types and the types of lending products they would like to see implemented.

The ongoing maturation of bridges between Solana and Ethereum, and Solana and Terra, makes this process straightforward. Users can now easily transfer assets via both Sollet and Wormhole, with additional avenues in development.

#### **3.2.2 Implementation of interest-bearing tokens**

Working closely with the Solana community, we are aware of the proposed specification for interest bearing tokens, and are prepared to implement it and include it into the protocol as it’s a necessary step in the broader value proposition of the protocol.

#### **3.2.3 Leveraged borrowing automated position management**

Extremely low transaction costs relative to Ethereum allow positions to be updated with speed and efficiency. Users who wish can give approval for the protocol to manage and automatically rebalance their leveraged positions akin to the solutions DeFiSaver provides to MakerDAO vault owners.

This is done by selling a portion of the user’s deposit share of the pool, swapping it on the open market for their debt asset, repaying a portion of their pool debt, and updating the user’s balances. The haircut collateral requires the same number of collateral tokens to withdraw from the protocol.

#### **3.2.5 Secondary markets for interest rate speculation**

When a user deposits an asset into the protocol, they are returned a token representing their base deposit and a token representing their interest earned. From there, the user can trade their deposited interest rate against other interest rates on Serum’s central limit order book.

#### **3.2.6 Liquidity provisioning for senior and junior debt positions**

We will introduce a series of complex structured risk products on Solana, realizing the senior / junior debt proof of concept first explored by our team in the initial Solana Wormhole hackathon in November 2020.

#### **3.2.7 Liquidation**

In engineering a borrowing and lending protocol, we must discuss the liquidation processes required to ensure solvency of the network. A position is up for liquidation when it falls beneath its minimum cRatio. The protocol then attempts to partially liquidate a percentage of the position every N number of slots through limit order bids on Serum DEX.

#### **3.2.8 Governance**

We are working to include a version of the Solana Program Library Governance Module that fits the protocol’s specific needs. Voting on this module will originate from community-led discussion on the governance forum, and we will use our experience to support the community in putting a process in place.

We’ve been working in the industry long enough to understand on-chain governance isn’t settled at launch. Governance is a process that becomes a living breathing entity that calcifies into a regimented, community-driven process over time. Communities do not like being pigeonholed into minor roles at the outset of a product launch and will disengage if they feel they do not have appropriate influence.

At launch, the protocol includes a governance “terminal,” essentially the open endpoints, for anyone to execute changes and complete upgrades to the protocol if sufficient votes are secured. A technical skill set and knowledge of the protocol codebase is needed to use it effectively, but the endpoint is open to the public.

On that note, these endpoints will be aggressively defended, with time-locks, early adopter token agreements in place to counter rogue proposals, and steep proposal quorums on launch, that will be relaxed over time as it’s demonstrated the protocol is battle-tested and hardened enough to sustain governance attacks.

Upon mainnet launch, the collateral selection used to create debt positions will be fixed to SOL and the stablecoins borrowable against this debt position. After the initial few months of protocol usage, we will consider whether the health and performance of the MVP has met the expectations of the community. At this point the governance module will vote on expanding protocol capacity and changing parameters such as underlying collateral types, debt ceilings, bridge integrations, and interest rate models. Over time the expansion of parameters will increase to encompass the entire application and will remove central control of the foundation in place of community governance.&#x20;

To recap, based on our experience we feel dictating a “solved” governance spec here would be disingenuous at best and prefer to be upfront about the complexities. Protocol governance is open from the earliest stage, it is not simply a development team operating behind a multisig, control of the governance module is root level access and it will be defended with appropriate measures.&#x20;

## **4. We are uniquely positioned to deliver this protocol**

Our team is uniquely positioned to implement this protocol and expand its liquidity base. Our founding team draws experience from MakerDAO, ConsenSys, MetaMask, Lunie.io, Witnet.io, and Blockdaemon, with a combined 10+ years of in-the-trenches blockchain experience.

**We have first-hand experience on:**

* Stabilizing MakerDAO, a multi-billion dollar lending protocol, in the wake of March 12, 2020 drawdown, defending and fortifying it against flash loan attacks, and correcting the Dai stablecoin peg over Summer 2020.
* Leading the onboarding of over $3 billion dollars of digital asset collateral to MakerDAO without loss of value.
* Building out support, knowledge base, content and community for Ethereum’s most widely used wallet as it grew from 20,000 users to over 1 million.
* Leading support, content and community for the first multi-blockchain non-custodial staking and governance interface with over thousands of users and several hundred million USD staked through the platform.

Our team has proven, practical experience in this domain, researching and implementing innovative governance defense tools to navigate protocols through the complexity as well as building and supporting staking and participatory governance user interfaces making it easy for anyone to participate in important governance decisions. Our team developed the \`dark spell\`, a code execution mechanism allowing a timelock to exist while preserving the ability for the MakerDAO community to patch critical vulnerabilities without being frontrun by adversarial attackers. Our team was also deeply involved in the earliest days of Ethereum’s cambrian explosion of ICO’s, DEX’s and early DeFi protocols, supporting the most widely used Ethereum wallet to this day. &#x20;

## **5. Jet Roadmap 2021/2022**

**Q2 2021**

* Jet Protocol launches and incorporates
* $4.85 million seed round of funding closed
* Development of Jet Protocol begins

### **Q3 2021**

* Launch capped deposit mainnet of core lending MVP&#x20;
* Audit codebase in preparation for un-capped mainnet redeploy
* Begin research, design, & implementation of V2

### **Q4 2021**

* V1 automated leveraged position management
* V1 structured products
* continued V2 implementation
* Late Q4: testing of Jet V2

### **Q1 2022**

* Jet V2 Launch

## **6. Summary**

* Jet will launch as a borrowing and lending protocol on the Solana Blockchain.&#x20;
* The protocol can create rules to govern the ratios, supported tokens, and a variety of other needs.
* The protocol will innovate on battle tested governance models from existing protocols, skewing towards community ownership and engagement.&#x20;
* This governance-first approach will help build an inclusive community to research, design, and implement useful lending products.&#x20;

## **Disclaimers**

This paper is for general information purposes only and does not constitute investment advice, or a recommendation or solicitation to buy or sell any investment. This paper should not be used in the evaluation of the merits of making any investment decision. It should not be relied upon for accounting, legal, tax, or investment advice or recommendations. The information and opinions reflected herein are subject to change without being updated.&#x20;

## **References:**
