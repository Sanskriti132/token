PROJECT TITTLE : SimToken
SimToken: A Basic Token Contract for Minting and Burning

Description:SimToken is a Solidity-based smart contract developed on the Ethereum network. 
For minting and burning tokens, it offers basic functionality. Users can learn the fundamentals of token administration in a decentralized setting with the aid of this contract.

GETTING STARTED:A straightforward Solidity token contract is called SimToken. It has public variables to hold the name, abbreviation, and total quantity of tokens, among other important token data. 
A mapping to monitor each address's balance is included in the contract. Tokens can be burned to lower the total supply and balance or minted again to enhance the total supply and balance.
The contract is perfect for instructional purposes or as a basis for more intricate token systems, as it illustrates straightforward yet efficient techniques for controlling a token's lifetime on a blockchain.

INSTALLING:For ease of use, I am using the online IDE Remix.
Go to Remix:
Go to the Remix IDE after opening your browser.
Make a New File:
Press the "File Explorer" symbol.
The "+" button can be clicked to start a new file.
Give SimToken.sol file name.
Copy and Paste the Code of Contract: into SimpleToken.sol 

Executing program:Deploying,Minting,Burning
Open the Remix IDE.
Make a fresh file. SimToken.sol.
In SimToken.sol, copy and paste your contract code.
Select 0.8.0+ under the "Solidity Compiler" tab, then click "Compile."
To deploy the contract, select the "Deploy & Run Transactions" option.
To see functions, expand the deployed contract.
To add tokens, use mint; to remove tokens, use burn.
To see supply and balances, check totalSupply and balances.

1.The purpose of the contract declaration for SimToken is to establish the start of the SimToken contract.
2. Variable Token Name string public tokenName = "SimToken"; Goal: Declares a public variable with the initial value "SimToken."
Use: Holds the token's entire name and makes it readable.
The purpose of declaring a public variable tokenAbbrv initialized as "ST" is to establish a token abbreviation variable string.
Use: Holds the token's abbreviation and makes it readable.
The Total Supply Variable uint public totalSupply = 0 is declared with the intention of initializing a public unsigned integer totalSupply to 0.
Use: Maintains tabs on the overall quantity of tokens in circulation.
3. Balances Mapping; defines a public mapping balances from address to uint (mapping(address => uint) public balances).
Use: Maintains tabs on how many tokens are held by each address.
4.The purpose of the function mint is to create tokens. It is declared as mint(address _to, uint _amount) public.
Use: Increases the overall supply and adds tokens to the balance of an address.
aggregateSupply += _amount; raises aggregateSupply by _amount.
balances[_to] += _amount; This adds _amount to the balance of _to.
5.The function burn(address _from, uint _amount) public {declares a burn function that burns tokens.
Use: Decreases the overall supply and removes tokens from the balance of an address.
need(balances[_from] >= _amount, "Not enough balance to burn"); if _from does not have at least _amount tokens, an error is raised.
totalSupply -= _amount; subtracts _amount from totalSupply.
reduces the balance of _from by _amount; balances[_from] -= _amount.



HELP:Compiler Mistakes: Solidity version 0.8.18 or higher is installed on  system.

AUTHOR:Sanskriti Anand
      SANSKRITIANAND@132
LICENSE:[SimTOKEN]:Sanskriti132/token
