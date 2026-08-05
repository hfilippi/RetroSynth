---
id: RS-000

slug: documentation-style-guide

title: Documentation Style Guide

version: 1.0.0

status: Draft

classification: Normative

language: en

owner: RetroSynth Project

maintainer: Horacio Filippi

authors:
  - Horacio Filippi

reviewers: []

approved_by: null

created: 2026-08-04
updated: 2026-08-04

license: CC BY-SA 4.0

category: Documentation

tags:
  - documentation
  - standards
  - process

related:
  - RS-001
---

# 🎹 RetroSynth Project

# 📚 RS-000 — Documentation Style Guide

> **Where Retro Computing Meets Modern Synthesis.**

---

| Field | Value |
|-------|-------|
| **Document ID** | RS-000 |
| **Version** | 1.0.0 |
| **Status** | Draft |
| **Classification** | Normative |
| **Language** | English |
| **License** | CC BY-SA 4.0 |

---

# 1. Introduction

Documentation is a fundamental engineering artifact within the RetroSynth Project.

It defines the project's architecture, preserves design decisions, communicates technical knowledge, and enables long-term collaboration between contributors.

Documentation is considered part of the product itself and follows the same engineering standards applied to source code.

Every document stored in the project repository SHALL comply with the rules defined by this specification unless explicitly exempted.

---

# 2. Purpose

The purpose of this document is to define a unified documentation standard for every component of the RetroSynth Project.

This standard ensures that project documentation is:

- Consistent
- Accurate
- Maintainable
- Version controlled
- Reviewable
- Searchable
- Scalable

The objective is to guarantee that documentation remains useful throughout the entire lifecycle of the project.

---

# 3. Scope

This specification applies to every document contained within the RetroSynth Project repository, including but not limited to:

- Architecture specifications
- Hardware specifications
- Software specifications
- User documentation
- Developer documentation
- Process documentation
- Governance documentation
- Architecture Decision Records (ADR)
- Templates
- Website documentation

Unless otherwise stated, every document SHALL comply with this specification.

---

# 4. Conformance Language

The key words **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **MAY**, and **OPTIONAL** in this document are to be interpreted as described in RFC 2119.

Whenever these keywords appear in a Normative document, they indicate the level of requirement intended by the author.

---

# 5. Documentation Principles

The following principles define the documentation culture of the RetroSynth Project.

## 5.1 Documentation is Part of the Product

Documentation SHALL be considered a product deliverable.

A feature is not complete until the corresponding documentation has been updated.

---

## 5.2 Documentation Before Implementation

Whenever practical, architectural decisions, interfaces, hardware designs and major features SHOULD be documented before implementation begins.

Documentation serves as the primary design artifact of the project.

---

## 5.3 Single Source of Truth

Every concept SHALL have one authoritative document.

Information SHALL NOT be duplicated unnecessarily.

Documents SHOULD reference related specifications instead of repeating existing content.

---

## 5.4 Documentation as Code

Documentation SHALL be treated with the same level of care as source code.

Every document SHALL:

- be stored in Git;
- maintain complete revision history;
- be reviewed before approval;
- follow Semantic Versioning;
- evolve together with the project.

---

## 5.5 Text First

Whenever possible, documentation assets MUST use text-based formats.

Preferred formats are:

- Markdown
- Mermaid
- SVG
- PlantUML
- Draw.io
- YAML
- JSON

Binary formats SHOULD only be used when no practical text-based alternative exists.

---

## 5.6 English as the Canonical Language

English SHALL be the canonical language of the RetroSynth Project.

Spanish SHALL be maintained as an official translation.

When discrepancies exist, the English version SHALL be considered authoritative until synchronization is completed.

---

## 5.7 Stable References

Documents SHALL reference other project documents using their permanent identifier.

Example:

```
RS-004
```

instead of

```
architecture.md
```

This guarantees stable references even if filenames or repository structures change.

---

## 5.8 Modular Documentation

Documentation SHOULD remain modular.

Large subjects SHOULD be divided into multiple focused documents rather than creating excessively large specifications.

Each document SHOULD address a single primary subject.

---

## 5.9 Evergreen Documentation

Documentation SHALL accurately describe the current state of the project.

Outdated information MUST be corrected, deprecated or archived.

Documentation SHALL evolve together with the software and hardware.

---

## 5.10 Architecture First

Engineering decisions SHOULD be documented before implementation whenever practical.

Design precedes implementation.

Implementation SHALL follow approved specifications whenever they exist.

---

# 6. Documentation Classification

RetroSynth defines two documentation classifications.

| Classification | Description |
|----------------|-------------|
| **Normative** | Defines mandatory rules, requirements, standards or specifications. Compliance is required. |
| **Informative** | Provides guidance, examples, explanations or tutorials. Compliance is not mandatory. |

Normative documents define project standards.

Informative documents support the understanding and application of those standards.