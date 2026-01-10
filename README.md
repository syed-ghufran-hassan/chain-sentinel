
# ChainSentinel

A blockchain-based security and reward system for gaming, using Chainlink VRF for provably fair random rewards.

A blockchain-based gaming reward system that uses Chainlink VRF for provably fair random rewards.

## Contracts Overview

### Core Contracts
- **ChainSentinelReward** - Main reward distribution contract using Chainlink VRF for random prize selection
- **ChainGuardGold** (ERC20) - In-game currency token with 10M initial supply
- **ChainGuardHero** (ERC721) - Unique hero NFTs with sequential minting
- **ChainGuardLoot** (ERC1155) - Multi-token loot items with metadata URI support

### Security Infrastructure
- **Timelock** - Time-delayed execution for critical administrative functions
- **EmergencyRecovery** - Multi-sig emergency recovery contract for critical situations
- **CircuitBreaker** - Automated circuit breaker for emergency operation controls
- All contracts include pause/unpause functionality and emergency withdrawal capabilities


### How It Works
1. Players pay a fee to open reward boxes through `ChainGuardReward.open()`
2. Chainlink VRF generates verifiable random numbers for fair prize selection
3. Rewards are distributed from a weighted prize pool containing ERC20, ERC721, or ERC1155 tokens
4. Contract supports refilling with additional tokens for ongoing gameplay
 