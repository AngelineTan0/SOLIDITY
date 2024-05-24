MyToken Smart Contract
Overview
MyToken is a simple ERC-20 compatible smart contract implemented in Solidity. This contract allows for minting and burning of tokens, maintaining a total supply, and keeping track of balances for each address. The token is named "ANGELINE" with the abbreviation "ANG".

Contract Details
Variables
tokenName: A string representing the name of the token. Set to "ANGELINE".
tokenAbbrv: A string representing the abbreviation of the token. Set to "ANG".
totalSupply: An unsigned integer representing the total supply of the tokens.
balances: A mapping that keeps track of the balances of each address.
Functions
mint
function mint(address _address, uint _value) public
Increases the total supply of the token and adds the specified amount to the balance of the given address.

Parameters:
_address: The address to which the tokens will be minted.
_value: The amount of tokens to mint.
burn
function burn(address _address, uint _value) public
Decreases the total supply of the token and subtracts the specified amount from the balance of the given address, provided the address has enough balance.

Parameters:
_address: The address from which the tokens will be burned.
_value: The amount of tokens to burn.
Usage
Deploying the Contract
To deploy the MyToken contract, follow these steps:

Open your preferred Solidity development environment (e.g., Remix).
Copy the MyToken contract code into a new Solidity file.
Compile the contract.
Deploy the contract to your desired Ethereum network.
Interacting with the Contract
After deploying the contract, you can interact with it using the functions provided:

Mint Tokens: Call the mint function with the desired address and amount of tokens to increase the balance and total supply.
Burn Tokens: Call the burn function with the desired address and amount of tokens to decrease the balance and total supply, ensuring the address has sufficient balance to burn.
Example
Here is an example of how you can interact with the deployed contract:

1. Minting 100 tokens to an address (0x123...):
MyToken.mint("0x123...", 100);
2. Burning 50 tokens from an address (0x123...):
MyToken.burn("0x123...", 50);

