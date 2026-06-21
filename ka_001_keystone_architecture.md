---
id: KA-001
title: Keystone Architecture
version: 1.0
status: active
category: architecture
owner: project_keystone
created: 2026-06-21
last_updated: 2026-06-21
depends_on:
  - PK-001
  - STD-000
  - ADR-001
provides:
  - keystone_architecture
supersedes: []
superseded_by: []
tags:
  - architecture
  - knowledge_architecture
  - decision_engine
---

# KA-001 | Keystone Architecture

## Purpose

This artifact defines the structural architecture of Project Keystone: its two complementary
systems, how they relate, and how authority flows between them. It does not define
governance (see STD-000 through STD-003) and does not define implementation detail (see
SPEC-tier artifacts). It defines structure, components, relationships, constraints, and
evolution.

This is the first KA-tier artifact in the repository, authorized by PK-001's founding
principle and following the taxonomy defined in STD-000.

## The Two Systems

Project Keystone consists of two complementary systems, first articulated in Architecture
Plate AP-001.

### 1. Knowledge Architecture

Knowledge is hierarchical and governed. It accumulates through deliberate promotion, not
accumulation by default.

The Knowledge Repository contains, in ascending order of conceptual permanence:

```text
Kernel → Standards → Capabilities → Specifications → Playbooks → Case Studies
```

This is consistent with, and governed by, the artifact taxonomy in STD-000. The Kernel (KK)
sits at the top of conceptual authority but is populated last in practice — Keystone has
built Standards before Kernel, which is intentional: governance must exist before the
principles it protects can be safely declared immutable.

### 2. Executive Decision Engine

Executive decision-making is adaptive and iterative, not hierarchical. It is triggered by
events, not scheduled by calendar.

AP-001 describes this engine as a nine-stage process:

```text
Trigger Detection → Decision Qualification → Reality Construction → Future Simulation →
Tradeoff Evaluation → Decision Commitment → Communication → Execution → Learning
```

ADR-001 establishes that `standards/keystone.md` ("Run Keystone") is the operational
implementation of this Engine's middle five stages — Decision Qualification through
Communication — with Trigger Detection and Execution remaining outside Run Keystone's current
scope. Decision Commitment carries a mandatory bias check, guarding specifically against
personal or career interest distorting judgment at the point of commitment.

## Relationship Between the Two Systems

Knowledge Architecture and the Executive Decision Engine are complementary, not redundant.

- The Decision Engine consumes Knowledge Architecture as input — at Future Simulation
  (Run Keystone Step 4, Build Mental Models), real decisions draw on existing Standards,
  Capabilities, and Specifications rather than reasoning from scratch each time.
- The Decision Engine produces Knowledge Architecture as output — at Learning (Run Keystone
  Step 8, Promote Learning), a reusable pattern discovered during a real decision is promoted
  into the Knowledge Repository, following STD-003's contribution process.

This is the same relationship the Founding Principle (PK-001) describes for innovation,
adoption, and monetization: each system feeds and is fed by the other. Knowledge without
decisions to apply it to is inert. Decisions without accumulated knowledge to draw on are
reinvented from zero every time.

## Constraints

- No artifact in the Knowledge Repository may contradict PK-001's Founding Principle.
- The Executive Decision Engine's nine stages are conceptual and canonical, per ADR-001;
  `standards/keystone.md` is its current operational expression for the middle five stages,
  not a separate or competing engine.
- Architecture Plates (visual artifacts under `assets/architecture_plates/`) carry the same
  architectural authority as written KA-tier documents, per the Engineering Log's
  "Architecture Plates" decision — AP-001's content is binding, not merely illustrative.
- Trigger Detection and Execution are acknowledged gaps in current operational tooling. They
  may be specified later as separate SPEC or PLAY artifacts once a real need for them shows
  up twice, per the Repository Growth Rule — they are not to be added speculatively now.

## Status

Active. This artifact incorporates ADR-001's resolution of the Run Keystone / Decision Engine
mapping and is no longer blocked on an open architectural question.
