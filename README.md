# Project: Create a Token

This Solidity  program demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to understand the require(), assert() and revert() statements.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract have three statements.Revert() Statement is 
used to roll back state changes and provide a meaningful error message to the user,Assert() is used to check for internal errors or bugs in the contract.and at the last require() is used to ensure
valid condition such as inputs, contract state variables etc.
## Getting Started

### Executing program

To run this program, you will use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., project.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.4;

contract singhToken {
    string public tokenName = "Whatsapp";
    string public tokenAbbrv = "Wtps";
    uint public totalSupply = 0;
    mapping(address => uint) public balances;
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }
    function burn(address _address, uint _value) public {
        require(balances[_address] >= _value, "Insufficient balance to burn");
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar.  click on the "Compile project.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "project" contract from the dropdown menu, and then click on the "Deploy" button.
these are the further steps 
1.Once the contract is deployed, we wi;; click on the  total supply which  is zero.
2.We will have  our token name of whatsapp and abbriviation wtps
3.we will click on the account up then copy it to the clipboard
4.we will paste it to the mint and put  some random tokens to it
5.cilck on the total supply then paste this same address to our balances
6.paste that addressin the burn function  and put value lower than the supply
7.we check our total supply

## Authors

Harman Singh

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
