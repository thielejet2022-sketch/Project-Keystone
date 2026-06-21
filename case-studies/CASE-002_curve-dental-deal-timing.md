---
id: CASE-002
title: Deal Timing & Revenue Distribution — Early-Close Incentive (Curve Dental)
version: 0.1
status: active
category: case
owner: JET
created: 2026-06-21
last_modified: 2026-06-21
depends_on: []
provides:
  - case_curve_dental_deal_timing
supersedes: []
superseded_by: []
tags:
  - case
  - revenue-operations
  - deal-desk
  - incentive-design
  - forecasting
---

# CASE-002: Deal Timing & Revenue Distribution — Early-Close Incentive (Curve Dental)

**Status:** Reconstructed from memory — see flagged items
**Date of decision:** 2025
**Tier:** CASE

## Context
~60% of monthly MRR was closing in the final 2 days of the month — a hockey-stick
revenue curve. This created compounding downstream strain: Finance/AP had to
collect one-time upfront service fees before deals could be recognized, with
almost no runway at month-end; Implementation had a 24-hour SLA to contact new
customers, and the volume spike made consistent SLA compliance unsustainable.

## Decision
Designed a customer-facing early-close incentive: a reduced one-time upfront
service fee for deals signed by the 21st of the month. Recurring SaaS fees
were fully protected — only the one-time fee was used as the lever, bounding
the cost of the incentive and avoiding any erosion of long-term contract
value.

## Why this approach (not just what)
Gave AEs a hard, meaningful CTA to pull closes into week 3 instead of
negotiating against month-end. Using only the one-time fee as the lever meant
the incentive was cheap relative to recurring revenue protected.

## Execution discipline (critical lesson)
The incentive only worked once the 21st deadline was held without exception.
Early flexibility on the deadline taught AEs and customers it was
negotiable, which undermined the entire behavior-change goal — this was the
operational risk that mattered more than the incentive design itself.

## Mechanism / validation
Tracked monthly via a formal report measuring the slope of the deals-closed
curve across the month. Pre-intervention: steep hockey stick, concentrated
in the final 2 days. Post-intervention: flatter distribution — slow week 1,
building week 2, ~70% of MRR closing by the 21st, then a genuine incremental
"week 4" of selling activity that hadn't functionally existed before
(previously absorbed into month-end crunch).

## Outcome
~70% of MRR closing by the 21st (vs. ~60% previously concentrated in the
final 2 days) — a materially flatter close-date distribution and an
effective additional week of productive selling time per month.

## Flagged for honesty in use
- The slope-of-close-date tracking was a formal report built/pulled —
  confirmed measured, not just recalled.
- The 70% figure is recollection of the tracked outcome; if asked for exact
  source data (dashboard, BI tool, etc.) in an interview, be ready to
  describe what it was pulled from rather than imply a live citation.

## Approval History

| Version | Date       | Reviewer | Status   | Notes |
| ------- | ---------- | -------- | -------- | ----- |
| 0.1     | 2026-06-21 | JET      | Approved | Reconstructed from memory, locked for commit. |
