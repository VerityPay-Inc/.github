<div align="center">
  <img src="Verity Logo.png" alt="Organization Banner" />
</div>

# Verity

> **Open specification infrastructure for verifiable digital interactions.**

Verity is an ecosystem of repositories with a single responsibility each: define protocol meaning, validate the corpus, execute reference semantics, and compare independent implementations honestly.

We believe protocols should outlive products, specifications should precede implementation, and interoperability should emerge from shared standards—not shared vendors.

---

## Our Mission

Our mission is to build public infrastructure that makes digital interactions more transparent, verifiable, and interoperable.

Rather than creating closed platforms, we create open specifications and the **platform tooling** that keeps them coherent, executable, and testable—so independent implementations can converge on the same behavior.

---

## Current Platform Status

| Repository | Role | Status |
|------------|------|--------|
| [**veritypay-spec**](https://github.com/VerityPay-Inc/veritypay-spec) | Specification foundation — normative protocol meaning | **Specification Foundation** |
| [**veritypay-tooling**](https://github.com/VerityPay-Inc/veritypay-tooling) | Validation — registries, cross-references, Edition manifests | **Validation Platform Ready** |
| [**veritypay-reference**](https://github.com/VerityPay-Inc/veritypay-reference) | Reference interpreter — executable oracle for verification | **Reference Interpreter Ready** |
| [**veritypay-conformance**](https://github.com/VerityPay-Inc/veritypay-conformance) | Conformance suite — VP-CS scenarios vs reference outcomes | **Conformance Platform Ready** |

Each repository has **one primary job**. Together they form the **Verity Specification Platform**.

**Current platform release:** **[Platform 1.2](https://github.com/VerityPay-Inc/veritypay-spec/blob/main/PLATFORM_RELEASES.md)** — extends Platform 1.1 with accepted **VP-RFC-0003** and **VP-RFC-0004**. **Verity Platform 1.0** names the first coordinated engineering baseline (validation, reference execution, conformance harness). Phase II (**Engineering Platform**) is complete. Draft **Platform 1.3** engineering work (`normalized_text`, VP-CS-0011–0013) is in progress atop Platform 1.2; normative acceptance of **VP-RFC-0011** remains pending.

For compatible repository baselines, see [PLATFORM_RELEASES.md](https://github.com/VerityPay-Inc/veritypay-spec/blob/main/PLATFORM_RELEASES.md) in `veritypay-spec`.

---

## Platform Architecture

Four repositories. One pipeline. No entangled responsibilities.

```text
┌─────────────────────────────────────────────────────────────┐
│                     veritypay-spec                          │
│  Normative protocol · VP-CS meaning · governance & RFCs    │
└───────────────────────────┬─────────────────────────────────┘
                            │ authoritative corpus
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                   veritypay-tooling                         │
│  vp validate · registry & edition checks                   │
└───────────────────────────┬─────────────────────────────────┘
                            │ validated specification input
                            ▼
┌─────────────────────────────────────────────────────────────┐
│                     vp-spec-model                           │
│  Typed registries · document corpus · reference graph      │
└───────────────────────────┬─────────────────────────────────┘
                            │
              ┌─────────────┴─────────────┐
              ▼                           ▼
┌─────────────────────────┐   ┌─────────────────────────────┐
│   veritypay-reference   │   │   veritypay-conformance   │
│   Reference oracle      │   │   VP-CS harness           │
│   Interpreter::evaluate │   │   load · run · compare    │
└────────────┬────────────┘   └──────────────┬──────────────┘
             │                               │
             └───────────┬───────────────────┘
                         ▼
              Independent implementations
              (adapters · products · CI)
```

**Flow:** Spec defines meaning → Tooling proves the corpus is coherent → Reference produces expected outcomes → Conformance compares implementations to that oracle.

Specifications define behavior. Implementations demonstrate behavior. Conformance proves behavior.

---

## Current Phase

| Phase | Name | Status |
|-------|------|--------|
| **I** | Specification Foundation | ✅ Complete |
| **II** | Engineering Platform | ✅ Complete |
| **III** | Protocol Expansion | 🚧 **Current** |
| **IV** | Independent Implementations | ⏳ Planned |
| **V** | Ecosystem & Adoption | ⏳ Planned |

Phase I established normative architecture, governance, and the specification corpus. Phase II delivered the **engineering platform**: validated spec input, a reference interpreter, and a runnable conformance harness that consumes specification-published VP-CS scenarios. **Platform 1.0** names that complete baseline.

Phase III **expands the protocol** on top of Platform 1.0—normative claim and evidence semantics, verification rules, and VP-CS coverage grounded in accepted RFCs. The platform architecture exists; the work now is growing what the protocol means and proving it across implementations.

See [SPECIFICATION_STATUS.md](https://github.com/VerityPay-Inc/veritypay-spec/blob/main/SPECIFICATION_STATUS.md) for specification maturity detail and [PLATFORM_RELEASES.md](https://github.com/VerityPay-Inc/veritypay-spec/blob/main/PLATFORM_RELEASES.md) for official compatibility across repositories.

---

## Next Priorities

- **Accept draft protocol RFCs** — move semantics such as **`normalized_text`** ([VP-RFC-0011](https://github.com/VerityPay-Inc/veritypay-spec/blob/main/rfcs/0011-normalized-text-assertion.md)) and assertion taxonomy ([VP-RFC-0005](https://github.com/VerityPay-Inc/veritypay-spec/blob/main/rfcs/0005-assertion-types.md)) toward governed acceptance
- **Expand verification rules** — additional VP-RULE coverage in `veritypay-reference` as RFCs land
- **Grow VP-CS catalog** — normative scenarios authored in `veritypay-spec`, executed by `veritypay-conformance`
- **Deepen claim and evidence models** — align [DATA_MODEL.md](https://github.com/VerityPay-Inc/veritypay-spec/blob/main/docs/01-architecture/DATA_MODEL.md) with accepted protocol semantics
- **Prepare for independent implementations** — adapters, self-attestation, and cross-vendor testing paths (Phase IV)

---

## Engineering Philosophy

```text
Research
   ↓
Specification
   ↓
Validation
   ↓
Implementation
   ↓
Conformance
   ↓
Community
```

We optimize for:

- Clarity over cleverness
- Standards over products
- Evidence over assumptions
- Interoperability over lock-in
- Long-term maintainability over short-term velocity

Protocol changes begin with **RFCs** in `veritypay-spec`. Engineering decisions are recorded through **ADRs** in each repository.

---

## Contributing

We welcome contributors interested in protocol design, documentation, validation tooling, reference semantics, conformance harnesses, and developer experience.

**Start here:**

1. [veritypay-spec](https://github.com/VerityPay-Inc/veritypay-spec) — read `CONTRIBUTING.md`, `SPECIFICATION_STATUS.md`, and [PLATFORM_RELEASES.md](https://github.com/VerityPay-Inc/veritypay-spec/blob/main/PLATFORM_RELEASES.md)
2. [ECOSYSTEM.md](https://github.com/VerityPay-Inc/veritypay-spec/blob/main/ECOSYSTEM.md) — role-specific reading order
3. [VP-RFC-0000](https://github.com/VerityPay-Inc/veritypay-spec/blob/main/rfcs/0000-rfc-process.md) — how protocol changes are proposed
4. Sibling repo `ROADMAP.md` — capability milestones for tooling, reference, and conformance

---

## Why Open?

Open specifications create stronger ecosystems than closed implementations.

Independent implementations strengthen interoperability.

Transparent governance strengthens trust.

Public engineering creates durable infrastructure.

---

## Build With Us

If you believe specifications should be public, platforms should be composable, and conformance should be honest—we'd love to build with you.
