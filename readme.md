# My Token

This "My Token"-style Solidity application shows the fundamental syntax and features of the Solidity programming language. This program's goal is to provide as a jumping-off point for individuals who are unfamiliar with Solidity and wish to acquire a sense of how it operates.

## Description

Written in Solidity, a programming language for creating smart contracts for the Ethereum blockchain, this application is a straightforward contract. A single function in the contract returns the string "My Token!" This software acts as an easy-to-understand primer on Solidity programming and can be used as a springboard for later, more intricate projects.

## Getting Started

### Executing program


To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {
    // public variables here
string public TokenName = "Charlie";
string public TokenAbbrv = "CHRL";
uint public  TotalSupply = 0;

    /// mapping variable here
    mapping(address => uint) public balances;
     
// mint function
    function mint (address _address, uint _value) public {
       TotalSupply += _value;
       balances[_address] += _value;
    }
    
// burn function
    function burn (address _address, uint _value) public {
       if (balances[_address] >= _value) {
          TotalSupply -= _value;
          balances[_address] -= _value;
       }
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile Jackelyn.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

## Authors

Jackelyn G. Dialino

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
