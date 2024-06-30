# DegenToken Smart Contract

This repository contains the smart contract for the DegenToken (DGN), implemented in Solidity.

## Overview

DegenToken is a basic ERC20 token with additional functionalities such as minting, burning, and a redemption feature.

- **Name**: DegenToken
- **Symbol**: DGN
- **Total Supply**: Defined during contract deployment

## Features

1. **Transfer Tokens**: Users can transfer DGN tokens to other addresses.
2. **Mint Tokens**: Only the contract owner can mint new DGN tokens.
3. **Burn Tokens**: Users can burn their own DGN tokens, reducing the total supply.
4. **Redemption**: Allows users to redeem tokens for prizes, implemented with a `Redeem` function.

## Prerequisites

- Understanding of Ethereum and Solidity
- Development environment set up with Solidity compiler (e.g., Remix, Truffle)

## Usage

1. **Deployment**: Deploy the smart contract to an Ethereum-compatible blockchain.
2. **Interact**: Use any Ethereum wallet or script to interact with the deployed contract.
   - Transfer tokens
   - Mint new tokens (owner only)
   - Burn tokens
   - Redeem tokens for prizes

## Getting Started

To get started with this repository:

```bash
git clone <repository-url>
cd DegenToken
```
## Authors

Swayam Raj Singh

[swayam](https://academy.metacrafters.io/profile)

## License
This project is licensed under the MIT License. See the LICENSE file for more details.
