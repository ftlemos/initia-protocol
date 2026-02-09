# Initia Protocol v1 — Threat Model & Non-Goals

## Threat Model

This section documents anticipated threats to the Initia Protocol v1 across
technical, social, economic, and user-facing dimensions.

The objective is not to claim perfect security, but to clearly define:
- what Initia defends against,
- what is mitigated by design,
- and what is explicitly out of scope.

---

### 1. Smart Contract Threats

**Threats**
- Re-entrancy
- Integer overflow / underflow
- Unauthorized minting
- Replay attacks
- Signature forgery
- Logical errors in mint eligibility

**Mitigations**
- Minimal, audited ERC-20 primitives
- Immutable minting rules deployed once in v1
- No admin or owner-controlled mint functions
- Strict input validation and replay protection
- Deterministic mint logic

**Residual Risk**
- Undiscovered logic bugs
- Upstream dependency vulnerabilities

---

### 2. Governance Abuse

**Threats**
- Governance capture
- Bribery or collusion
- Governance-driven coercion or censorship

**Mitigations**
- Governance is **purely signaling** in v1
- No governance execution powers
- Governance cannot:
  - mint tokens
  - change parameters
  - upgrade contracts
- No upgrade hooks or admin keys

**Residual Risk**
- Off-chain actors may socially over-weight governance signals

---

### 3. Minting & Economic Attacks

**Threats**
- Sybil attacks
- Fake or duplicated identity proofs
- Claim flooding
- Speculative manipulation

**Mitigations**
- One-claim-per-identity assumption
- Deterministic mint amounts
- No discretionary minting
- Mint rules are immutable once deployed

**Residual Risk**
- Weaknesses in external identity systems
- Coordinated off-chain attacks

---

### 4. Wallet & User Security

**Threats**
- Phishing
- Malicious frontends
- Wallet malware
- Social engineering

**Mitigations**
- Protocol does not custody funds
- No approval-heavy flows
- No hidden contract calls
- Clear documentation and warnings

**Residual Risk**
- User error
- Compromised devices

---

### 5. Infrastructure & Off-Chain Threats

**Threats**
- RPC manipulation
- Indexer censorship
- Frontend downtime
- UI tampering

**Mitigations**
- On-chain contracts are canonical
- Direct contract interaction always possible
- No centralized server dependency for correctness

**Residual Risk**
- Temporary usability degradation

---

### 6. Legal & Social Threats

**Threats**
- Regulatory misclassification
- Jurisdictional pressure
- Brand impersonation or confusion

**Mitigations**
- Protocol neutrality
- No promises of profit
- Open-source transparency

**Residual Risk**
- External legal interpretation beyond protocol control

---

## Non-Goals

The following are explicitly **not goals** of Initia Protocol v1:

### 1. No Discretionary Governance
- Governance does not decide outcomes
- Governance does not control minting
- Governance does not execute changes

### 2. No Upgradeability
- Contracts are immutable
- No proxy patterns
- No emergency keys

### 3. No Custodial Features
- No fund custody
- No balance management
- No recovery mechanisms

### 4. No On-Chain Identity Resolution
- Identity verification is external
- Contracts only validate proofs, not identities

### 5. No Guaranteed Economic Outcomes
- No price guarantees
- No yield promises
- No loss protection

### 6. No Active Moderation
- No blacklists
- No account freezes
- No censorship controls

---

## Safety Notice (Non-Technical Users)

- Initia Protocol v1 is experimental software
- Blockchain transactions are irreversible
- Loss of private keys means loss of tokens
- Do not interact via untrusted websites
- Governance signals do **not** imply safety or endorsement

If you do not understand Ethereum transactions,
**do not interact directly without guidance**.

---

## Summary

Initia v1 prioritizes:
- Determinism over discretion
- Immutability over flexibility
- Neutral execution over governance power

Security is achieved through **simplicity, immutability, and minimized trust** —
not through active control.
