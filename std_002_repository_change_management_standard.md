---
id: STD-002
title: Repository Change Management Standard
version: 0.1
status: draft
category: standard
owner: project_keystone
created: 2026-06-21
last_updated: 2026-06-21
depends_on:
  - STD-000
  - STD-001
provides:
  - change_management_standard
supersedes: []
superseded_by: []
tags:
  - governance
  - versioning
  - standards
  - lifecycle
---

# STD-002 | Repository Change Management Standard

## Purpose

This standard defines how artifacts within Project Keystone change over time: how versions
increment, how status moves through its lifecycle, and how artifacts are superseded rather
than silently edited. It exists to close a real gap — STD-003 referenced this standard as a
dependency before it was written.

## Version Numbering

Artifacts use a two-part version number: `major.minor`.

- **Minor** increments (0.1 → 0.2) for clarifying edits that do not change the artifact's
  meaning or guidance — wording, formatting, examples.
- **Major** increments (0.x → 1.0) when an artifact moves from `draft` or `review` to
  `active`, or when its guidance materially changes.

A major version increment to 1.0 or beyond should coincide with a status of `active`.
Artifacts should not claim `active` status while still at version 0.x.

## Status Lifecycle

Every artifact's `status` field moves through a fixed set of states, in order:

```text
draft → review → active → deprecated
```

- **draft** — newly created, not yet validated against real use. This is the default for any
  artifact created from a single application, per the Repository Growth Rule.
- **review** — has been exercised at least once and is under active reconsideration.
- **active** — validated through repeated real use; authoritative for current work.
- **deprecated** — no longer current guidance, retained for historical record. A deprecated
  artifact must set `superseded_by` to the artifact that replaces it.

Status moves forward by deliberate decision, not by default. An artifact does not become
`active` simply by aging.

## Superseding, Not Editing

When an artifact's guidance changes in a way that contradicts its prior version, the prior
artifact is not silently rewritten. Instead:

1. The new artifact is created with its own `id` and `supersedes` field pointing to the prior
   artifact's `id`.
2. The prior artifact's `status` is updated to `deprecated`, and its `superseded_by` field is
   set to the new artifact's `id`.
3. Both artifacts remain in the repository. History is preserved, not erased.

Minor clarifications that do not change meaning may be edited in place with a minor version
bump and a standard commit, rather than superseded.

## Relationship to STD-003

STD-003 defines the contribution package format. This standard defines what happens to an
artifact's own metadata (`version`, `status`, `supersedes`, `superseded_by`) as it evolves
after that initial contribution. Every contribution governed by STD-003 should set its
initial version and status according to this standard.

## Repository Philosophy

Change management exists so that the repository's history remains legible. Anyone reading an
artifact months later should be able to tell, from its metadata alone, how mature it is, what
it replaced, and whether it has since been replaced — without needing to ask.
