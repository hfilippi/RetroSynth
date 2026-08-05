# 🏛️ Architecture Decision Records (ADR)

> Architecture is the set of decisions that are difficult to change.

---

## Purpose

Architecture Decision Records (ADR) document the significant architectural decisions made throughout the RetroSynth Project.

Each ADR captures:

- the context that led to the decision;
- the decision itself;
- the expected consequences;
- the alternatives that were evaluated.

The objective is to preserve the reasoning behind architectural choices so that future contributors understand not only *what* was decided, but also *why*.

---

## Lifecycle

Each ADR follows one of the following states:

| Status | Description |
|----------|-------------|
| Draft | Under discussion |
| Proposed | Awaiting approval |
| Accepted | Official project decision |
| Deprecated | No longer recommended |
| Superseded | Replaced by another ADR |

---

## Naming Convention

```
ADR-XXXX-short-title.md
```

Example:

```
ADR-0001-engine-first-architecture.md
```

ADR numbers are permanent.

Numbers SHALL NEVER be reused.

---

## Index

| ADR | Title | Status |
|------|-------------------------------|----------|
| ADR-0001 | Engine First Architecture | Accepted |
| ADR-0002 | Service-Oriented Architecture | Accepted |
| ADR-0003 | Hardware Modular Architecture | Accepted |

---

## Relationships

Most ADRs are referenced by one or more RetroSynth Specification (RS) documents.

Typical relationship:

```
RS-004
     │
     ├── ADR-0001
     ├── ADR-0002
     └── ADR-0003
```

---

## Modification Policy

Accepted ADRs SHALL NOT be modified to change their architectural intent.

If an architectural decision changes, a new ADR SHALL be created.

Older ADRs remain part of the project's historical record.

---

## References

- RS-001 — Project Charter
- RS-004 — Architecture Specification

---

## Changelog

### 1.0.0

- Initial version.