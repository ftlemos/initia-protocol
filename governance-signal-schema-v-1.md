# Initia Protocol v1 — Governance Signal Format Schema

## 1. Purpose

This document defines the **standard format** for governance signals
in Initia Protocol v1.

The schema exists to:
- improve clarity,
- enable comparison,
- support archival,
- and reduce ambiguity.

Signals are **non-binding** and **off-chain**.

---

## 2. Signal Structure

Each governance signal MUST include the following fields.

### 2.1 Required Fields

#### `signal_id`
- Type: string
- Description: Unique identifier for the signal
- Example:

---

#### `signal_type`
- Type: enum
- Allowed values:
- `informational`
- `recommendation`
- `validation`
- `risk_notice`
- Description: Classifies the intent of the signal

---

#### `timestamp`
- Type: ISO 8601 datetime (UTC)
- Description: Time of signal submission
- Example:

---

#### `signal_type`
- Type: enum
- Allowed values:
- `informational`
- `recommendation`
- `validation`
- `risk_notice`
- Description: Classifies the intent of the signal

---

#### `timestamp`
- Type: ISO 8601 datetime (UTC)
- Description: Time of signal submission
- Example:

---

#### `author`
- Type: string
- Description: Pseudonymous or real identifier
- Notes:
- No identity verification required
- Wallet address optional

---

#### `summary`
- Type: string (max 280 characters)
- Description: Concise explanation of the signal

---

#### `rationale`
- Type: markdown text
- Description: Detailed reasoning behind the signal

---

### 2.2 Optional Fields

#### `supporting_data`
- Type: list of links or references
- Description: Evidence, analytics, research, or discussions

---

#### `intended_audience`
- Type: enum or string
- Examples:
- `protocol designers`
- `token holders`
- `researchers`
- `general public`

---

#### `confidence_level`
- Type: enum
- Allowed values:
- `low`
- `medium`
- `high`
- Description: Self-declared confidence of the author

---

#### `related_signals`
- Type: list of `signal_id`
- Description: References to prior signals

---

## 3. Example Signal

```yaml
signal_id: INITIA-GOV-2026-W14-002
signal_type: recommendation
timestamp: 2026-04-08T12:00:00Z
author: anonymous-holder-7f3a
summary: Consider stricter identity proof constraints in v2
rationale: |
Analysis of claim patterns suggests that certain identity proofs
may allow repeated participation. While v1 rules are immutable,
future versions could benefit from stronger uniqueness guarantees.
supporting_data:
- https://example.com/analysis-report
intended_audience: protocol designers
confidence_level: medium
