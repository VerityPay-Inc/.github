# VerityPay

**Privacy-preserving, trust-minimized payroll infrastructure** for cross-border remote work payments.

VerityPay enables employers to fund payroll **upfront** and release wages through **deterministic escrow rules**, while minimizing public exposure of salary data. Built on **Stellar** using **Trustless Work** escrow primitives, with an optional **zero-knowledge (ZK)** module for income and compliance proofs. Developed as an open-source public good with contributor funding via **Drips Network**.

---

## What VerityPay is (and isn’t)

✅ **Is**
- Open payroll rails + reference implementations
- Trust-minimized wage delivery (fund custody + release rules enforced)
- Privacy by default (minimal on-chain metadata; encrypted off-chain details)
- Modular verification (human approval, oracles, or arbitration as plug-ins)
- A contributor-first OSS project

❌ **Is not**
- An “anonymous payroll” system
- A token or speculative DeFi protocol
- A replacement for compliance providers (we integrate where needed)

---

## Repositories (Start here)

### 1) Core docs & specs (start here)
- **veritypay-core** — white paper, architecture, data model, roadmap, repo map

### 2) MVP payroll engine
- **veritypay-orchestrator** — payroll cycles, milestone schedules, state sync, API

### 3) Escrow integration
- **veritypay-escrow-adapter** — Trustless Work integration library + test harness

### 4) Minimal UI
- **veritypay-ui** — employer dashboard + worker status/claim flows

### 5) Privacy utilities
- **veritypay-privacy** — commitments, encryption formats, selective disclosure helpers

### 6) ZK research module (optional)
- **veritypay-zk** — circuits + prover/verifier reference + benchmarks

---

## MVP Scope (Phase 1)

The MVP focuses on:
- Creating payroll escrows (weekly/bi-weekly milestones)
- Funding payroll upfront with stablecoins
- Approve/dispute + release flows
- Privacy v1: commitments + encrypted off-chain payloads
- Minimal UI and API

---

## Contributing

We welcome contributions across:
- Core protocol / payroll engine
- Privacy model & cryptography utilities
- Frontend UX and design
- Documentation and diagrams
- ZK research

Start with:
- `veritypay-core/docs/CONTRIBUTING.md`
- “good first issues” in each repo

---

## Security & Responsible Disclosure

If you find a vulnerability, please open a public issue.

See: **veritypay-core/docs/SECURITY_MODEL.md**

---

## Community & Contact

- Discussions:
- Chat:
- Updates:
