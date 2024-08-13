# Glossary

### Annual Percentage Yield (APY)

The real rate of return earned on an investment over a year, taking into account the effect of compounding interest. In the context of EASP, APY reflects the potential growth of EUTO through automatic staking and compounding.

### Auto Compounding

A feature within EASP that automatically reinvests staking rewards at regular intervals, leading to exponential growth in token holdings without requiring manual intervention from the user.

### Auto Rebase

A mechanism that automatically adjusts the total supply of EUTO periodically based on the protocol's reward yield. This ensures the consistent distribution of rewards and maintains the desired supply dynamics.

### Approval

A function in ERC20-compliant tokens that allows a token holder to approve another address to spend a specified amount of tokens on their behalf.

### Elastic Supply Stability Reserve (ESSR)

A financial reserve in the Eutopia ecosystem funded by transaction fees. ESSR acts as a buffer to stabilize the token's supply and price, particularly during periods of market volatility.

### Epoch

A fixed period used by the protocol to determine when rebase operations and reward distributions occur. In EASP, an epoch typically lasts 15 minutes.

### ERC20

A widely-used standard for creating fungible tokens on the Ethereum blockchain. EUTO is an ERC20-compliant token, meaning it adheres to this standard for interoperability with other Ethereum-based platforms and services.

### EUTO

The native cryptocurrency of the Eutopia ecosystem, used within the EASP for staking, earning rewards, and participating in governance. It’s an ERC20 token with auto-compounding and auto-rebase features.

### Eutopia Autostaking Protocol (EASP)

A decentralized financial protocol that simplifies staking by automatically staking and compounding EUTO within users’ wallets. It aims to provide high, consistent APYs and streamline the user experience.

### Fee-on-Transfer

A mechanism where a fee is deducted from every transaction involving the token, with the collected fees typically directed towards the ESSR, liquidity pools, or treasury.

### Gon Balances

A technical term used within the Eutopia smart contract to manage token balances in a way that facilitates efficient rebasing. Gons represent the smallest indivisible units of EUTO tokens.

### Initializable

A pattern used in upgradeable smart contracts that defers initialization logic until the contract is deployed and set up. This approach is crucial in contracts that use OpenZeppelin’s upgradeable libraries.

### Liquidity Pool

A pool of tokens locked in a smart contract that facilitates trading on decentralized exchanges like Uniswap. In EASP, liquidity pools are critical for maintaining market stability and enabling seamless trades.

### Manual Rebase

A feature allowing the contract owner to trigger a rebase operation manually, outside of the auto-rebase schedule. This can be used to adjust the token supply in response to specific market conditions.

### Minting

The process of creating new tokens and adding them to the total supply. In traditional tokens, minting is done manually or based on specific criteria, but in EASP, the concept of minting is integrated into the auto-rebase mechanism.

### Rebase

A process that adjusts the total supply of tokens in a user’s wallet proportionally to all holders. In the context of EASP, rebasing is used to automatically distribute rewards and manage the token supply.

### Reentrancy Guard

A security mechanism used to prevent reentrancy attacks, where a malicious contract repeatedly calls a function before the previous execution is completed, potentially leading to unexpected behavior or theft of funds.

### Swap and Liquify

A process where tokens held by the contract are swapped for ETH (or another asset) and added to a liquidity pool. This function helps maintain liquidity and supports the stability of the token’s price.

### Treasury

A designated address or pool of funds within the Eutopia ecosystem that collects fees and other revenues. The treasury is used to support the ongoing development, marketing, and stability of the protocol.

### Uniswap V2

A decentralized exchange protocol on the Ethereum blockchain that allows users to trade ERC20 tokens directly from their wallets. Eutopia integrates with Uniswap V2 to manage liquidity and enable trading of EUTO.

### Upgradeable Contract

A smart contract designed to be modified or upgraded without losing its state or requiring a complete redeployment. This flexibility allows the Eutopia contract to adapt to new requirements or improvements over time.
