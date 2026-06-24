---
id: PLAY-002
title: Real-Time Metric Capture & Attribution Ledger
version: 0.1
status: active
category: playbook
owner: JET
created: 2026-06-24
last_modified: 2026-06-24
depends_on: []
provides:
  - play_metric_capture_attribution_ledger
supersedes: []
superseded_by: []
tags:
  - playbook
  - governance
  - metrics
  - attribution
  - career
---

# PLAY-002: Real-Time Metric Capture & Attribution Ledger

**Tier:** PLAY

## Purpose

JET has repeatedly identified, after leaving a role, that a metric improvement he drove was
never captured with enough rigor to survive scrutiny later — baseline lost, no saved snapshot,
no third-party corroboration, nothing but recollection. This pattern recurs across Curve
Dental, Checkmate, Qu POS, and PAR Technology, with PAR being the extreme case (four years,
zero captured metrics, narrative only). This playbook exists to prevent the pattern from
recurring at any future employer by making capture a real-time habit rather than a
retrospective reconstruction exercise.

## The Three-Layer Mechanism

### Layer 1 — Capture (at initiation, not after results land)
For every initiative where JET has real influence over outcome, open a log entry **before**
changing anything:
- Date opened
- Initiative description
- Baseline metric, with a **snapshot saved outside company systems** (export, screenshot,
  or report link saved to JET's own Drive/Notion) — system access is lost on departure, so
  the proof must live somewhere JET still controls after leaving
- Stakeholders involved (manager, peer, anyone who could later corroborate this wasn't
  solo-attributed work)
- Stated hypothesis/target, captured *before* the outcome is known — this is what makes the
  eventual result provable as caused by the initiative, not a retroactive story

### Layer 2 — Audit (fixed cadence, not "whenever remembered")
A short recurring pass — biweekly or monthly — through all open log entries:
- Has the baseline changed since the entry was opened?
- Is there a new snapshot to capture?
- Is the entry still accurate and current?
This is the step that has historically been skipped, and the direct cause of the gap this
playbook exists to close.

### Layer 3 — Credit (attribution proof captured concurrently, not separately)
Every entry includes a corroboration field — a dated, external artifact showing someone else
recognized the change as JET's: a Slack message, a one-line email, a meeting note, a
manager's comment. This is what converts "I improved forecast accuracy" into a claim that
holds up under questioning years later, consistent with Keystone's existing "true, useful,
durable, original" artifact standard and honesty-flag requirement.

## Entry Template

```
- Date opened:
- Initiative:
- Baseline (snapshot saved at):
- Stakeholders involved:
- Hypothesis/target:
- Result (snapshot saved at):
- Corroboration (who/what, dated):
- Honesty flag: [measured | estimated | recalled]
```

## Constraints

- This playbook governs *capture discipline going forward* — it does not retroactively fix
  gaps in existing CASE artifacts (e.g., CASE-006's open gaps). Those remain flagged as gaps
  pending JET's direct account, per existing practice.
- Snapshots and corroboration artifacts must be stored outside the employer's systems from
  day one of capture — waiting until departure is too late, as system access is typically
  revoked immediately.
- This playbook does not specify a tool or UI — that is an open implementation question,
  deliberately left flexible so JET can fit it to whatever tool is most natural to his daily
  workflow (dictation-based capture, visual review, etc.).

## Relationship to Existing Tools

This playbook is upstream of the case-study pipeline: a well-maintained ledger entry should
make drafting a future CASE artifact (per STD-003 contribution format) substantially faster
and higher-fidelity than reconstructing the same initiative from memory months or years later.

## Approval History

| Version | Date       | Reviewer | Status | Notes |
| ------- | ---------- | -------- | ------ | ----- |
| 0.1     | 2026-06-24 | JET      | Approved | Motivated directly by recurring capture gaps across Curve Dental, Checkmate, Qu POS, and PAR Technology. Tool/UI implementation deliberately left open as a follow-on decision. |
