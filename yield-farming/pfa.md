# BIOS Protocol Fee Accrual (PFA)

{% hint style="info" %}
We're still working on this page. More coming soon!
{% endhint %}

Yield in System11 is disutributed according to the values set in the YieldManager contract.

You can read the current values from the ABI method: getEthDistributionWeights

There are four variables in the distribution weights. The YieldManager will sum the weights and divide the yield according to the proportions:

 - BIOS buyback: L1 asset directly applied to market buy of $BIOS
 - Treasury Account: L1 asset transferred to treasury account. This is used to fund gas for system transactions
 - PFA: L1 asset transferred into EtherRewards contract for distribution to $BIOS stakers (on current chain)
 - Strategy Rewards: L1 asset distributed to the holders of Strategy positions

BIOS buyback is typically set to 0.
Treasury Account is set to a minimal value per chain, so on ETH Mainnet it can be large, while a less-expensive chain will have a lower value (~1%).
PFA is typically set to 11%
Strategy Rewards takes the remainder, usually 88%.
