# MyToken
This program is a solidty programe and is written to understand and demonstrate simple functions and units in the language. this can be called a starting point for eveeryone who's intending to leanr more about solidity anmd the thinsg which can be done in this langauge.

## Description
this is a solidity program and we use solidity to program various things in the fintech industry. this code here has two main simple fucntions namely mint and burn. as suggested in the name the mint function adds and burn functions subtracts or burns tokens. All of this happens whenwe pass a certain amount of tokens with a given address and minting and burning of tokens take place.

## Getting Started
### Executing program
To run this program we use an online etherium IDE called remix as shown in the course

We start by creating a new file and then save the file with a .sol extension(which says that its a solidity language file) Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT 
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "ADVIKHOLAU";
    string public tokenAbbrv = "AH";
    uint public totalSupply = 0;
    // mapping variable here
    mapping(address => uint) public balances;
    // mint function
    function mint (address tokenaddr,uint t_value) public {
        totalSupply += t_value;
        balances[tokenaddr] += t_value;
    }
    // burn function
    function burn (address tokenaddr,uint t_value) public {
        if (balances[tokenaddr] >= t_value){
            totalSupply -= t_value;
            balances[tokenaddr] -= t_value;
        }
    }

}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to the appropriate compatible version), and then click on the "Compile" button

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab. Select the "MyToken" contract, and then click on the "Deploy" button.

We can interact with it once the contract opens(interact i.e. minting and burn ing and balancing tokens. Click on the "MyToken" contract in the left-hand sidebar, and then click on any of its functions to interact with it.

## Authors
Advik Holalu
@advikholalu@gmail.com

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
