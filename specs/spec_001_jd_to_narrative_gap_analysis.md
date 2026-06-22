---
id: SPEC-001
title: JD-to-Narrative Gap Analysis
version: 0.2
status: draft
category: specification
owner: project_keystone
created: 2026-06-21
last_updated: 2026-06-22
depends_on:
  - STD-000
  - STD-001
  - PLAY-001
provides:
  - jd_to_narrative_gap_analysis
supersedes: []
superseded_by: []
tags:
  - specification
  - career
  - run_keystone
  - executive_positioning
---

# SPEC-001 | JD-to-Narrative Gap Analysis

## Purpose

This specification defines a repeatable method for converting a job description into a
structured interview-positioning strategy using the Run Keystone protocol.

It exists because evaluating "fit" against a JD is, structurally, an executive decision
problem: incomplete evidence, competing tradeoffs, and a need for defensible judgment under
time pressure. Run Keystone is built for exactly this category of problem.

## When To Use

Apply this specification whenever a real job description exists and an interview is scheduled
or imminent. Do not apply it speculatively to JDs of casual interest — per the Repository
Growth Rule, specifications should be exercised on real decisions before being treated as
settled process.

## Procedure

Run Keystone's eight steps map to JD evaluation as follows.

### Step 1 — Define the Decision
Do not default to "should I take/pursue this role." Identify the narrower, controllable
decision — typically: *how do I position [specific prior experience] as credible evidence for
[specific JD requirement] without it reading as [specific risk]?*

### Step 2 — Define Success
State 2-3 concrete, observable markers (e.g., callback secured, comp anchored at a specific
band, candidate controls a specific frame in interview) rather than a vague outcome.

### Step 3 — Gather Evidence
Separate the JD into facts (explicit requirements, reporting lines, stated priorities) versus
assumptions (inferred company pain points, unstated culture signals). Cross-reference against
the candidate's actual background to surface the real gap — title, scope, domain, or
technical depth — rather than assuming the gap before checking.

**Method:** Execute PLAY-001 (Company Research Protocol for Interview Prep) in full — all four
passes (ownership/capital structure, M&A-to-proof-point mapping, hiring manager dossier, JD
line-mining) — rather than relying on whatever a pre-existing Company Intelligence Brief
happens to cover. A CIB built before a specific JD existed will typically cover Passes 1–3 but
not Pass 4; Pass 4 must still be run explicitly even when a CIB exists.

### Step 4 — Build Mental Models
Identify which existing Keystone frameworks apply. If none exist yet for the gap identified,
that absence is itself useful evidence for what to build next — do not force-fit an unrelated
framework.

### Step 5 — Evaluate Tradeoffs
Surface explicit positioning tradeoffs (e.g., technical depth vs. judgment-level framing,
leading with title vs. leading with scope) rather than defaulting to one without
articulating the alternative.

### Step 6 — Form Executive Judgment
State which audience (recruiter screen vs. hiring manager vs. panel) the judgment applies to.
Positioning that works for one audience may be wrong for another within the same process.

### Step 7 — Executive Recommendation
Produce concrete, usable output — a scripted answer, a likely-question table, or a closing
question — not abstract advice.

### Step 8 — Promote Learning
If the pattern proves reusable, promote it into the repository following STD-003. This
specification is itself a Step 8 output from its first real application. PLAY-001 is, in turn,
a Step 8 output from this specification's own first live run — its Step 3 execution against a
real JD (Actionstep) surfaced that Pass 4 hadn't been run as a deliberate step, even with a
CIB in hand.

## Constraints

- This specification governs *positioning strategy*. It does not generate factual claims not
  supplied by the candidate. All examples and metrics must originate from the candidate's
  actual experience.
- Output should distinguish clearly between recruiter-screen-level framing and
  technical-round-level framing; collapsing the two produces answers calibrated to the wrong
  audience.
- Step 3 must not be considered complete until all four PLAY-001 passes have been explicitly
  run, even when a pre-existing CIB appears to cover the company.

## Approval History

| Version | Date       | Reviewer | Status | Notes |
| ------- | ---------- | -------- | ------ | ----- |
| 0.1     | 2026-06-21 | JET      | Approved | Initial specification, drafted prior to first live run. |
| 0.2     | 2026-06-22 | JET      | Approved | Added PLAY-001 dependency and explicit method for Step 3, after first live run (Actionstep) surfaced that JD line-mining (Pass 4) wasn't executed as a deliberate step despite an existing CIB. |
