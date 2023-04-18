# MY TOKEN

This Solidity smart contract named "MyToken" defines a custom token on the Ethereum blockchain. It allows the creation, tracking, and destruction of tokens.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has two functions: "mint" and "burn" which are used for adding and subtracting tokens from an address respectively. The "mint" function is used to add tokens to a specific address and increases the total supply of the token. The "burn" function is used to remove tokens from a specific address and decreases the total supply of the token.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;
contract MyToken {

// public variables here
string public tokenName = "SANJAY";
string public tokenAbbrv = "SAN";
uint public totalSupply = 0;


// mapping variable here
mapping(address => uint) public balances;



// mint function
function mint (address _address, uint _value) public {
totalSupply += _value;
 balances [ _address] += _value;
}


// burn function
function burn(address _address, uint _value) public {
if (balances [_address] >= _value) {
totalSupply -= _value;
balances[_address] -= _value ; 
}
}
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to greater then "0.7.0" and less than "0.9.0" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mint , burn function which take two input the address of the account and amount of which which we want to mint or burn respectively  and some public variable tokenName , tokenAbbr , totalSupply . and some mapping variable balances which return uint (the balance ) with associate account. 

## Authors

sanjay


## License

The code is released under the GNU General Public License v3.0.
