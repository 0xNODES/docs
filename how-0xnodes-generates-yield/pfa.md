---
description: Use the BIOS Protocol Fee Accrual (PFA) System to Earn Native Assets
---

# How Staking BIOS Earns Native Assets

To learn _how_ to stake $BIOS, see [Getting Started](broken-reference).&#x20;

Users who stake $BIOS earn new rewards every time the protocol harvests yield. On a chain-by-chain basis, the protocol’s yield-harvesting processor periodically harvests and liquidates yield accrued from 0xNODES strategies. A portion of the yield collected from every strategy harvested on a chain is rewarded to users who stake $BIOS on that chain (see [Yield Distribution](yield-harvest-and-distribution.md)). Each user’s rewards are proportional to their share of the total amount of $BIOS staked on that chain.

$$
Native Asset Yield = \\ StrategyYield * StrategyPFAWeight * (\frac{BIOS Staked By User}{Total BIOS Staked})
$$

The [BIOS token](https://0xnodes.io/bios) is available on every chain supported by 0xNODES. At the time of writing, BIOS can be purchased on Uniswap (Ethereum), SushiSwap (Ethereum), PancakeSwap (Binance Smart Chain), QuickSwap (Polygon), and Hermes (Metis). Users can also [bridge BIOS across chains](../moving-bios-between-chains/how-to-move-your-bios-to-the-polygon-network.md) using a 3rd-party protocol such as MultiChain.
