---
id: ADR-0002

title: Service-Oriented Architecture

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
  - services
  - modularity
  - operating-system

related:
  - RS-004
  - ADR-0001
  - ADR-0003

license: CC BY-SA 4.0
---

# ⚙️ ADR-0002 — Service-Oriented Architecture

> **Status:** Accepted

---

# 1. Context

RetroSynth OS is expected to grow over time, incorporating new capabilities such as additional synthesis engines, user interface features, communication protocols, storage backends, and hardware revisions.

A monolithic application architecture would tightly couple these responsibilities, making maintenance, testing and future expansion increasingly difficult.

The project therefore requires a modular software architecture where each subsystem performs a single responsibility and communicates through well-defined interfaces.

---

# 2. Decision

RetroSynth OS SHALL adopt a **Service-Oriented Architecture (SOA)**.

Core functionality SHALL be implemented as independent services coordinated by a central **Service Manager**.

Each service SHALL expose a stable public interface and SHALL remain independent from the implementation details of other services.

Services SHALL communicate through interfaces and the internal event system rather than direct dependencies whenever practical.

---

# 3. Service Catalog

The initial system defines the following core services:

| Service | Responsibility |
|----------|----------------|
| AudioService | Audio device management and real-time processing |
| EngineService | Discovery, loading and lifecycle of synthesis engines |
| MidiService | MIDI input, output and routing |
| PresetService | Patch loading, saving and serialization |
| DisplayService | Screen rendering and display management |
| InputService | Physical controls and touchscreen input |
| StorageService | Persistent storage management |
| DemoService | Demonstration playback |
| UpdateService | System and engine updates |

Additional services MAY be introduced in future releases without affecting existing interfaces.

---

# 4. Motivation

The Service-Oriented Architecture provides:

- clear separation of responsibilities;
- independent testing of subsystems;
- easier maintenance;
- improved scalability;
- simpler replacement of implementations;
- cleaner dependency management.

---

# 5. Consequences

## Positive

- Services can evolve independently.
- Unit testing becomes significantly easier.
- New functionality can be introduced with minimal impact.
- Platform-specific implementations remain isolated.
- Long-term maintainability improves.

## Negative

- Increased architectural complexity.
- Additional interfaces must be designed and documented.
- Startup sequence requires dependency management.

---

# 6. Service Lifecycle

Every service SHALL follow the same lifecycle.

```text
Created
    │
Initialize
    │
Running
    │
Paused
    │
Stopped
    │
Destroyed
```

The Service Manager is responsible for controlling these state transitions.

---

# 7. Dependency Rules

Services SHALL NOT create circular dependencies.

Dependencies SHALL always point toward lower-level abstractions.

Example:

```text
UI Service
     │
     ▼
Engine Service
     │
     ▼
Audio Service
```

Circular references are prohibited.

---

# 8. Event-Based Communication

Whenever possible, services SHALL communicate through the RetroSynth Event Bus.

Typical events include:

- NoteOn
- NoteOff
- PatchLoaded
- PatchSaved
- EngineChanged
- DemoStarted
- DemoStopped
- SystemBoot
- SystemShutdown

This minimizes coupling between subsystems and simplifies future expansion.

---

# 9. Threading Considerations

Each service SHALL execute in the appropriate execution context.

Typical execution model:

- UI Thread
- Audio Thread
- MIDI Thread
- Background Worker
- Storage Thread

The Audio Thread SHALL remain isolated from blocking operations.

Services interacting with the Audio Thread SHALL use lock-free communication mechanisms.

---

# 10. Implementation Impact

This decision affects:

- RetroSynth OS
- Service Manager
- Event Bus
- Thread Model
- Engine Manager
- User Interface
- Future SDK

Every subsystem introduced after this ADR SHALL be implemented either as a service or as a component owned by a service.

---

# 11. Compliance Requirements

Every service SHALL:

- expose a documented public interface;
- define a lifecycle;
- avoid circular dependencies;
- remain independently testable;
- separate interface from implementation.

Failure to comply with these principles requires an explicit superseding ADR.

---

# 12. References

- RS-004 — Architecture Specification
- ADR-0001 — Engine First Architecture
- ADR-0003 — Hardware Modular Architecture

---

# Changelog

## 1.0.0

- Initial version.