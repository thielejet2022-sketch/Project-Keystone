---
id: FRAME-001
title: Bounded Lever Realignment
version: 0.1
status: draft
category: framework
owner: JET
created: 2026-06-21
last_modified: 2026-06-21
depends_on:
  - CASE-001
  - CASE-002
provides:
  - framework_bounded_lever_realignment
supersedes: []
superseded_by: []
tags:
  - framework
  - pricing
  - incentive-design
  - stakeholder-alignment
---

# FRAME-001: Bounded Lever Realignment

**Tier:** FRAME
**Status:** Draft — derived from two Case Studies, not yet exercised on a third

## Core Insight

When two or more stakeholders have genuinely competing interests over the same decision, the
instinctive move is to negotiate a tradeoff between them. The more durable move is to find a
single, deliberately bounded mechanism that lets both interests win through the same
behavior — so the stakeholders stop pulling against each other and start pulling the same
direction.

The mechanism must be *bounded*: it should touch only the smallest piece of value necessary
to create the incentive, leaving the larger, more important value untouched. An unbounded
lever (discounting everything, moving every tier) recreates the original tradeoff instead of
resolving it.

## Where This Pattern Showed Up

**CASE-001 (Curve Dental G/B/B packaging):** Sales wanted easy-to-sell bundles; the CFO
wanted margin protection; the two pulled against each other. The bounded lever was anchoring
the highest-demand module above the base tier — this simultaneously protected margin (CFO)
and created upgrade pull (sales), without trading one against the other. Curve Pay added a
second bounded lever: a discount tied only to payments attach, never touching the recurring
SaaS fee.

**CASE-002 (Curve Dental deal timing):** Finance/AP needed deals spread out to process
upfront fees; Implementation needed deals spread out to meet SLA; AEs needed a reason to
close earlier than the deadline they'd always closed against. The bounded lever was a
discount on the one-time upfront fee only, for deals signed by the 21st — recurring revenue
was fully protected, and the lever was cheap relative to what it fixed.

## The Pattern, Generalized

1. **Identify the real tension** — name the specific stakeholders and what each actually
   needs, not just "there was disagreement."
2. **Find the smallest piece of value that can move** — the part of the deal/price/process
   that, if adjusted, doesn't damage the thing everyone actually depends on (margin,
   recurring revenue, core SLA).
3. **Attach the incentive to that piece, and only that piece.** Resist the urge to make the
   incentive bigger or broader to "make sure it works" — boundedness is what keeps the
   tradeoff from reappearing.
4. **Hold the mechanism firm once live.** (See CASE-002's execution lesson: exceptions teach
   people the boundary is negotiable, which undoes the realignment.)
5. **Measure the shift, not just the existence of the new mechanism** — both source cases
   used a concrete before/after metric (deal-desk involvement rate; close-date distribution
   slope) rather than assuming the lever worked because it was designed well.

## Applicability

This pattern fits situations with:
- Two or more stakeholders with a genuine, named conflict of interest
- A decision being treated as a tradeoff/negotiation by default
- At least one piece of value that is separable from the core asset everyone depends on

It does **not** fit situations where the underlying problem is a missing capability or
missing information (see CASE-003's short-cycle forecasting blind spot — a different pattern:
finding what the current process can't see, rather than realigning competing interests).

## Limitations and Open Questions

- Derived from exactly two cases, both at Curve Dental, both pricing/incentive decisions. Not
  yet tested against a case outside pricing/packaging, or outside one company. Should remain
  `draft` until exercised on a third, ideally unrelated, case.
- Unclear yet whether "boundedness" has a measurable threshold, or is simply a qualitative
  design discipline. Future cases should test this.

## Approval History

| Version | Date       | Reviewer | Status | Notes |
| ------- | ---------- | -------- | ------ | ----- |
| 0.1     | 2026-06-21 | JET      | Draft  | Proof-of-concept framework distilled from CASE-001 and CASE-002. Remains draft per STD-002 until exercised on a third independent case. |
