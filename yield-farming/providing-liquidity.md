---
description: Liquidity is Deployed into 0xNODES Strategies
---

# Providing Liquidity

Users provide liquidity on the 0xNODES platform by entering a Strategy. Users first need to deposit the native asset (e.g., ETH on Ethereum) into the system, often referred to as depositing into the kernel. Next, users invest by selecting and entering a strategy. Once a user has entered a strategy, the system takes care of the rest. Withdrawing funds is the opposite of entering a strategy. The user removes funds from the strategy (principal) and then withdraws funds from the kernel account into the user’s wallet (principal and yield).

![0x\_NODES Strategies: Deposit Native Assets, Earn Native Assets](<../.gitbook/assets/asset flow.png>)

The blockchain network will charge a gas fee for token approvals, kernel deposits, withdrawals, and entering or exiting a strategy. The kernel covers the cost of all other operations, therefore subsidising or significantly reducing the amount of gas and other fees that is typically required to participate in yield farming. For example, for a user to directly provide liquidity to three farms on Uniswap, the user would first need to execute three token swaps (incurring swap fees and gas costs), deposit their liquidity into three farms (gas costs), and stake the LP tokens three times (more gas costs). Beyond gas and swap fees, the user would also experience significant opportunity costs in the form of time: they would need to conduct significant research to identify the best liquidity pools, keep watch of APYs, and manually move their assets into optimal pools over time. 0xNODES takes care of all of this for you.
