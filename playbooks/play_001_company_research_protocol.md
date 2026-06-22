---
id: PLAY-001
title: Company Research Protocol for Interview Prep
version: 0.1
status: active
category: playbook
owner: JET
created: 2026-06-22
last_modified: 2026-06-22
depends_on:
  - SPEC-001
provides:
  - play_company_research_protocol
supersedes: []
superseded_by: []
tags:
  - playbook
  - career
  - interview-prep
  - research
---

# PLAY-001: Company Research Protocol for Interview Prep

**Tier:** PLAY
**Executes:** SPEC-001 (JD-to-Narrative Gap Analysis), specifically Step 3 — Gather Evidence

## Purpose

SPEC-001 calls for separating JD facts from assumptions and cross-referencing against the
candidate's background, but doesn't specify *how* to do that research. This playbook is the
concrete method — used repeatedly, by hand, before SPEC-001 existed as a named spec — that
fills that gap. SPEC-001 references this playbook rather than re-describing it.

## The Four Passes

### Pass 1 — Ownership & Capital Structure
Identify who owns the company and what that implies about urgency and mandate.
- Funding round and stage (seed/growth/PE buyout/public)
- Sponsor's stated investment thesis at time of investment
- Named partner/deal lead assigned to the account, if identifiable
- Time elapsed since investment vs. sponsor's typical hold period
- Any visible exit signals (process rumors, banker engagement, portfolio page changes)

**Why it matters:** ownership stage and hold-period proximity predict whether the mandate is
growth-at-all-costs, margin/EBITDA tightening ahead of a sale, or steady-state — and that
shapes what the hiring manager actually needs from this role.

### Pass 2 — M&A History, Causally Linked to Own Experience
List every acquisition with who/when/what/why — but don't stop at the list. For each one,
identify a specific personal proof point that maps to the *integration problem* that
acquisition created (data normalization, system consolidation, comp/process harmonization).
- Don't generically claim "I have M&A experience" — name the specific acquisition-side problem
  you solved (e.g., Python-based data normalization at Dental HQ mapping to the Curve Dental
  standard) and connect it directly to the target company's specific acquisition.

**Why it matters:** this is where a candidate stops sounding relevant and starts sounding like
the obvious hire — generic relevance vs. a named, structurally identical problem already solved.

### Pass 3 — Hiring Manager Dossier
Build the hiring manager as a person, not a title.
- LinkedIn profile, tenure in current role, time in company
- Current location/hometown
- Career path — prior companies, what kind of operator they are
- Any shared network, school, or prior-company overlap

**Why it matters:** shapes both rapport-building and a read on what kind of operator they're
likely to respond to (builder vs. process person, technical vs. commercial, etc.).

### Pass 4 — JD Line-Mining for Rockstar Moments
Re-read the JD specifically hunting for phrases — not requirements in general, but exact
language — where existing experience is a near-literal match. The goal is identifying the
2-4 lines in the JD where the candidate can point at the posting itself and say "this, I've
done exactly this."
- Distinct from Pass 2: Pass 2 is about acquisition-specific narrative; Pass 4 is about
  matching the JD's own vocabulary and requirements line-by-line.
- Flag the inverse too: JD lines with no real match, so they're answered deliberately rather
  than discovered live in the room.

**Why it matters:** recruiters and hiring managers pattern-match against the language they
wrote. A candidate who can mirror that language credibly reads as a stronger match than one
who is accurate but generic.

## Constraints

- All four passes must use real, verifiable candidate experience (per SPEC-001's constraint)
  — Pass 2 and Pass 4 are the most likely to tempt overreach; do not stretch a proof point to
  fit a requirement it doesn't actually match.
- Pass 1 and Pass 3 rely on external research and may carry confidence gaps (marked ❓ or 🔍
  per existing CIB convention) — these should be explicitly flagged as open, not implied as
  settled, in any output.
- This playbook produces *inputs* to SPEC-001's narrative output — it is not itself a
  finished interview script.

## Relationship to Existing Tools

A Company Intelligence Brief (CIB), where one already exists, may pre-fill Pass 1–3
substantially. Pass 4 (JD line-mining) is rarely covered by a CIB, since a CIB is built before
a specific JD is in hand — this pass should be run explicitly even when a CIB exists.

## Approval History

| Version | Date       | Reviewer | Status | Notes |
| ------- | ---------- | -------- | ------ | ----- |
| 0.1     | 2026-06-22 | JET      | Approved | Formalized from JET's existing informal research pattern, used repeatedly prior to this writeup. First applied retroactively to Actionstep prep. |
