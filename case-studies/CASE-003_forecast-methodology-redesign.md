---
id: CASE-003
title: Forecast Methodology Redesign — Short-Cycle Discovery & Multi-Brand Adaptation
version: 0.2
status: active
category: case
owner: JET
created: 2026-06-21
last_modified: 2026-06-22
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
Forecast error rate averaged ±25% — a structural problem, not a precision problem.
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

## Methodology shift (top-down → bottoms-up, layered inputs)
The redesign is more precisely described as a shift in forecasting
methodology, not just a new model:

- **Top-down → bottoms-up.** The prior model was top-down: a single
  team-level number, sandbagged ~20% to compensate for known inaccuracy.
  The redesign rebuilt forecasting bottoms-up — individual rep-level
  regression aggregated upward, rather than a team average, because rep
  heterogeneity was itself a forecast-error source the top-down view
  couldn't see.
- **CRM exit criteria as a forecasting input, not just pipeline hygiene.**
  Standard pipeline review treated stage *entry* as the signal. The
  redesign treated stage *exit* criteria — the specific, defined
  conditions required to advance a deal — as the actual forecasting
  checkpoint, since entry-stage data was lagging and unreliable for
  short-cycle deals.
- **Weighted forecast over flat pipeline count.** Deals were weighted by a
  composite of stage, deal size, and behavioral signal rather than counted
  at face value. This weighting is what closed the gap on the structurally
  invisible short-cycle deals.
- **Behavioral indicators as a leading layer over lagging CRM data.** Gong
  signals — activity recency, sentiment, last contact — became the
  mid-month correction layer precisely because CRM stage data lags by
  nature; behavioral data moves first.
- **Rep-level performance metrics replacing team averages.** The ramp-up
  model and micro-by-rep regression are this in practice: a ramping rep
  gets a different curve than a tenured rep, rather than both being
  smoothed into one blended team number.

This same pattern — layered, behaviorally-weighted, bottoms-up forecasting
— has recurred elsewhere in JET's career (flagged here as "recurred
elsewhere," not yet documented as separate case artifacts); see FRAME-002.

## Outcome

| Metric | Before | After |
|---|---|---|
| Forecast error (4-week horizon) | ±25% avg (range ±20–30% month to month) | ±5% |
| Methodology | Top-down team average + gut inflation compensation | Bottoms-up, rep-level: exit-criteria checkpoints + weighted forecast + Gong behavioral signals + rep ramp model |
| Board confidence | Low — known inaccuracy | High — explicitly validated |
| Brands covered | — | 3 distinct models for 3 distinct business models |

## Related work
Dental HQ's Python-based Zoho data transformation automation is a related
but separate piece of work and should be captured as its own artifact
(referenced here, not duplicated).

## Flagged for honesty in use
- The ±25% figure is a monthly average; actual monthly variance ranged
  ±20–30%. If asked for precision, use "~25% average, ranging 20–30% month
  to month" rather than a single static number — this is the strongest
  quantified claim in the case and should be stated accurately.
- "Validated by exec team and Board of Directors" is a strong claim — be
  ready to describe what specifically was presented (the methodology? the
  resulting numbers? both?) rather than leave it vague under follow-up.
- The "recurred elsewhere" claim (Qu, Checkmate, PAR) is JET's professional
  recollection, not yet backed by committed case artifacts for those
  companies — be ready to speak to it as pattern recognition across roles,
  not as documented Keystone cases, unless/until those are captured
  separately.

## Approval History

| Version | Date       | Reviewer | Status   | Notes |
| ------- | ---------- | -------- | -------- | ----- |
| 0.1     | 2026-06-21 | JET      | Approved | Reconstructed from memory, locked for commit. |
| 0.2     | 2026-06-22 | JET      | Approved | Added methodology-shift framing (top-down vs bottoms-up, exit criteria, weighted forecast, behavioral indicators, rep-level metrics) and clarified ±25% as a monthly average (range ±20–30%). |
