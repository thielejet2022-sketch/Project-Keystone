---
id: STD-000
title: Repository Artifact Classification Standard
version: 0.2
status: draft
category: standard
owner: project_keystone
created: 2026-06-20
last_updated: 2026-06-21
depends_on: []
provides:
  - artifact_classification
supersedes: []
superseded_by: []
tags:
  - governance
  - repository
  - standards
  - taxonomy
---

# STD-000 | Repository Artifact Classification Standard

## Purpose

This standard establishes the official taxonomy of artifacts used throughout Project Keystone.

Every authoritative artifact created within the repository shall belong to one and only one primary artifact classification defined by this standard.

The purpose of artifact classification is to provide a consistent architectural language, clarify the role of every document, and ensure that repository growth remains intentional rather than organic.

---

# Design Philosophy

Project Keystone is an Executive Decision Architecture.

Its artifacts represent different levels of abstraction, authority, and permanence.

An artifact's classification communicates:

- Why it exists
- How it evolves
- How authoritative it is
- How it relates to other artifacts
- Who should consume it

Artifact classification is independent of folder structure.

Artifacts are organized by architectural purpose rather than storage location.

---

# Artifact Taxonomy

## STD | Standards

Repository governance, conventions, and operating rules.

Standards define how Keystone itself operates.

### Characteristics

- Rarely changed
- Highly authoritative
- Repository-wide applicability

### Examples

- Metadata Standard
- Repository Change Management Standard
- Markdown Style Standard

---

## ADR | Architecture Decision Records

Permanent record of significant architectural decisions.

ADRs capture **why** architectural decisions were made.

### Characteristics

- Immutable after acceptance
- Historical record
- May be superseded, never edited

### Examples

- Executive Decision Engine
- Trigger Events
- Knowledge Architecture Separation

---

## KA | Keystone Architecture

Defines the structural architecture of Project Keystone.

Architecture explains relationships between major components.

### Characteristics

- Evolves deliberately
- Highly authoritative
- References Standards and ADRs

---

## KK | Keystone Kernel

Defines immutable principles and executive laws.

The Kernel provides the philosophical foundation for every capability.

### Characteristics

- Changes infrequently
- Highest conceptual authority
- Technology independent

---

## CAP | Capabilities

Defines major executive capabilities delivered by Keystone.

Capabilities describe what Keystone enables executives to accomplish.

### Examples

- AI Monetization
- Pricing Strategy
- Executive Dashboard Design
- Decision Confidence

---

## SPEC | Specifications

Detailed implementation guidance supporting a capability.

Specifications translate architecture into repeatable execution.

### Characteristics

- Detailed
- Practical
- Frequently referenced

---

## PLAY | Playbooks

Operational guidance.

Playbooks describe repeatable methods used to execute a specification.

### Examples

- Executive Pricing Workshop
- Packaging Design Session
- Board Presentation Framework

---

## CASE | Case Studies

Applied examples demonstrating Keystone principles in practice.

Case Studies validate architecture through real-world application.

### Examples

- ServiceNow
- Microsoft Copilot
- Snowflake
- Salesforce Agentforce

---

## FRAME | Frameworks

Reusable strategic frameworks, mental models, and decision tools distilled from patterns
observed across two or more Case Studies.

Frameworks generalize a recurring pattern of executive decision-making into a portable
tool — independent of any single case, brand, or employer — that can be applied forward to
new, not-yet-encountered decisions.

A Framework is distinct from a Capability: a Capability describes *what* Keystone enables an
executive to accomplish in a domain; a Framework is a specific, reusable *tool* for reasoning
through a recurring class of decision, regardless of domain.

### Characteristics

- Bottom-up: emerges from repeated patterns in Case Studies, not designed top-down
- Requires at least two independent Case Studies exhibiting the same underlying pattern
  before formalization, per the Repository Growth Rule
- Portable across domains, brands, and employers
- Evolves as new cases either confirm, extend, or complicate the pattern

### Examples

- Bounded Lever Realignment (a single, cost-bounded lever resolves a multi-stakeholder
  tradeoff rather than trading competing interests against one another)

---

## LAB | Laboratory Notes

Working exploration.

Laboratory artifacts capture discovery, experimentation, and architectural exploration.

LAB artifacts are intentionally non-authoritative.

Ideas mature within the Laboratory before becoming formal Keystone artifacts.

---

# Artifact Relationships

Repository artifacts generally mature through the following progression.

```text
LAB
↓
ADR
↓
KA
↓
KK
↓
CAP
↓
SPEC
↓
PLAY
↓
CASE
↓
FRAME
```

Not every artifact follows every stage.

The progression represents the normal evolution of architectural maturity. FRAME is the one
tier that matures in reverse relative to the others — it is synthesized upward out of two or
more CASE artifacts that independently exhibit the same pattern, rather than being authored
top-down and then applied. A FRAME may, once mature, go on to inform new CAP or SPEC
artifacts — closing the loop from applied practice back into architecture.

---

# Authority Hierarchy

When conflicts occur, the following order of precedence applies.

1. Standards
2. Keystone Architecture
3. Keystone Kernel
4. Architecture Decision Records
5. Capabilities
6. Specifications
7. Playbooks
8. Case Studies
9. Frameworks
10. Laboratory Notes

Higher-order artifacts govern lower-order artifacts.

Lower-order artifacts may never contradict higher-order artifacts.

A Framework's authority is bounded by the Case Studies it was derived from: it may not claim
broader applicability than its source cases actually support, and must be revisited if a new
case contradicts it.

---

# Classification Rules

Every authoritative artifact shall:

- Declare exactly one primary classification
- Follow the metadata requirements defined by STD-001
- Follow the repository governance defined by STD-002
- Reference dependencies where applicable

---

# Repository Philosophy

Project Keystone is not a document repository.

It is an evolving Executive Decision Architecture.

Artifact classification exists to preserve conceptual integrity as the repository grows.

A clear architectural taxonomy enables Keystone to remain understandable, maintainable, and extensible for future contributors.

---

# Approval History

| Version | Date       | Reviewer | Status   | Notes |
| ------- | ---------- | -------- | -------- | ----- |
| 0.1     | 2026-06-20 | JET      | Approved | Initial taxonomy: STD, ADR, KA, KK, CAP, SPEC, PLAY, CASE, LAB. |
| 0.2     | 2026-06-21 | JET      | Approved | Added FRAME tier to formalize reusable frameworks distilled from two or more Case Studies, per explicit request when building the first such artifact (FRAME-001). Updated maturity progression and authority hierarchy accordingly. |
