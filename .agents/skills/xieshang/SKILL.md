---
name: xieshang
description: "Consultation only: run brainstorming + CPPCC left-right debate and Party Committee decision without code execution. Use when you want to see the plan before committing to execution."
argument-hint: "task description"
---

# 协商（$xieshang）— SWCC Codex Wrapper

This repo-level skill makes the original SWCC workflow directly callable from Codex.

Required execution order:

1. Read `.agents/swcc-runtime.md`.
2. Read `.claude-plugin/skills/xieshang/SKILL.md`.
3. Follow the source workflow exactly, but translate Claude-only agent calls using the runtime mapping.
4. Keep all artifacts, user-confirmation pauses, and output filenames from the source workflow unchanged.

This wrapper exists only to expose the existing SWCC consultation workflow as a Codex repo-level skill.

---

$ARGUMENTS
