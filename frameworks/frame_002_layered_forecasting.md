---
id: FRAME-002
title: Layered Forecasting — Exit-Criteria & Behaviorally-Weighted Methodology
version: 0.1
status: draft
category: framework
owner: JET
created: 2026-06-22
last_modified: 2026-06-22
depends_on:
  - CASE-003
provides:
  - framework_layered_forecasting
supersedes: []
superseded_by: []
tags:
  - framework
  - forecasting
  - revenue-operations
  - behavioral-signals
  - rep-level-performance
---

# FRAME-002: Layered Forecasting — Exit-Criteria & Behaviorally-Weighted Methodology

**Tier:** FRAME
**Status:** Draft — derived from one committed Case Study; pattern recurrence
elsewhere is flagged but not yet documented as independent case artifacts.

## Core Insight

A forecast's accuracy ceiling is not set by effort, tooling, or how often the number gets
revisited — it's set by which layer of data the forecast actually relies on. CRM stage data
alone is structurally lagging: it tells you where a deal *was*, not where it's going. The fix
is not a better single source, but a stack of layers, each one correcting a blind spot the
layer below it cannot see — moving the underlying methodology from top-down/team-level to
bottoms-up/rep-level in the process.

## Where This Pattern Showed Up

**CASE-003 (Curve Dental / Flex Dental / Dental HQ forecast redesign):** Forecast error
averaged ±25% under a top-down, team-level model sandbagged ~20% to compensate for known
inaccuracy. Decomposing the pipeline surfaced a specific structural blind spot (sub-14-day
deals invisible to standard review). The fix layered exit-criteria checkpoints, a
weighted-forecast logic, Gong-sourced behavioral signals, and rep-level ramp/regression
models on top of the existing CRM — taking accuracy to within ±5% by the mid-month checkpoint.

**Recurred elsewhere (flagged, not yet documented):** JET recalls the same layered,
bottoms-up, behaviorally-weighted pattern showing up in forecasting work at Qu, Checkmate,
and PAR. These are not yet captured as Keystone case artifacts — referenced here as
professional pattern recognition across roles, not as independent committed evidence. Should
be written up as separate CASE artifacts if this framework is to graduate past draft
(see Limitations).

## The Pattern, Generalized

```
TOP-DOWN (legacy)                    BOTTOMS-UP (redesign)
─────────────────                    ──────────────────────

  [Team Forecast]                      [Rep A]──┐
       │                               [Rep B]──┤
       │  flat team avg                [Rep C]──┼──► [Aggregate]
       │  + "gut" inflation            [Rep D]──┤      (sum of individually
       ▼  (sandbagged ~20%)            [Rep E]──┘       modeled reps)
  Single number,                            │
  low confidence                            ▼
                                      Heterogeneity preserved
                                      (ramp curve ≠ tenured curve)


FORECAST INPUT LAYERS (stacked, not single-source)
───────────────────────────────────────────────────

  LAYER 1 — CRM STAGE DATA            (lagging by nature; structurally
            │                          blind to short-cycle deals)
            ▼
  LAYER 2 — EXIT CRITERIA             (forecast checkpoint = stage EXIT,
            │                          not entry — a tighter, fact-based gate)
            ▼
  LAYER 3 — WEIGHTED FORECAST         (deal weight = stage × size ×
            │                          behavioral signal, not flat count)
            ▼
  LAYER 4 — BEHAVIORAL INDICATORS     (activity recency, sentiment, last
            │                          contact — LEADS the CRM, doesn't lag it)
            ▼
  LAYER 5 — REP-LEVEL PERFORMANCE     (ramp model + micro-regression per
                                       rep, not a team blend)
            │
            ▼
   ┌──────────────────────┐
   │  Wide error margin →   │
   │  tight, confidence-    │
   │  validated forecast    │
   └──────────────────────┘
```

1. **Name which layer the current forecast actually relies on.** Most broken forecasts rely
   on exactly one layer (usually raw CRM stage data) and call the result "the forecast."
2. **Move the checkpoint from stage entry to stage exit.** Entry-stage data is provisional;
   exit criteria are the fact-based gate that should drive the number.
3. **Replace flat counts with weighting.** Weight by stage, size, and behavioral signal so
   the forecast reflects deal quality, not just deal presence in the pipeline.
4. **Add a leading layer the CRM cannot provide.** Behavioral signal (call activity,
   sentiment, recency) moves before CRM stage does — this is what enables mid-cycle
   correction rather than waiting for the next stage change to update the number.
5. **Model performance at the individual level, not the team level.** Aggregate after
   modeling individually — aggregating first (top-down) hides the heterogeneity that is
   often the actual source of forecast error.

## Applicability

This pattern fits situations with:
- A forecast (or any recurring estimate) currently built top-down from a single,
  largely lagging data source
- Meaningful heterogeneity at the individual contributor/unit level that a team-level
  average would obscure
- Availability of at least one behavioral/leading-indicator data source distinct from the
  system of record

It does **not** fit situations where the underlying problem is competing stakeholder
interests rather than a data/visibility gap (see FRAME-001 — a different pattern: realigning
incentives, rather than correcting what current data can't see).

## Limitations and Open Questions

- Derived from exactly one committed case (CASE-003). Pattern recurrence at Qu, Checkmate,
  and PAR is flagged from memory but not yet documented as independent case artifacts —
  this framework should remain `draft` and not be cited as "confirmed three times" until
  at least two of those are written up as their own CASE entries, per the framework
  promotion gate.
- Unclear yet whether all five layers are required in every application, or whether the
  framework still holds with three or four layers present. Future cases should test which
  layers are load-bearing versus supplementary.

## Approval History

| Version | Date       | Reviewer | Status | Notes |
| ------- | ---------- | -------- | ------ | ----- |
| 0.1     | 2026-06-22 | JET      | Draft  | Derived from CASE-003. Recurrence at Qu, Checkmate, and PAR flagged as professional recollection, not yet independently documented. Remains draft per STD-002 framework promotion gate until confirmed by additional committed cases. |
