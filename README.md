# ERC20 Token and Vault Smart Contracts

This repository contains two Solidity smart contracts: `ERC20` and `Vault`. The `ERC20` contract implements a basic ERC-20 token, named "Metacrafters" with the symbol "Meta," while the `Vault` contract serves as a simple vault to deposit and withdraw tokens.

## ERC20 Contract

### Overview
- The `ERC20` contract is an implementation of the ERC-20 standard token.
- It includes functionalities like transferring tokens, approving spending limits, transferring tokens on behalf of others, minting new tokens, and burning existing tokens.
- The token has a name ("Metacrafters"), symbol ("Meta"), and 18 decimals.

### Functions
1. **`transfer`**: Transfers tokens from the sender to the specified recipient.
2. **`approve`**: Approves a spender to spend a specific amount of tokens on behalf of the owner.
3. **`transferFrom`**: Transfers tokens from one address to another on behalf of the owner.
4. **`mint`**: Mints new tokens and assigns them to the caller.
5. **`burn`**: Burns a specified amount of tokens from the caller's balance.

### Events
- `Transfer`: Emitted when tokens are transferred.
- `Approval`: Emitted when approval for spending is granted.

## Vault Contract

### Overview
- The `Vault` contract is designed to act as a secure vault for depositing and withdrawing ERC-20 tokens.
- It takes an ERC-20 token address as a parameter during deployment and ensures that only that token can be deposited and withdrawn.
- Users can deposit tokens into the vault, receiving shares in return, and later withdraw tokens based on the number of shares they own.

### Functions
1. **`deposit`**: Allows users to deposit ERC-20 tokens into the vault, receiving shares in return. The number of shares is determined proportionally to the total supply and the amount deposited.
2. **`withdraw`**: Allows users to withdraw tokens from the vault based on the number of shares they possess. The withdrawn amount is calculated proportionally to the total supply and the number of shares burned.

### Variables
- `token`: Address of the ERC-20 token accepted by the vault.
- `totalSupply`: Total number of shares in the vault.
- `balanceOf`: Mapping of user addresses to their corresponding share balances.

## Usage
1. Deploy the `ERC20` contract to create the Metacrafters token.
2. Deploy the `Vault` contract, providing the address of the Metacrafters token as a parameter.
3. Interact with the ERC-20 token functionalities and deposit/withdraw tokens using the Vault contract.

## Author 

Niranjan D N

dnniranjan97@gmail.com
