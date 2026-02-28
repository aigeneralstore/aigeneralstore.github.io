---
layout: post
title: "Threshold Signatures: A Practical Guide"
date: 2026-02-28
category: cryptography
tags: [mpc, threshold, tss, wallet]
---

Threshold signature schemes (TSS) allow a group of parties to jointly sign messages without any single party holding the complete private key.

## Why Threshold Signatures?

Traditional key management has a fundamental problem: **single point of failure**.

- Lose the key → lose everything
- Key gets stolen → funds drained
- One person controls everything

Threshold signatures solve this by splitting the key across multiple parties.

## How It Works

```
        Key Generation
             │
    ┌────────┼────────┐
    ▼        ▼        ▼
  Party 1  Party 2  Party 3
  (share)  (share)  (share)
    │        │        │
    └────────┼────────┘
             ▼
        Combined Signature
```

**Key properties:**
- No single party ever has the full key
- Any `t-of-n` parties can sign
- Fewer than `t` parties learn nothing

## Common Schemes

| Scheme | Curve | Notes |
|--------|-------|-------|
| GG18 | Secp256k1 | Original, some attacks found |
| GG20 | Secp256k1 | Fixed GG18 issues |
| FROST | Any | Flexible, provably secure |
| BLS | BLS12-381 | Aggregate signatures |

## Use Cases

1. **Institutional Custody** - Require multiple approvers
2. **DAO Treasury** - Community-controlled funds
3. **Personal Security** - Distribute trust across devices/people

---

*The future of key management is distributed trust.*
