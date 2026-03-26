---
name: jicha
description: "Inspection only: run Discipline Commission code review and automated tests on current working tree changes. Use after writing code to check quality before committing."
argument-hint: "[optional focus areas]"
---

# 监察（$jicha）— SWCC Codex Wrapper

This repo-level skill makes the original SWCC workflow directly callable from Codex.

Required execution order:

1. Read `.agents/swcc-runtime.md`.
2. Read `.claude-plugin/skills/jicha/SKILL.md`.
3. Follow the source workflow exactly, but translate Claude-only agent calls using the runtime mapping.
4. Keep all artifact paths and review expectations from the source workflow unchanged.

This wrapper only exposes the existing inspection flow to Codex.

---

$ARGUMENTS
