---
id: ADR-001
title: Reconciling Run Keystone with the Executive Decision Engine
version: 1.0
status: active
category: architecture_decision_record
owner: project_keystone
created: 2026-06-21
last_updated: 2026-06-21
depends_on:
  - KA-001
  - PK-001
provides:
  - decision_engine_run_keystone_mapping
supersedes: []
superseded_by: []
tags:
  - adr
  - decision_engine
  - run_keystone
  - governance
---

# ADR-001 | Reconciling Run Keystone with the Executive Decision Engine

## Context

AP-001 (Architecture Plate) describes a nine-stage Executive Decision Engine. Independently,
`standards/keystone.md` ("Run Keystone") defines an eight-step operational decision protocol.
These were created in separate sessions without being reconciled, producing two documents
that appear to describe the same system with different stage counts.

This inconsistency surfaced during JD-to-Narrative Gap Analysis work (SPEC-001), where Run
Keystone was already in production use.

## Decision

The nine-stage Executive Decision Engine, as described in AP-001, is the canonical
full-lifecycle model. Run Keystone is not a competing model — it is the operational
implementation of the Engine's middle five stages: Decision Qualification through
Communication.

| Decision Engine stage | Implementation |
|---|---|
| Trigger Detection | Outside Run Keystone — signal recognition that a decision exists |
| Decision Qualification | Run Keystone Step 1 (Define the Decision), including Step 2 (Define Success) as a sub-step |
| Reality Construction | Run Keystone Step 3 (Gather Evidence) |
| Future Simulation | Run Keystone Step 4 (Build Mental Models) |
| Tradeoff Evaluation | Run Keystone Step 5 |
| Decision Commitment | Run Keystone Step 6 (Form Executive Judgment) |
| Communication | Run Keystone Step 7 (Executive Recommendation) |
| Execution | Outside Run Keystone — carried out by the executive after the recommendation |
| Learning | Run Keystone Step 8 (Promote Learning) |

Run Keystone's "Define Success" has no separate Engine-stage home; it is retained as a
sub-step of Decision Qualification rather than introducing a tenth Engine stage.

## Business Rationale

The Engine's nine-stage scope addresses two specific, well-documented executive failure
modes that an eight-step reasoning checklist alone does not:

1. **Signal blindness** — decisions are often acted on too late because no explicit stage
   exists for recognizing that a decision is needed before reasoning begins. Trigger
   Detection exists to make this stage explicit and separate from qualification.

2. **Self-interested distortion at commitment** — executives more often distort judgment at
   the point of commitment, under the pressure of career risk, ego, or sunk cost, than they
   distort the underlying facts. Decision Commitment (Run Keystone Step 6 / Form Executive
   Judgment) therefore carries a mandatory bias check: before forming judgment, explicitly
   name how the decision affects the decision-maker personally — career, reputation, prior
   public position — and assess whether that interest is distorting the recommendation that
   follows. This bias check is a required component of Step 6, not a separate stage.

## Consequences

- `standards/keystone.md` should be updated to explicitly scope itself as implementing
  Decision Qualification through Communication, and to add the mandatory bias check inside
  Step 6.
- KA-001 should reference this ADR rather than re-deriving the mapping independently.
- AP-001's nine stages remain valid and unchanged. No image revision is required for the
  stage names or count — only the written standards need updating to reflect this mapping
  and the new bias-check requirement, which is text-only and not depicted in the current
  plate.
- Future Engine-stage artifacts (Trigger Detection, Execution) may be specified later as
  separate SPEC or PLAY artifacts once a real need for them shows up twice, per the
  Repository Growth Rule.

## Status

Active. This is a final architectural decision, not a draft — per STD-000, ADRs are
immutable after acceptance and may only be superseded, never edited.
