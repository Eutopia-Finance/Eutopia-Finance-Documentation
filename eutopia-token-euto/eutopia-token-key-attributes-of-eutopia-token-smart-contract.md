---
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Eutopia Token: Key Attributes of Eutopia Token Smart Contract

### Token Details

* Name: Eutopia
* Symbol: EUTO
* Decimals: 18 (standard for ERC20 tokens)
* Eutopia Token Smart Contract (Ethereum Mainnet): \
  [https://etherscan.io/address/0xb6551900d7fb1b51ebb29fa0143a6ebf0fb0d47f](https://etherscan.io/address/0xb6551900d7fb1b51ebb29fa0143a6ebf0fb0d47f)\
  [https://1.routescan.io/address/0xb6551900d7FB1b51ebb29FA0143a6EBf0FB0D47F](https://1.routescan.io/address/0xb6551900d7FB1b51ebb29FA0143a6EBf0FB0D47F)
* Eutopia Token Smart Contract (Ethereum Sepolia Testnet): \
  [https://sepolia.etherscan.io/address/0xb6551900d7fb1b51ebb29fa0143a6ebf0fb0d47f](https://sepolia.etherscan.io/address/0xb6551900d7fb1b51ebb29fa0143a6ebf0fb0d47f)\
  [https://11155111.testnet.routescan.io/address/0xb6551900d7FB1b51ebb29FA0143a6EBf0FB0D47F](https://11155111.testnet.routescan.io/address/0xb6551900d7FB1b51ebb29FA0143a6EBf0FB0D47F)
* Eutopia Token Smart Contract (Source): [https://github.com/Eutopia-Finance/EUTO-Token-Smart-Contract/blob/main/contracts/Eutopia.sol](https://github.com/Eutopia-Finance/EUTO-Token-Smart-Contract/blob/main/contracts/Eutopia.sol)
* Whitepaper: [Eutopia Autostaking Protocol Whitepaper](https://drive.google.com/file/d/1kM9wqKc-RoyxjGZJ1kEQDT4A3OaFWFoO/view?usp=sharing)

### Supply Details

* Total Supply: The total supply of Eutopia is defined as `INITIAL_FRAGMENTS_SUPPLY`, set to `40 * 10^8 * 10^18` tokens. This represents the upper limit of the token's supply.

### Minting and Burning

* Minting: The rebase mechanism effectively adjusts the total supply by increasing or decreasing it based on the reward yield.
* Burning: There is no explicit burn function. However, tokens sent to the `DEAD` address are effectively removed from circulation.

### Transfers and Approvals

* Transfer Function:
  * Implemented via the transfer and `transferFrom` functions, allowing token transfers between addresses.
* Approval and TransferFrom:
  * `approve` function allows a token holder to approve another address (spender) to spend tokens on their behalf.
  * `transferFrom` function allows the spender to transfer tokens from the holder's address, up to the approved amount.

### Events

* Transfer Event: Emitted in several functions (`_basicTransfer`, `_transferFrom`, `_takeFee`, etc.) to indicate the movement of tokens between addresses.
* Approval Event: Emitted in the `approve`, `increaseAllowance`, and `decreaseAllowance` functions, indicating when an approval is granted to a third party to manage tokens.

### Pausable and Upgradeable Mechanisms

* Pausable
  * The contract utilizes the `PausableUpgradeable` library, which allows the owner to pause and unpause the contract's critical operations. This means that rebase, swap, and other essential functions can be paused in case of emergencies or for maintenance, providing an additional layer of control and security.
* Upgradeable
  * The contract uses OpenZeppelin’s upgradeable libraries (`Initializable`, `ERC20Upgradeable`, `OwnableUpgradeable`, etc.) to ensure it can be upgraded without losing its state.

### Integration with Other Contracts

* Uniswap Integration:
  * The contract integrates with Uniswap through `IUniswapV2Router02` and `IUniswapV2Pair`. It interacts with Uniswap to add liquidity (`_addLiquidity`), swap tokens for ETH (`_swapTokensForETH`), and synchronize the pair state (`manualSync`).
* Treasury and Liquidity Receivers:
  * Specific addresses (`liquidityReceiver`, `treasuryReceiver`, `essrReceiver`) are designated to collect fees or manage funds during various operations.

### Security Features

* Reentrancy Guard:
  * The contract inherits from `ReentrancyGuardUpgradeable` to protect against reentrancy attacks.
* Access Control:
  * The `OwnableUpgradeable` contract provides basic access control, ensuring that only the owner can execute specific functions (e.g., setting fees, exempting addresses from fees, etc.).

### Compliance

* ERC20 Compliance:
  * The contract adheres to the ERC20 standard, implementing required functions like `totalSupply`, `balanceOf`, `transfer`, `approve`, `allowance`, and `transferFrom`. This ensures interoperability with other ERC20-compliant contracts and platforms.

This detailed breakdown covers all the essential attributes and functionalities of the Eutopia Token Smart Contract based on the provided Solidity code. It highlights the technical aspects and how they align with standard practices in the Ethereum ecosystem.
