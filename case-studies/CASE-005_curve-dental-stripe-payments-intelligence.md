---
id: CASE-005
title: Stripe Payments Operational Intelligence System (Curve Dental, NewCo LLC)
version: 0.2
status: draft
category: case
owner: JET
created: 2026-06-22
last_modified: 2026-06-22
depends_on: []
provides:
  - case_curve_dental_stripe_churn_reduction
supersedes: []
superseded_by: []
tags:
  - case
  - billing
  - cross-functional-handoff
  - revops-automation
  - executive-reporting
  - revenue-operations
---

# CASE-005: Stripe Payments Operational Intelligence System (Curve Dental, NewCo LLC)

**Status:** Drafted from a full source document (case study write-up) — high fidelity; one remaining gap flagged below before promotion to active
**Date of decision:** [JET to confirm — approximate window only]
**Tier:** CASE

## Context
Curve Dental launched Stripe Connected Accounts as a new revenue stream
through payment processing fees. A critical blind spot existed between
sales and payment activation: Sales closed deals in Salesforce, but
nothing tracked whether customers actually completed Stripe onboarding.
Salesforce tracked the pipeline, Stripe tracked payment activity, and no
system connected the two. Finance was spending 3 hours/day manually
investigating leadership's ad hoc questions about the initiative, and
executive leadership across Product, Revenue, Finance, and the C-suite
had no reliable visibility into whether the initiative was working.

## Decision
Diagnosed the abandonment as an operational-instrumentation gap, not a
product or pricing problem — deals could close and then silently fail
downstream with no one noticing. Designed and built an automated
operational intelligence layer bridging Salesforce's revenue pipeline and
Stripe's payment infrastructure, rather than escalating it as a Sales or
Product issue.

## Mechanics
Lightweight integration architecture, deliberately chosen over a custom
application for speed of deployment and maintainability by non-technical
stakeholders:
- **Stripe API** — real-time payment account data and onboarding status
- **Salesforce API/sync** — correlates deals with payment activation
  status, with Salesforce as system of record
- **Google Sheets** — central control module and data repository
- **Google AppScript** — automation engine for sync and business logic

Built four capabilities on top of that architecture:
1. **Onboarding pipeline monitoring** — tracked customer progress through
   every milestone, account creation through first payment processed
2. **Portfolio health scoring** — algorithmic classification of accounts
   as High-Performing, Dormant, or At-Risk based on payment velocity and
   engagement
3. **Exception alerting** — proactive notifications on stalled
   onboarding, so account managers could intervene before abandonment
   rather than discovering it after the fact
4. **Executive reporting** — daily automated dashboards built to answer
   leadership's strategic questions directly, eliminating the need for
   finance to manually investigate

## Cross-functional tension
[Gap: not explicitly documented in the source, but reasonably inferable
— Sales owned the close, Finance owned the manual investigation burden,
and no function owned the handoff itself. Worth JET confirming whether
this was framed/resisted by any function before the fix, or simply an
unowned gap nobody had contested.]

## Why this approach (not just what)
Three deliberate design choices, explicitly reasoned in the source
material rather than just implemented:
- **Lightweight over custom-built:** Google Sheets as the integration
  layer instead of a full application — traded technical elegance for
  speed and non-technical maintainability.
- **Automated exception detection over manual review:** algorithmic
  flagging of at-risk accounts so nothing depended on someone remembering
  to check.
- **Executive-first reporting:** dashboards designed around leadership's
  actual strategic questions, not generic operational metrics — directly
  eliminating the 3-hours/day finance burden rather than just automating
  it.

## Outcome
| Metric | Before | After |
|---|---|---|
| Onboarding abandonment rate | 20% | 4% |
| Payment revenue share | Baseline | +8% |
| Daily manual reporting effort | 3 hours | Eliminated |
| Additional headcount required | Planned | Zero |

Second-order finding: the system **uncovered performance blind spots at
the individual rep level** — specific Account Executives whose deals
consistently stalled during onboarding, enabling targeted coaching that
wouldn't have been visible without the unified view.

## Flagged for honesty in use
- **Confirmed metric:** 20% onboarding abandonment reduced to 4% is the
  validated figure (JET confirmed 2026-06-22). An earlier recall of this
  story (PartsBase recruiter screen) cited "~30% attrition reduced to
  ~8% churn" — that figure is superseded and should not be cited.
- Cross-functional tension section remains inferred, not confirmed.
- Everything else in this version is sourced from a full written case
  study document, not a compressed interview recap — meaningfully higher
  fidelity than CASE-004.

## Approval History

| Version | Date       | Reviewer | Status   | Notes |
| ------- | ---------- | -------- | -------- | ----- |
| 0.1     | 2026-06-22 | JET      | Superseded | Initial draft from PartsBase screening-call recap. |
| 0.2     | 2026-06-22 | JET      | Pending  | Rebuilt from full source case study document. Metric confirmed as 20%/4% (abandonment), superseding the earlier 30%/8% recall. |
