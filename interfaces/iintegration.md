---
description: >-
  Standard interface for a yield integration contract compatible with the
  Kernel.
---

# IIntegration

{% hint style="info" %}
An Integration represents a single pool of funds at the system integration level. However, the integration may ultimately adapt to any number of points in the external integration.
{% endhint %}

{% hint style="warning" %}
The system will recognize an integration implementing `IIntegration` by denoting it as poolID 0.
{% endhint %}

```
// SPDX-License-Identifier: GPL-2.0
pragma solidity 0.8.4;

interface IIntegration {
    event Deploy(address token, uint256 amount);
    event HarvestYield(address token, uint256 amount);
    event Deposit(address token, uint256 amount);
    event Withdraw(address token, uint256 amount);

    /// @param tokenAddress The address of the deposited token
    /// @param amount The amount of the token being deposited
    function deposit(address tokenAddress, uint256 amount) external;

    /// @param tokenAddress The address of the withdrawal token
    /// @param amount The amount of the token to withdraw
    function withdraw(address tokenAddress, uint256 amount) external;

    /// @dev Deploys all tokens held in the integration contract to the integrated protocol
    function deploy() external;

    /// @dev Harvests token yield from the integration
    function harvestYield() external;

    /// @dev This returns the total amount of the underlying token that
    /// @dev has been deposited to the integration contract
    /// @param tokenAddress The address of the deployed token
    /// @return The amount of the underlying token that can be withdrawn
    function getBalance(address tokenAddress) external view returns (uint256);

    /// @dev Returns the total amount of yield awaiting to be harvested
    /// @dev using the relevant integration's own function
    /// @param amount The amount of available yield for the specified token
    function getPendingYield(address) external view returns (uint256 amount);
}

```
