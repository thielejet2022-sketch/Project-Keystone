---
id: STD-005
title: Design System Standard
version: 0.1
status: active
category: standard
owner: project_keystone
created: 2026-06-21
last_updated: 2026-06-21
depends_on:
  - STD-000
provides:
  - design_system_standard
  - architecture_plate_visual_spec
supersedes: []
superseded_by: []
tags:
  - design
  - visual_standard
  - architecture_plates
  - governance
---

# STD-005 | Design System Standard

## Purpose

This standard defines the visual language, layout rules, and production requirements for all
Project Keystone visuals. It governs Architecture Plates, the project's official executive
architecture artifacts, and any future visual artifact produced for the repository.

This standard promotes content previously held in `design-system/README.md`, which defined
real, actively-used rules (AP-001 was built against it) but lived outside the repository's
artifact taxonomy. Promoting it closes that gap rather than leaving active design rules
undocumented as a numbered standard.

## Core Principle

Every visual should look like part of the same enterprise architecture system. Do not create
isolated graphics.

## Architecture Plate Rules

- Use landscape orientation
- Use deep blueprint navy background
- Include subtle drafting grid and construction marks
- Preserve strict symmetry
- Use generous negative space
- Use thin precision linework
- Use gold only for executive significance, decision points, or critical paths
- Use blueprint cyan for architecture and system structure
- Use modern geometric sans serif typography
- Include an engineering-style title block
- Preserve the main architecture layout during edits

## Title Block Standard

Required fields:

| Field | Standard |
|---|---|
| Project | Project Keystone |
| Plate Number | AP-XXX |
| Title | Architecture Plate Title |
| Revision | Version Number |
| Status | Draft / Review / Approved |
| Architect | James Thiele |
| Date | Current generation date |

## Editing Rule

When modifying an existing Architecture Plate, change only the requested item.

Do not recenter, redesign, resize, restyle, or move unrelated components unless explicitly
requested.

## Version History

| Version | Date | Change |
|---|---|---|
| 0.1.0 | 2026-06-20 | Initial design system established — Architecture Plate standards, title block standard, blueprint visual language, initial editing rules. (Originally recorded in design-system/changelog.md.) |
| 0.1 | 2026-06-21 | Promoted from design-system/README.md to STD-005, conforming to STD-001 metadata schema. No change to substantive rules. |
