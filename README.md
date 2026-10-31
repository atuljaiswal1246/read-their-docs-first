# read-their-docs-first

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE)

A Claude Code skill that forces agents to read a project's own docs before making any changes.

## What it does

Don't break conventions you never read. Before editing anything, the agent must:

* **Read the project docs** — `README.md`, `AGENTS.md`, `CLAUDE.md`, `CONTRIBUTING.md`, whatever exists.
* **Note the rules** — coding style, commit conventions, file structure, testing requirements.
* **Follow the conventions** — changes match what the docs say, not assumptions.
* **If docs are missing or unclear, ask** — don't guess.

## Install

```bash
mkdir -p ~/.claude/skills
cp -r read-their-docs-first ~/.claude/skills/read-their-docs-first
```

Load it in your session:

```
/skill read-their-docs-first
```

Or add it to your `CLAUDE.md` so it's active in every session.

## How it works

```
about to edit project
    ↓
agent reads README.md, AGENTS.md, CLAUDE.md, CONTRIBUTING.md
    ↓
agent notes rules (style, commits, structure, tests)
    ↓
agent follows conventions in all changes
    ↓
if docs unclear, agent asks before acting
```

## Why it matters

Ignoring project docs causes:

* Style violations maintainers will reject
* Commit message format rejections
* Files placed in wrong directories
* Broken agent protocols the team already agreed on

## Files

| File | Purpose |
|------|---------|
| `SKILL.md` | The skill — the rule, protocol, and example |

## Contributing

Pull requests welcome. Open an issue to discuss changes first.

## License

MIT