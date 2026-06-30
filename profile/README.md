# Verity

> **Building open specification infrastructure for verifiable digital interactions.**

Verity is an open engineering initiative dedicated to creating durable, implementation-independent specifications that anyone can inspect, implement, and improve.

We believe protocols should outlive products, specifications should precede implementation, and interoperability should emerge from shared standards—not shared vendors.

---

# Our Mission

Our mission is to build public infrastructure that makes digital interactions more transparent, verifiable, and interoperable.

Rather than creating closed platforms, we create open specifications that enable independent implementations and long-term ecosystem growth.

Every repository in this organization contributes to that mission.

---

# The Verity Specification Platform

The Verity Specification Platform is the engineering ecosystem used to design, validate, execute, and evolve open protocol specifications.

It is composed of several independent repositories, each with a single responsibility.

| Repository | Purpose | Status |
|------------|---------|--------|
| **veritypay-spec** | Canonical VerityPay specification | 🟢 Active |
| **veritypay-tooling** | Specification validation and publication tooling | 🟡 Planned |
| **veritypay-reference** | Reference interpreter (executable specification) | ⚪ Planned |
| **veritypay-conformance** | Conformance suite and interoperability testing | ⚪ Planned |
| **veritypay-examples** | Educational examples and reference integrations | ⚪ Planned |

Future repositories may include language SDKs, documentation websites, and additional protocol specifications.

---

# Current Focus

We are currently preparing the **Genesis Edition** of the VerityPay Specification.

Current priorities include:

- Finalizing the public specification
- Building specification tooling
- Creating the reference interpreter
- Establishing automated conformance testing
- Preparing contributor-ready implementation repositories

See **SPECIFICATION_STATUS.md** inside `veritypay-spec` for current project maturity.

---

# Engineering Philosophy

Everything we build follows a simple hierarchy.

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

Specifications define behavior.

Implementations demonstrate behavior.

Conformance proves behavior.

---

# Repository Principles

Every repository has exactly one primary responsibility.

Repositories communicate through published specifications rather than hidden implementation details.

We optimize for:

- Clarity over cleverness
- Standards over products
- Evidence over assumptions
- Interoperability over lock-in
- Long-term maintainability over short-term velocity

---

# Contributing

We welcome contributors interested in:

- Protocol design
- Documentation
- Specification tooling
- Reference implementations
- Testing
- Examples
- Developer experience

Before contributing, start with:

1. `veritypay-spec`
2. `CONTRIBUTING.md`
3. `SPECIFICATION_STATUS.md`
4. `VP-RFC-0000`

Protocol changes begin with RFCs.

Engineering decisions are recorded through ADRs.

---

# Roadmap

### Phase I — Institutionalize the Specification

✅ Complete

### Phase II — Build the Specification Platform

🟡 In Progress

### Phase III — Enable Independent Implementations

⚪ Planned

### Phase IV — Ecosystem Growth

⚪ Planned

---

# Why Open?

Open specifications create stronger ecosystems than closed implementations.

Independent implementations strengthen interoperability.

Transparent governance strengthens trust.

Public engineering creates durable infrastructure.

---

# Build With Us

Verity exists to create engineering infrastructure that anyone can understand, implement, and improve.

If you believe specifications should be public, interoperable, and built to outlive their creators, we'd love to build with you.
