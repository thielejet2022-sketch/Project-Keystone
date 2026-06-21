---
id: CASE-001
title: À La Carte → Good/Better/Best Packaging (Curve Dental)
version: 0.1
status: active
category: case
owner: JET
created: 2026-06-21
last_modified: 2026-06-21
depends_on: []
provides:
  - case_curve_dental_gbb_packaging
supersedes: []
superseded_by: []
tags:
  - case
  - pricing
  - packaging
  - deal-desk
  - revenue-operations
---

# CASE-001: À La Carte → Good/Better/Best Packaging (Curve Dental)

**Status:** Reconstructed from memory — see flagged items
**Date of decision:** January 2025 (implementation)
**Tier:** CASE

## Context
Curve Hero shipped as a base module with à la carte add-ons. By the time a
deal was built out to meet customer needs, total price routinely exceeded
buyer tolerance, triggering deal desk intervention on the large majority of
deals rather than as an exception.

## Decision
Proposed restructuring into Good/Better/Best tiers, drawing on prior NCR
hardware pricing experience where tiered bundling controlled discount creep
and shaped buyer choice. Implemented as new business practice, January 2025.

## Tier composition mechanics
- A specific high-demand module (per product's qualitative market read) had
  two variants — one populating Better, a more full-featured version
  populating Best — giving each upper tier a distinct upgrade reason.
- Curve Pay was structured as a cross-cutting module available across all
  three tiers; attaching it triggered a bundle-wide discount regardless of
  tier, creating a separate attach-driven incentive lever alongside the
  tier-upgrade lever. Curve Pay processed payments through Stripe as the
  underlying facilitator.

## Cross-functional tension
- Sales favored the bundle concept — easier to sell a tier than negotiate
  an à la carte stack.
- The harder question was tier composition: which modules/variants went
  where.
- CFO weighed in based on margin contribution per module — popularity and
  profitability didn't always align.
- Resolution: anchor high-demand modules above the base tier (protecting
  margin while creating upgrade pull); use Curve Pay as an independent
  cross-tier discount lever tied to payments attach.

## Why this approach (not just what)
Tiering converts "discount to close the gap" into "select the tier that
fits." The Curve Pay structure adds a second lever that captures
margin/volume benefit via attach rate without requiring a tier upgrade.

## Outcome
Deal desk involvement rate dropped from ~80% to ~15% (team's tracked/
recalled historical average) between implementation (Jan 2025) and end of
Q2 2025.

## Flagged for honesty in use
- Tier-content decisions were judgment/feedback-driven (product's market
  read), not attach-rate-data-driven.
- The 80%→15% figure is the deal desk team's recollection of historical
  involvement rate, not a formal analytics export.

## Approval History

| Version | Date       | Reviewer | Status   | Notes |
| ------- | ---------- | -------- | -------- | ----- |
| 0.1     | 2026-06-21 | JET      | Approved | Reconstructed from memory, locked for commit. |
