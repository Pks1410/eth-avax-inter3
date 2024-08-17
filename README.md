# Project Title: Create and Mint Token

# Description
This Solidity smart contract implements a simple ERC20 token called "Prakhar" with the symbol "PKS". The contract uses OpenZeppelin's ERC20 and Ownable libraries to provide standard token functionalities along with ownership control.

## Features
* Minting: The contract owner can mint new tokens to a specified address.
* Burning: Any token holder can burn their own tokens, reducing the total supply.
* Transferring: Token holders can transfer tokens to other addresses.

## Smart Contract Details
1. Constructor
```shell 
constructor() Ownable(msg.sender) ERC20('Prakhar', 'PKS') {}
```
* The constructor initializes the token with the name "Prakhar" and the symbol "PKS".
* Ownership is set to the address that deploys the contract.
2. Minting Tokens
```shell
function mint(address to, uint256 amount) public onlyOwner {
    _mint(to, amount);
}
```
* This function allows the contract owner to mint new tokens to a specified address.
* Only the contract owner can call this function.
3. Burning Tokens
```shell
function burn(uint256 amount) public {
    _burn(_msgSender(), amount);
}
```
* This function allows any token holder to burn a specified amount of their own tokens.
* This reduces the total supply of tokens.
4. Transferring Tokens
```shell
function transferTokens(address recipient, uint256 amount) public returns (bool) {
    return transfer(recipient, amount);
}
```
* This function allows token holders to transfer their tokens to another address.
* It returns true if the transfer is successful.
     

## Getting Started

### Installing

* User can clone this repository to there local system or can dowload zip file.
* User is required to install Node.js prior before executing the program.


### Executing program

1. after cloning the Repository, open first terminal and enter the commands: 

```shell
npm i
```
```shell
npm install @openzeppelin/contracts
```
2. Now open second terminal and enter the following commands to compile the contract if not compiled yet:

```shell
npx hardhat compile
```
3. Now Start the hardhat node:

```shell
npx hardhat node
```
4. Finally in the third terminal, deploy the contract on hardhat localhost, using the following command:

```shell
npx hardhat run --network localhost scripts/deploy.js
```
5. This will deploy the contract successfully.

## Help

To Understand the Hardhat commands on can use this command in terminal:


npx hardhat help


## Authors

* Name: Prakhar Sahu
* MetacrafterID: Prakhar1410 (1410sahu.prakhar@gmail.com)
* Loom Video 2nd attempt Link: https://www.loom.com/share/e9741706acd24676936ca41a8c62ca1a?sid=17878552-b6ba-43e6-9ca5-86914aaeae0c
* Loom Video 1st attempt Link: https://www.loom.com/share/8ad528a2243645a88ddcfd19d8df0d06?sid=edb788bb-2495-48af-a4aa-82525a6cc9ae



