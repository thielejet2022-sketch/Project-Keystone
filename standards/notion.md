---
id: STD-004
title: Notion Rendering Standard
version: 0.1
status: draft
category: standard
owner: project_keystone
created: 2026-06-21
last_updated: 2026-06-21
depends_on:
  - STD-000
provides:
  - notion_rendering_standard
supersedes: []
superseded_by: []
tags:
  - governance
  - notion
  - standards
---

# STD-004 | Notion Rendering Standard

## Purpose

This standard defines the role of Notion within Project Keystone: a rendered, visual layer
for repository content, never an authoritative source.

## Guiding Principle

GitHub remains the single source of truth, per standards/github.md. Notion exists to make
that content easier to browse and present — dashboards, framework cards, visual summaries —
not to hold unique content.

## Direction of Sync

Sync is one-directional: GitHub → Notion.

- Authoritative artifacts are authored and committed to GitHub first.
- Notion pages are generated or updated to reflect committed GitHub content.
- Notion is never edited directly as a record of new thinking. If new thinking happens in
  Notion, it is exploratory only — equivalent to a LAB note — until promoted into GitHub via
  the normal STD-003 contribution process. Only then does the Notion view get regenerated.

## What Belongs in Notion

- Dashboard views of Framework Library entries
- Visual cards summarizing CAP/SPEC/PLAY artifacts
- Status overviews (e.g., which milestones are active, which frameworks exist)

## What Does Not Belong in Notion

- Original drafts of standards, specifications, or frameworks
- Anything that should be versioned and is not also committed to GitHub
- Working notes that haven't been promoted through STD-003

## Failure Mode This Prevents

Without this standard, Notion risks becoming a second, ungoverned authoritative source —
content edited there without a corresponding GitHub commit would have no version history,
no commit narrative, and no STD-003 validation. This standard exists to prevent that drift
before it happens.
