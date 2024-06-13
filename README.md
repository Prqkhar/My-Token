# My Token

Simple overview of use/purpose: This Solidity smart contract implements a basic ERC20-like token (`MyToken`) with functions to mint new tokens and burn existing tokens.

## Description

`MyToken` is a basic implementation of a token on the Ethereum blockchain. It includes functionality to mint new tokens and burn existing tokens, managing balances using mappings. The contract starts with a total supply of 0 and allows for dynamic minting and burning of tokens as needed.

## Getting Started

### Installing

To download and interact with the `MyToken` smart contract:

1. Clone the repository from GitHub:

   git clone https://github.com/yourusername/MyToken.git

2. Navigate into the project directory:

cd MyToken/

## Executing Program

To run and deploy the MyToken contract:

Use Remix IDE or your preferred Solidity development environment.
Compile the MyToken.sol file with Solidity version ^0.8.0.
Deploy the contract on a local blockchain or test network like Ropsten.
solidity

// Example deployment script in Remix IDE
pragma solidity ^0.8.0;

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract MyToken {

    // Public variables for token details
    string public tokenName = "Master_Chief";
    string public tokenAbbreviation = "MC";
    uint public totalSupply = 0;

    // Mapping of addresses to balances
    mapping(address => uint) public balances;

    // Mint function to increase total supply and address balance
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // Burn function to decrease total supply and address balance
    function burn(address _address, uint _value) public {
        require(balances[_address] >= _value, "Insufficient balance");
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}


## Help

If you encounter any issues or have questions:

Check the Solidity documentation for language-specific questions.
Review the contract code for specific functionality details.
Contact the author for further assistance.

## Authors

Author Name: Prakhar Tiwari

Contact: dhruvtiwari360@gmail.com
