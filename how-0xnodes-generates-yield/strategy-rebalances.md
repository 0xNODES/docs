# Strategy Rebalances

Rebalancing is part of the aggregation operation that allows 0xNODES to generate maximum yield for users at reduced costs; specifically, the platform batches all user assets when it deploys funds into a strategy, performing operations on all funds at once for massive efficiency gains.&#x20;

When the rebalance operation occurs, any kernel assets that need to be deployed to strategies are moved, and any strategy assets that need to be brought back to the kernel will be moved. There is typically a net positive or negative that needs to be moved during each rebalance. Immediately after rebalance, necessary assets will be available in the kernel for withdrawal.&#x20;

Please note that when you exit a strategy, your strategy asset balances are updated in the accounting contract. If you wish to enter another strategy, you may do so immediately. If you wish to withdraw your assets from the system completely, you may have to wait until the strategy’s funds are rebalanced to withdraw the funds to your wallet. The kernel maintains a reserve balance so that most user withdrawals will not usually encounter this.&#x20;

0xNODES is implementing a synthetic credit network, which will allow for all withdrawals to occur without rebalancing, streamlining the withdrawal process for the user.
