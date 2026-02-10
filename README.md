# initia-protocol
Smart contracts and dApp for the Initia micro-action token.
# Initia Protocol

Initia is a lean, bootstrap-first impact token built on a low-gas Layer-2 chain. It mints new tokens only when users perform verifiable “micro-actions” and receive peer approval. Initia’s design ensures every token in circulation directly represents a meaningful contribution.

---

##  Overview

- **Token:** `InitiaToken` (symbol: `INITIA`), ERC-20  
- **Total Supply:** Capped at launch via bonding curve  
- **Bootstrap Pool:** Small initial allocation for early adopters/partners  
- **Bonding Curve:** Holds ~99 % of supply; mints as users buy in

##  Architecture

1. **InitiaToken (ERC-20)**  
   - Standard mint/burn/transfer functionality  
   - `onlyOwner` minting restricted to ClaimManager

2. **ClaimManager**  
   - Users call `submitClaim(proofUrl)` on-chain  
   - Peers vote via `voteClaim(claimId)` (requires 3 yes-votes)  
   - After voting period (2 days), anyone calls `executeClaim(claimId)`  
     → mints a fixed reward (e.g. 10 INITIA) to the claimer

3. **Governance (Phase 3+)**  
   - On-chain proposals & voting (snapshot + simple majority)  
   - Reputation tracking via optional stake/slashing per claim

---

##  Getting Started

### 1. Prerequisites

- Node.js & npm  
- Hardhat  
- A Layer-2 RPC endpoint (e.g. Optimism, Base)  
- A funded deployer wallet (testnet or mainnet)

### 2. Installation

```bash
git clone https://github.com/<your-username>/initia-protocol.git
cd initia-protocol
npm install ```


## Protocol Status

- Initia Protocol v1 is declared **frozen**
- See: [v1 Frozen Declaration](docs/v1-frozen-declaration.md)
