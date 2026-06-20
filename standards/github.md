# GitHub Standards

**Project Keystone**

Version: Living Document

---

# Purpose

GitHub serves as the authoritative source for all Project Keystone standards, workflows, architecture decisions, and project artifacts.

Conversations are exploratory.

Markdown specifications are authoritative.

A standard does not officially exist until it has been promoted into this repository.

---

# Guiding Principles

## Standards Over Memory

Do not rely on conversational memory for long-term project behavior.

If a process becomes repeatable and valuable, document it.

---

## Version Everything

Treat documentation with the same discipline as software.

Every meaningful change should be committed with an explanation describing why the decision was made.

---

## Build From Proven Experience

Do not document hypothetical processes.

Only promote patterns that have been successfully used in real work.

---

## Incremental Evolution

Prefer many small improvements over large speculative rewrites.

Every commit should make the repository measurably better.

---

# Repository Philosophy

The repository documents:

* Standards
* Workflows
* Architecture
* Design decisions
* Lessons learned
* Reusable patterns

The repository is **not** intended to capture temporary notes, brainstorming, or one-off experiments.

---

# Commit Standards

## Commit Format

```text
<prefix>: <short description>
```

Example:

```text
docs: establish Keystone guiding principle
```

---

# Approved Commit Prefixes

| Prefix    | Purpose                                          |
| --------- | ------------------------------------------------ |
| feat:     | New functionality                                |
| fix:      | Bug correction                                   |
| docs:     | Documentation updates                            |
| refactor: | Internal restructuring without behavioral change |
| style:    | Formatting, naming, whitespace, presentation     |
| test:     | Tests or validation                              |
| build:    | Build process or dependency updates              |
| ci:       | GitHub Actions or automation                     |
| perf:     | Performance improvements                         |
| chore:    | Repository maintenance                           |
| adr:      | Architecture Decision Record                     |

---

# Commit Philosophy

A commit should explain **why**, not merely **what**.

Anyone reading the Git history months later should understand the decision that was made.

---

# Extended Commit Description

Whenever practical, include an extended description that answers four questions.

## Decision

What decision was made?

---

## Business Driver

Why was the change necessary?

What problem or opportunity does it address?

---

## Expected Outcome

What capability or behavior should improve?

---

## Impact

Which part of Keystone is affected?

Examples:

* Architecture
* Documentation
* Workflow
* Standards
* UI
* Automation
* Other

---

# Documentation Standards

Documentation should explain:

* Why something exists
* The decision behind it
* How it should be used
* Any important constraints

Documentation should avoid unnecessary implementation detail unless required.

---

# Lessons Learned

When a repeatable improvement is discovered, ask:

> Is this a reusable standard?

If **No**

Leave it in the conversation.

If **Yes**

Promote it into this repository.

---

# Repository Growth Rule

No new Markdown document should be created until the information has been needed at least twice.

This encourages a lean repository and prevents speculative documentation.

---

# Keystone Principle

Project Keystone exists to improve real executive decisions.

If a feature, framework, workflow, or document does not measurably improve an active decision-making process, it should wait until there is demonstrated need.

Real work creates standards.

Standards improve future work.
