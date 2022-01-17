# JET Staking

We envision JET staking as the ultimate place for long term believers in the protocol. For that reason, we combined governance and staking into a single module -- To vote on DAO proposals, users must be staked in the JetGovern application.&#x20;

**Unbonding Period**

Should a JET holder wish to move their tokens once claimed and staked, a user must initiate  unbonding of their staked tokens in order to be able to remove them from the module. During the unbonding period, staked JET will remain held in the insurance fund (described below) and will not accrue additional airdropped tokens, or be available for voting on proposals. Any votes that have been cast on active proposals will be rescinded.

The bonding period duration is 29.5 days (one full lunar cycle). After beginning the unbonding period, the total JET in the process of unbonding will be displayed as so in the JetGovern dashboard. Additionally, a countdown until the end of the unbonding period for each unstaked lot will be displayed on the "Flight Logs" page. When the unbonding period for any lot of unstaked tokens ends, a "withdraw" button will appear on the dashboard near the "stake/unstake" buttons for tat lot -- The user may then withdraw JET back to their wallet when they choose to do so.

If the user changes their mind and would like to restake before their JET is unbound and available for withdrawal, they may do so in the "Flight Logs" page at any time during the unbonding period. Restaking will re-enable rewards instantly, and users may again vote on proposals with that lot of JET.&#x20;

Note that if a user cast a vote on an active proposal and unstaked those tokens, they will need to re-vote on the proposal after restaking, since the act of unstaking and placing JET into the unbonding queue rescinds any active votes.

#### Earn Protocol Fees by Staking

While staked, users will earn a set chunk of protocol revenue equal to 40% of all protocol revenue as described on the ["Fees" page](fees.md)

#### **Staked JET as a Primary Insurance Fund**

Staked JET makes up the junior tranche of the Jet Insurance Fund, which backstops the protocol, protecting depositors against losses in the event of an incident. Subject to governance processes, the protocol treasury may also provide relief in these instances.

These funds could be mobilized via governance on issues such as: Code exploits which target total value locked or individual users funds Oracle or liquidation failures which cause bad debt to cause the system’s functionality to stop working

We envision that in the future, and subject to governance, only a portion of staked JET will enter the insurance fund, with the rest being actively managed by Jet DAO governance.
