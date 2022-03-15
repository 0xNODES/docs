# Yield Distribution

New native asset rewards, earned from providing liquidity to a strategy or staking BIOS, are distributed to the user every time yield is harvested from the [0xNODES Strategies](native-strategies.md). Users manage their rewarded yield through the [0xNODES website](https://system11.0xnodes.io) (i.e., view yield, claim/withdrawal yield, or enter yield into a strategy).

The 0xNODES yield harvester is the protocol that distributes rewards to users as claimable native assets. To liquidate yield the protocol periodically harvests funds deployed into high-performing pools by [0xNODES Strategies](native-strategies.md)_._ The protocol updates the annual percentage rate (APR) for each strategy on the __ [0xNODES website](https://system11.0xnodes.io) and [0xNODES subgraphs](../subgraphs/0xnodes-subgraphs.md).

![](<../.gitbook/assets/yield harvest.png>)

The protocol distributes yield into four proportions, based on distribution weights set in the YieldManager contract:

1. Strategy Rewards: % of yield distributed to the holders of a given strategy, in the form of native assets. Users who deposit native assets into strategies receive the largest proportion of the yield.
2. BIOS Protocol Fee Accrual (PFA): % of yield distributed to $BIOS stakers on the current chain, in the form of native assets.
3. BIOS buyback: % of yield used to the market buy of $BIOS&#x20;
4. Treasury Account: % of yield used to cover gas for system transactions, future development and maintenance of the platform, and investment losses so users can withdraw their full principal.

Distribution weights vary based on market conditions; users can view current weights by querying the getEthDistributionWeights ABI methods of the chain's [YieldDistribution contract](../contracts/other-contracts.md). Typically, strategy rewards are approximately 88%, the BIOS PFA rewards are approximately 11%, BIOS buyback is <1%, and the Treasury Account is set to a minimal value on a chain-by-chain basis, often ranging from 1-5 (Ethereum often has a higher Treasury Account % than other chains due to the high gas fees involved).
