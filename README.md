# FundMe Project

This repository contains a Solidity smart contract project for a decentralized funding application called "FundMe." The project utilizes the Ethereum blockchain and employs various scripts and contracts to manage the funding process.

## Smart Contracts

### `DeployFundMe.s.sol`

This contract handles the deployment of the FundMe contract. It initializes a HelperConfig contract to determine the active network configuration and deploys the main FundMe contract.

### `HelperConfig.s.sol`

This contract manages network configurations, providing the appropriate price feed address based on the network ID. It supports two network configurations: one for a specific network ID and another for any other network.

### `Interactions.s.sol`

This contract includes two scripts: FundFundMe and WithdrawFundMe. These scripts interact with the deployed FundMe contract to fund it and withdraw funds, respectively.

### `FundMe.sol`

The main FundMe contract allows users to fund the contract with Ether. It utilizes Chainlink price feeds to ensure that the funded amount meets a minimum USD value. The owner of the contract can withdraw funds and manage various functionalities.

### `PriceConverter.sol`

A library providing functions to convert Ether amounts to USD using Chainlink price feeds.

## Testing

The project includes tests for various functionalities. Notable test files are `InteractionsTest.t.sol` and `FundMeTest.t.sol`, covering interactions with the FundMe contract and its core functionality.

## How to Use

1. Deploy the `DeployFundMe` contract to initialize the `FundMe` contract.
2. Interact with the `FundMe` contract by using the `FundFundMe` script to fund the contract and the `WithdrawFundMe` script to withdraw funds.
3. Use the provided tests, such as `InteractionsTest` and `FundMeTest`, to ensure the correct behavior of the contracts.

Feel free to explore and contribute to the project. If you encounter any issues or have suggestions, please create an issue or pull request.
