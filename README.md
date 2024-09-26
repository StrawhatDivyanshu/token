## Project Title
**MyToken ERC-20 Compatible Smart Contract**

## Description
The **MyToken** smart contract is written in Solidity and allows for the creation and management of a custom token. It features:
- Public variables for token details such as name, abbreviation, and total supply.
- A mapping to keep track of address balances.
- Functions for minting and burning tokens:
  - **Mint**: Increases both the total supply and the balance of a specified address.
  - **Burn**: Decreases the total supply and the balance of a specified address, with a condition to prevent burning more tokens than held.

## Getting Started

### Installing
To use the smart contract, follow these steps using **Remix IDE**:

1. **Open Remix IDE**: Visit [Remix IDE](https://remix.ethereum.org).
2. **Create a New File**: In the file explorer, create a new file named `MyToken.sol`.
3. **Copy the Contract Code**: Copy and paste the provided smart contract code into `MyToken.sol`.

### Executing the Program

#### Compile the Contract:
1. Select Solidity compiler version `0.8.18`.
2. Click the **Solidity Compiler** tab in Remix and press **Compile MyToken.sol**.

#### Deploy the Contract:
1. Go to the **Deploy & Run Transactions** tab.
2. Choose **Injected Web3** to deploy to a testnet or **JavaScript VM** for local testing.
3. Click the **Deploy** button for `MyToken`.

#### Interact with the Contract:
- After deployment, interact with the contract using the deployed contract's interface in Remix.
- To mint tokens, use the **mint** function, providing an address and a value.
- To burn tokens, use the **burn** function, providing an address and a value.

## Contract Code
```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

contract MyToken {
    // public variables here
    string public Token_Name = "Republic credits";
    string public Token_Abbrv = "RC";
    uint public Total_Supply = 0;

    // mapping variable here
    mapping(address => uint) public Balance;

    // mint function
    function Mint(address _Space, uint _Capacity) public {
        Total_Supply += _Capacity;
        Balance[_Space] += _Capacity;
    }

    // burn function
    function Burn(address _Space, uint _Capacity) public {
        if (Balance[_Space] >= _Capacity) {
            Total_Supply -= _Capacity;
            Balance[_Space] -= _Capacity;
        }
    }
}
```

## Help
For common issues:

- **Compilation Errors**: Ensure that Solidity version `0.8.18` is selected.
- **Deployment Issues**: Verify your Remix IDE environment and network settings.

For further assistance, consult the [Remix IDE documentation](https://remix-ide.readthedocs.io/en/latest/).
