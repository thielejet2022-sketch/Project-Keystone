---
id: CASE-003
title: Forecast Methodology Redesign — Short-Cycle Discovery & Multi-Brand Adaptation
version: 0.1
status: active
category: case
owner: JET
created: 2026-06-21
last_modified: 2026-06-21
depends_on: []
provides:
  - case_forecast_methodology_redesign
supersedes: []
superseded_by: []
tags:
  - case
  - forecasting
  - revenue-operations
  - sales-analytics
  - multi-brand
---

# CASE-003: Forecast Methodology Redesign — Short-Cycle Discovery & Multi-Brand Adaptation

**Status:** Reconstructed from memory — see flagged items
**Date:** 2025
**Tier:** CASE

## Context
Forecast error rate ran ±25% — a structural problem, not a precision problem.
Sales leadership knew they were chronically under-forecasting but couldn't
isolate why, and compensated by inflating guesses ~20% off actuals rather
than fixing the model. Work spanned three sister brands under one parent
company/role: Curve Dental, Flex Dental, and Dental HQ — each with a
materially different go-to-market motion.

## Root cause discovery
Breaking down deal metrics by AE, lead source, deal type/size, and phase
timing surfaced the real driver: 45% of monthly revenue came from deals
with a lead-to-close cycle under 14 days. Standard pipeline reviews were
structurally blind to these — deals entering and closing within the same
month, after the forecast had already been set. Traditional pipeline-based
forecasting was missing nearly half the month's eventual revenue at the
moment of forecast.

## Complicating factor — AE turnover
High month-to-month AE churn broke historical pattern forecasting. Solved
with a rep ramp-up model, continuously updated against actual results,
which smoothed AE variability through 2025.

## Gong integration layer
Mid-month forecast updates sharpened using Gong signals — recent activity,
deal probability, last contact, customer sentiment. By the mid-month
checkpoint, accuracy reached within ±5% of actuals.

## Long-range forecasting
Linear regression and seasonality modeling applied for quarterly/half-year
projections, using micro-by-rep analysis rather than team averages —
materially more precise for a heterogeneous sales team. Validated by the
exec team and Board of Directors.

## Brand-specific adaptation (why this is more than one model)
- **Flex Dental:** Single AE + BDR structure required a different lens
  entirely. Identified a two-factor pattern — lead count as primary driver,
  plus a "sales fatigue" cycle (observable dips in deal count/aging
  followed by pipeline rebuild). Modeling that cycle once identified
  materially improved accuracy.
- **Dental HQ:** PLG model — self-enrolled prospects, reps engaging only
  for support/lapsed signups. Zoho CRM didn't track deal progression,
  requiring 4–6 hrs/month manual transformation until a Python script
  automated it with a full audit trail (separate artifact — see related
  work below). Same forecasting framework applied progressively despite a
  fundamentally different business model, with accuracy improving over
  time.

## Why this approach (not just what)
The core insight — that a forecast can be structurally blind to a real
revenue pattern rather than just imprecise — is the transferable
principle. The fix wasn't "try harder," it was finding the specific blind
spot (short-cycle deals), then building distinct models per brand rather
than forcing one framework onto three different go-to-market motions.

## Outcome

| Metric | Before | After |
|---|---|---|
| Forecast error (4-week horizon) | ±25% | ±5% |
| Methodology | Gut + inflation compensation | Data-driven: short-cycle model + Gong signals + rep ramp model |
| Board confidence | Low — known inaccuracy | High — explicitly validated |
| Brands covered | — | 3 distinct models for 3 distinct business models |

## Related work
Dental HQ's Python-based Zoho data transformation automation is a related
but separate piece of work and should be captured as its own artifact
(referenced here, not duplicated).

## Flagged for honesty in use
- The ±25%→±5% figures are recollection of tracked/reported error rates,
  not a re-derived calculation — confirm against source reporting if
  pressed on provenance, since this is the strongest quantified claim in
  the case.
- "Validated by exec team and Board of Directors" is a strong claim — be
  ready to describe what specifically was presented (the methodology? the
  resulting numbers? both?) rather than leave it vague under follow-up.

## Approval History

| Version | Date       | Reviewer | Status   | Notes |
| ------- | ---------- | -------- | -------- | ----- |
| 0.1     | 2026-06-21 | JET      | Approved | Reconstructed from memory, locked for commit. |
