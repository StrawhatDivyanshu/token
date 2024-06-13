MyToken is a simple ERC-20-like smart contract written in Solidity. This contract allows users to mint and burn tokens, managing their total supply and individual balances. It includes essential functionalities such as minting new tokens to an address, burning tokens from an address, and maintaining a record of token balances.

Features
Public Variables:

name: Stores the token name.
symbol: Stores the token abbreviation.
totalSupply: Stores the total supply of the token.
Mapping:

balances: Maps addresses to their respective token balances.
Minting:

The mint function increases the total supply and the balance of a specified address.
Burning:

The burn function decreases the total supply and the balance of a specified address.
Events:

Transfer: Logs minting and burning actions for transparency.
