# SIMTOKEN

SimToken: A Basic Token Contract for Minting and Burning.This program  demonstrates the basic syntax and functionality of creating token in Solidity programming language. 

## DESCRIPTION

SimToken is a Solidity-based smart contract developed on the Ethereum network. 
For minting and burning tokens, it offers basic functionality. Users can learn the fundamentals of token administration in a decentralized setting with the aid of this contract.

## GETTING STARTED

A straightforward Solidity token contract is called SimToken. It has public variables to hold the name, abbreviation, and total quantity of tokens, among other important token data. 
A mapping to monitor each address's balance is included in the contract. Tokens can be burned to lower the total supply and balance or minted again to enhance the total supply and balance.
The contract is perfect for instructional purposes or as a basis for more intricate token systems, as it illustrates straightforward yet efficient techniques for controlling a token's lifetime on a blockchain.

### INSTALLING

For ease of use, I am using the online IDE Remix.
Go to Remix:
Go to the Remix IDE after opening your browser.
Make a New File:
Press the "File Explorer" symbol.
The "+" button can be clicked to start a new file.
Give SimToken.sol file name.
Copy and Paste the Code of Contract: into SimpleToken.sol 

### EXECUTING PROGRAM

Deploying,Minting,Burning
Open the Remix IDE.
Make a fresh file. SimToken.sol.
In SimToken.sol, copy and paste your contract code.
Select 0.8.0+ under the "Solidity Compiler" tab, then click "Compile."
To deploy the contract, select the "Deploy & Run Transactions" option.
To see functions, expand the deployed contract.
To add tokens, use mint; to remove tokens, use burn.
To see supply and balances, check totalSupply and balances.

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix
website and then move to contract and click SimToken https://remix.ethereum.org/#lang=en&optimize=false&runs=200&evmVersion=null&version=soljson-v0.8.26+commit.8a97fa7a.js

    contract SimToken {
    
    string public tokenName = "SimToken";
    string public tokenAbbrv = "ST";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;

    function mint(address _to, uint _amount) public {
        totalSupply += _amount;
        balances[_to] += _amount;
    }

    function burn(address _from, uint _amount) public {
        require(balances[_from] >= _amount, "Not enough balance to burn");
        totalSupply -= _amount;
        balances[_from] -= _amount;
    }
    }

## HELP
Compiler Mistakes: Solidity version 0.8.18 or higher is installed on  system.

## AUTHOR
Sanskriti Anand
SANSKRITIANAND@132

## LICENSE
[SimTOKEN]:Sanskriti132/token
