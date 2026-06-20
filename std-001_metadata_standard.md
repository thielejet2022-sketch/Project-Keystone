---
id: STD-001
title: Metadata Standard
version: 0.1
status: draft
category: standard
owner: project_keystone
created: 2026-06-20
last_updated: 2026-06-20
depends_on: []
provides:
  - metadata_standard
supersedes: []
superseded_by: []
tags:
  - metadata
  - standards
  - governance
---

# STD-001 | Metadata Standard

## Purpose

This standard defines the metadata schema used by every authoritative artifact within Project Keystone.

The objective is consistency, discoverability, dependency management, and long-term maintainability.

Metadata shall use only approved fields and approved values.

## Required Metadata

Every authoritative Keystone artifact must begin with YAML front matter.

```yaml
---
id:
title:
version:
status:
category:
owner:
created:
last_updated:
depends_on:
provides:
supersedes:
superseded_by:
tags:
---
