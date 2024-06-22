# Solidity

## MyToken Smart Contract

This repository contains the smart contract for a custom token on the Ethereum blockchain. The token is named "Tether" with the abbreviation "USDT". The contract allows minting and burning of tokens and tracks balances associated with addresses.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Functions](#functions)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

This project implements an ERC-20-like token contract on the Ethereum blockchain. The contract allows the creation (minting) and destruction (burning) of tokens and keeps track of each address's balance.

## Features

- Public variables for token details (name, abbreviation, total supply).
- Mapping to store the balance of each address.
- Mint function to create new tokens.
- Burn function to destroy tokens, with checks to prevent burning more tokens than the address holds.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Aviraj2003/Solidity.git
   cd solidity
   ```

2. Install the required dependencies if any.

## Usage

To use this smart contract, you can deploy it on an Ethereum-compatible blockchain using a tool like Remix, Truffle, or Hardhat. Below are the instructions for using Remix.

### Using Remix

1. Open [Remix IDE](https://remix.ethereum.org/).
2. Create a new file and paste the contract code into the file.
3. Compile the contract.
4. Deploy the contract using the "Deploy" button in the Remix interface.
5. Interact with the contract using the deployed instance.

### Example Usage

```solidity
// Minting 100 tokens to the address 0x123...
MyToken.mint("0x123...", 100);

// Burning 50 tokens from the address 0x123...
MyToken.burn("0x123...", 50);
```

## Functions

### Public Variables

- `tokenName`: The name of the token (e.g., "Tether").
- `tokenAbbrv`: The abbreviation of the token (e.g., "USDT").
- `totalSupply`: The total supply of the token.

### mint(address _add, uint _value)

Creates new tokens and assigns them to the specified address. Increases the total supply by the specified value.

**Parameters:**
- `_add`: The address to which the tokens will be minted.
- `_value`: The number of tokens to mint.

### burn(address _add, uint _value)

Destroys tokens from the specified address. Decreases the total supply by the specified value. Ensures the address has sufficient balance to burn the tokens.

**Parameters:**
- `_add`: The address from which the tokens will be burned.
- `_value`: The number of tokens to burn.

**Requirements:**
- The address must have a balance greater than or equal to the number of tokens to burn.

## Contributing

If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License. 

## Contact

For questions or feedback, feel free to contact me:

- Email: aviraj9888@gmail.com
- GitHub: [Aviraj2003](https://github.com/Aviraj2003)

---
