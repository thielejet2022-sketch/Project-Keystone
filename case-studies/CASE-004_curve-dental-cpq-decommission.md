---
id: CASE-004
title: Salesforce CPQ Decommission (Curve Dental)
version: 0.2
status: active
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

**Date of decision:** [JET to confirm — approximate window only]
**Tier:** CASE

## Context
Curve Dental was running Salesforce CPQ as part of its quote-to-cash
stack. The trigger was a workflow complaint: reports JET built and shared
with Finance, Product, and Customer Success could not be opened properly
by those teams, because the recipients did not hold CPQ licenses. Initial
discovery into workarounds showed they would be too cumbersome to be
practical, and a parallel evaluation of simply buying additional CPQ
licenses for those teams did not pencil out — not cost-justified for the
value being unlocked.

During that research, JET also discovered that Salesforce had quietly
announced it was ending support/sales of CPQ in its current form, moving
toward a "Revenue Cloud"-type module (exact product name unconfirmed).
That timing reinforced the decision rather than caused it — the core
driver was that CPQ was disproportionately complex for a workflow that
didn't need that level of sophistication, at a $40K/year license cost
with no corresponding value-add.

## Decision
Evaluated and decommissioned Salesforce CPQ, replacing it with native
Salesforce flows built in-house.

## Mechanics
[Gap: the specific native-flow build — how quoting/approval logic was
replicated, what was descoped vs. preserved — is still not detailed
beyond the high-level "native Salesforce flows" description. Lower
priority gap; the case is usable without it.]

## Cross-functional tension
Relatively clean process overall, with one notable moment of resistance:
the CEO was defensive when JET first raised decommissioning CPQ, on the
grounds that CPQ had originally been adopted to mitigate a functionality
gap between Maxio (the billing/invoice engine) and NetSuite — CPQ was
filling an invoicing handoff gap, not just doing quoting. JET's research
addressed this directly: the native-flow replacement needed to (and did)
preserve whatever bridge CPQ had been providing between Maxio and
NetSuite, which is what ultimately resolved the CEO's objection.

## Why this approach (not just what)
Two judgment calls stand out:
1. **Treating it as a discovery problem, not a licensing problem.**
   The instinctive fix to "people can't open the reports" is to buy more
   licenses. JET tested that option financially first and only moved to
   replacement once it was clear the ROI wasn't there.
2. **Solving the CEO's actual underlying concern, not just the surface
   objection.** The CEO's pushback wasn't really about CPQ itself — it
   was about losing the Maxio-to-NetSuite bridge CPQ happened to provide.
   Recognizing that distinction is what let JET propose a replacement
   that addressed the real risk instead of arguing past it.

## Outcome
- ~$40K/year in licensing cost avoided.
- Improved data sharing across Product and Customer Success teams, who
  could now open and act on reports without needing CPQ licenses.
- Maxio-to-NetSuite invoicing continuity preserved through the
  replacement, resolving the CEO's core objection.

## Flagged for honesty in use
- Mechanics section (the specific native-flow build) remains at a
  high level — sufficient for narrative use, but not detailed enough to
  defend a technical deep-dive without further input from JET.
- All other sections reflect JET's direct account (2026-06-22) and are
  not under the reconstruction caveat that applied to v0.1.

## Approval History

| Version | Date       | Reviewer | Status   | Notes |
| ------- | ---------- | -------- | -------- | ----- |
| 0.1     | 2026-06-22 | JET      | Superseded | Initial draft from Actionstep screening-call recap. |
| 0.2     | 2026-06-22 | JET      | Approved | Context, tension, and rationale filled in directly by JET. Mechanics remains high-level by choice, not by gap. Promoted to active. |
