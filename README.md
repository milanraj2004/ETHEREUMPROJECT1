# ETH1_Project - ETH PROOF: Beginner EVM Course
Presenting a basic Solidity smart contract that simulates a token and has the necessary features, like minting and burning tokens.




## Description:-
Solidity is a programming language used to create smart contracts on the Ethereum blockchain, and this program represents a contract written in that language. Everything that was covered in the ETH Beginner Course under Solidity is all compiled into one program. Examples of this include public variables that hold information about your coin, a mapping from addresses to balances, a mint function that requires two parameters (an address and a value), and a burn function.


## Getting Started And Code

Remix is an online Solidity IDE that you may use to run this program. Visit https://remix.ethereum.org/ to get started on the Remix website.

To start a new file on the Remix website, click the "+" symbol located in the sidebar on the left. Save the file (for example, ETH!_Project.sol) ending in.sol. Paste the following code into the file after copying it:

```javascript

// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

contract MyToken {

    // public variables here
    string public Token_Name ="MILAN kanishk ";
    string public Token_Abbrev="RAJ";
    uint public total_Supply = 0;


    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        total_Supply += _value;
        balances[_address] +=_value;
    }

    // burn function
    function burn (address _address, uint _value) public {
      if (balances[_address] >= _value){
        total_Supply -= _value;
        balances[_address] -=_value;
    }
    }

}
```

## Overview

This project aims to provide users a hands-on grasp of a variety of topics covered in the ETH_Beginner Course on Solidity. To support learning and show how important Solidity concepts work, this software offers practical examples and implementations.
