---
id: CASE-004
title: Salesforce CPQ Decommission (Curve Dental)
version: 0.1
status: draft
category: case
owner: JET
created: 2026-06-22
last_modified: 2026-06-22
depends_on: []
provides:
  - case_curve_dental_cpq_decommission
supersedes: []
superseded_by: []
tags:
  - case
  - salesforce
  - tech-stack
  - cost-optimization
  - revenue-operations
---

# CASE-004: Salesforce CPQ Decommission (Curve Dental)

**Status:** Reconstructed from a recruiter screening-call recap — lower fidelity than CASE-001–003, flagged for JET review before promotion to active
**Date of decision:** [JET to confirm — approximate window only]
**Tier:** CASE

## Context
Curve Dental was running Salesforce CPQ as part of its quote-to-cash
stack. [Gap: specific pain point — pricing complexity, license cost,
configuration overhead, or data fragmentation — needs JET's detail; only
the outcome was captured in the interview recap, not the triggering
problem.]

## Decision
Evaluated and decommissioned Salesforce CPQ, replacing it with native
Salesforce flows built in-house.

## Mechanics
[Gap: what the native flows actually did, how they replicated CPQ's
quoting/approval logic, what was descoped vs. preserved — not captured
in the source material.]

## Cross-functional tension
[Gap: not captured in the interview recap — likely candidates are Sales
(quoting speed/complexity) and Finance (margin/discount controls),
consistent with the CPQ-replacement pattern, but this needs JET's actual
account rather than inference.]

## Why this approach (not just what)
Removing a licensed CPQ layer in favor of native flows traded platform
flexibility for lower cost and tighter data integration with Product and
Customer Success — but the judgment call behind *why* native flows were
sufficient (vs. a different CPQ alternative, or no replacement at all)
isn't yet documented.

## Outcome
- ~$40K/year in licensing cost avoided.
- Improved data sharing across Product and Customer Success teams
  (mechanism not yet detailed).

## Flagged for honesty in use
- **This entire case is currently under-evidenced.** It was reconstructed
  from a compressed recap of a live interview answer, not from a direct
  working session like CASE-001–003. Numbers (the $40K figure) and the
  high-level outcome are reasonably solid; context, mechanics, and
  cross-functional tension are inferred gaps, not JET's actual account.
- Do not cite the tension/mechanics sections in an interview until JET
  fills them in — they are placeholders, not memory.

## Approval History

| Version | Date       | Reviewer | Status   | Notes |
| ------- | ---------- | -------- | -------- | ----- |
| 0.1     | 2026-06-22 | JET      | Pending  | Drafted from screening-call recap; needs JET's detail on context, mechanics, and tension before promotion to active. |
