# MetaAssignmentSolidity
/*MyToken is a simple ERC20-like token implemented in Solidity. This smart contract allows users to mint and burn tokens, keeping track of the total supply and individual balances. The contract provides basic functionalities needed for a token on the Ethereum blockchain, including minting new tokens and burning existing ones.*/

/*Contract Details
Public Variables
tokenName: Stores the name of the token. In this contract, the token name is "Meta".
tokenAbbrv: Stores the abbreviation of the token. In this contract, the abbreviation is "Mta".
totalSupply: Tracks the total supply of the token in circulation. Initially set to 0.
Mapping
balances: A public mapping that associates each address with its token balance. This allows the contract to keep track of how many tokens each address holds.
Functions*/
mint
solidity
function mint(address _address, uint256 _value) public
Purpose: Creates new tokens and assigns them to a specified address.
Parameters:
_address: The address that will receive the newly minted tokens.
_value: The amount of tokens to be minted.
Functionality:
Increases totalSupply by _value.
Increases the balance of _address by _value.
burn
solidity

function burn(address _address, uint256 _value) public
Purpose: Destroys tokens, reducing both the total supply and the balance of a specified address.
Parameters:
_address: The address from which the tokens will be burned.
_value: The amount of tokens to be burned.
Functionality:
Checks if _address has at least _value tokens.
If the balance check passes, decreases totalSupply by _value.
Decreases the balance of _address by _value.
Usage
Minting Tokens
To mint tokens, call the mint function with the recipient's address and the number of tokens to mint. For example:

solidity

myToken.mint(0x1234..., 100);
This call will:

Increase the totalSupply by 100.
Increase the balance of the address 0x1234... by 100.
Burning Tokens
To burn tokens, call the burn function with the address holding the tokens and the number of tokens to burn. For example:

solidity

myToken.burn(0x1234..., 50);
This call will:

Check if 0x1234... has at least 50 tokens.
If the check passes, decrease the totalSupply by 50.
Decrease the balance of 0x1234... by 50.
Conclusion
MyToken provides a basic implementation of a token with minting and burning capabilities. This contract can serve as a foundation for more complex token functionality or as an educational tool for learning about token contracts on the Ethereum blockchain.

This README.md file provides an overview of the contract, details about its public variables and functions, and examples of how to use the mint and burn functions. This should help users understand what the contract does and how to interact with it.
