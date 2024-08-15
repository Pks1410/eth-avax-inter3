# eth-avax-inter3
This smart contract implements an ERC20 token named "Prakhar" with the symbol "PKS" using Solidity. It extends the OpenZeppelin ERC20 and Ownable contracts.

Minting: The contract owner can mint new tokens using the mint(address to, uint256 amount) function.
Burning: Users can burn their own tokens with the burn(uint256 amount) function.
Transferring: Tokens can be transferred between addresses using the transferTokens(address recipient, uint256 amount) function.
