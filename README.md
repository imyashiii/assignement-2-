# MyToken
This solidity program basically used to mint and burn a specific token that is mentioned in the program. The main purpose of this program is to get the normal understanding about the basic conepts of solidity like- variables, mapping, function, conditional statements etc.

## Description
This program is written in solidity which is mostly used to build smart contracts. In this program we have created a smart contract named as MyFirstToken. In this contract I have specified the name of the token and the total supplied tokens to different addresses. After that we have created two functions for transaction of the tokens. First function is to mint (add) tokens and the second one is for burn (deducting) tokens from the specified address. These addresses are mapped with balances which holds the value of the tokens in that particular address.

## Getting Started

### Executing Program
To execute this program you can go to the Remix IDE which is open IDE for Solidity. For that you can click on this link https://remix.ethereum.org/

Once you successfully reached to the IDE create a new file by clicking on the '+' icon and saving that file with .sol extension (e.g. MyToken.sol). After this copy and paste the code in your file that is given below 

```javascript
pragma solidity 0.8.18;
contract MyFirstToken {
    string public tokenName = "Beta";
    uint public totalSuppliedTokens; 
    mapping (address => uint) public balances;
    function minting(address a, uint tokens) public{
        totalSuppliedTokens += tokens;
        balances[a] += tokens;
    }
    function burning(address a, uint tokens) public{
        if(balances[a] >= tokens){
            totalSuppliedTokens -= tokens;
            balances[a] -= tokens;
        }
    }
}

```

After pasting this code you have to compile the code from the left hand sidebar. click on the 'Solidity Compiler' then click on the 'Compile MyToken.sol' button.

After the successful compilation of the code you have to deploy the program. For that you have again another option on the left sidebar that is 'Deploy & Run Transactions' and then you will see a deploy button; before clicking on it make sure that the file showing there is 'MyToken.sol'. Then you will be able to see the file in the 'Deployed/Unpinned Contracts' click on that now all the public variable and functions are visible to you now execute and fetch the values according to you.


## Authors
Yashika Swami

## License
This project is licensed under the MIT License.
