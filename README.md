# MetaToken Smart Contract

## Overview

The `MetaToken` smart contract is an ERC20 token implementation built on the Ethereum blockchain. It allows for minting by the owner, transferring tokens, and burning tokens. This contract leverages the OpenZeppelin library for secure and standard token functionality.

## Features

- **Minting**: The contract owner can mint new tokens.
- **Transferring**: Users can transfer tokens to other addresses.
- **Burning**: Users can burn their own tokens to reduce the total supply.

## Smart Contract Functions

### 1. `constructor()`

- **Description**: Initializes the ERC20 token with a name ("MetaToken") and symbol ("MetaToken"). Sets the contract deployer as the owner.

### 2. `mint(address _to, uint256 _amount)`

- **Description**: Mints new tokens and assigns them to the specified address.
- **Parameters**:
  - `_to`: The address to receive the minted tokens.
  - `_amount`: The amount of tokens to mint (without decimals).
- **Modifiers**: `onlyOwner` - Only the owner can call this function.

### 3. `transfer(address to, uint256 value)`

- **Description**: Transfers tokens from the sender to the specified address.
- **Parameters**:
  - `to`: The address of the recipient.
  - `value`: The amount of tokens to transfer.
- **Returns**: A boolean indicating success.

### 4. `burn(uint256 _amount)`

- **Description**: Burns a specified amount of tokens from the caller's balance.
- **Parameters**:
  - `_amount`: The amount of tokens to burn.

## Error Handling

- **Require Statements**: Used to validate conditions:
  - Ensures the caller has a sufficient balance before transferring or burning tokens.
  - Ensures only the owner can mint new tokens.

## Deployment

To deploy the contract, you can use tools like Remix, Truffle, or Hardhat. Here's how to do it with Remix:

1. Open [Remix IDE](https://remix.ethereum.org/).
2. Create a new file and paste the contract code.
3. Install the OpenZeppelin Contracts library by adding the dependency in the Remix environment.
4. Select the appropriate compiler version (0.8.13 or above).
5. Compile the contract.
6. In the "Deploy & Run Transactions" tab, select the contract and click "Deploy".

## Usage

After deploying the contract, you can interact with it through the Remix interface or integrate it into a web application using Web3.js or ethers.js.
