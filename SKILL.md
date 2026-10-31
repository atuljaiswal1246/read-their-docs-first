---
name: read-their-docs-first
description: Read the project's own docs before making any changes. Don't break conventions you never read.
metadata:
  source: owner, 2026-10-31
  verified: false
---

# read-their-docs-first

## Core rule

Before making any changes to a project, read its own documentation first — `README.md`, `AGENTS.md`, `CLAUDE.md`, `CONTRIBUTING.md`, and any local guides. Don't break conventions you never read.

## Protocol

Before editing anything:

1. **Read the project docs.** `README.md`, `AGENTS.md`, `CLAUDE.md`, `CONTRIBUTING.md` — whatever exists.
2. **Note the rules.** Coding style, commit conventions, file structure, testing requirements, agent behavior expectations.
3. **Follow the conventions.** Your changes must match what the docs say, not what you assume.
4. **If docs are missing or unclear,** ask before acting rather than guessing.

## Why

Ignoring project docs causes:
- Style violations the maintainers will reject
- Commit message format rejections
- File placement in wrong directories
- Breaking agent protocols the team already agreed on

## Gate

No changes until the docs are read. If the project has rules and you never read them, stop and read them first.

## Example

```
Project AGENTS.md says:
- All commits must include a scope: "feat(header): add toggle"
- Tests must pass before any commit

You must follow both — not just write code and push.
```

Read the docs, then write the code — never the other way around.