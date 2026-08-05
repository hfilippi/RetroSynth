---
id: ADR-0001

title: Engine First Architecture

version: 1.0.0

status: Accepted

classification: Normative

language: en

owner: RetroSynth Project

maintainer: Horacio Filippi

authors:
  - Horacio Filippi

reviewers: []

approved_by: Horacio Filippi

created: 2026-08-05
updated: 2026-08-05

category: Architecture Decision Record

tags:
  - architecture
  - engine
  - modularity

related:
  - RS-004
  - ADR-0002

license: CC BY-SA 4.0
---

# 🏗️ ADR-0001 — Engine First Architecture

> **Status:** Accepted

---

# 1. Context

RetroSynth is intended to support multiple synthesis technologies while maintaining a unified operating system and user experience.

Traditional synthesizer implementations frequently embed synthesis logic directly into the application or firmware, making future expansion increasingly complex.

The project requires an architecture where synthesis engines can evolve independently without impacting the operating system.

---

# 2. Decision

RetroSynth SHALL adopt an **Engine First Architecture**.

The operating system SHALL be designed around a generic synthesis engine interface.

Individual synthesis engines SHALL implement that interface without exposing engine-specific behavior to the operating system.

The operating system SHALL remain completely agnostic regarding the internal implementation of each synthesis engine.

---

# 3. Motivation

The Engine First Architecture provides:

- modularity;
- long-term maintainability;
- engine independence;
- easier testing;
- future extensibility;
- simplified software architecture.

---

# 4. Consequences

## Positive

- New synthesis engines can be added without modifying RetroSynth OS.
- Community-developed engines become possible.
- User interface remains independent of synthesis implementation.
- Reduced coupling between subsystems.
- Easier automated testing.

## Negative

- Additional abstraction layer.
- Well-defined interfaces become mandatory.
- Engine API stability becomes critical.

---

# 5. Alternatives Considered

## Monolithic Architecture

Rejected.

Embedding synthesis logic directly into the operating system would significantly reduce extensibility.

---

## Hardware-Specific Architecture

Rejected.

Tightly coupling software to a specific chip would prevent future platform evolution.

---

## Plugin-Based Without Common Interface

Rejected.

A shared interface is required to guarantee interoperability.

---

# 6. Implementation Impact

This decision affects:

- Engine API
- Engine Manager
- Preset Manager
- Demo Manager
- Visualization System
- RetroSynth Studio

Every synthesis engine SHALL implement the common engine interface defined by RS-004.

---

# 7. Compliance Requirements

Every synthesis engine SHALL:

- expose the official Engine API;
- support lifecycle management;
- expose visualization data;
- provide patch serialization;
- support engine discovery.

Failure to satisfy these requirements means the engine SHALL NOT be considered compatible with RetroSynth OS.

---

# 8. References

- RS-004 — Architecture Specification
- ADR-0002 — Service-Oriented Architecture

---

# Changelog

## 1.0.0

- Initial version.