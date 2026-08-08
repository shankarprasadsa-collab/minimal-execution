# Minimal Execution

A minimal execution skill for AI coding agents.

## Purpose

Minimal Execution enforces four principles:

1. Do exactly what the user asks.
2. Do not assume missing requirements.
3. Prefer the simplest solution.
4. Stop when the requested work is complete.

## Supported agents

- Cursor
- Claude Code

## Repository structure

```text
minimal-execution/
├── .claude/
│   └── skills/
│       └── minimal-execution/
│           └── SKILL.md
├── .cursor/
│   └── rules/
│       └── minimal-execution.mdc
├── CLAUDE.md
├── README.md
└── SKILL.md
```

`SKILL.md` is the canonical skill definition.

The Claude Code copy is placed in `.claude/skills/minimal-execution/SKILL.md`.

The Cursor rule is placed in `.cursor/rules/minimal-execution.mdc` and is configured to apply always.

## Installation

### Use as a GitHub repository

Push this repository to GitHub, then copy or clone it into the project where you want the behavior applied.

### Cursor

Copy `.cursor/rules/minimal-execution.mdc` into the target repository's `.cursor/rules/` directory.

Cursor project rules are file-based and can be version-controlled with the project. citeturn0search3turn0search9

### Claude Code

Copy `.claude/skills/minimal-execution/` into the target repository's `.claude/skills/` directory.

Keep `SKILL.md` in that directory.

## Design

The package intentionally contains no scripts, dependencies, build system, or runtime code.

It only contains the instructions required to apply Minimal Execution.
