---
name: zhixing
description: "Execute only: run State Council task decomposition, Discipline Commission task review, Ministry execution, and multi-dimensional review. Use when you already have a plan (from $xieshang or your own) and want to execute it."
argument-hint: "[plan description] or empty to use existing dangwei-decision.md"
---

# 执行（$zhixing）— SWCC Codex Wrapper

This repo-level skill makes the original SWCC workflow directly callable from Codex.

Required execution order:

1. Read `.agents/swcc-runtime.md`.
2. Read `.claude-plugin/skills/zhixing/SKILL.md`.
3. Follow the source workflow exactly, but translate Claude-only agent calls using the runtime mapping.
4. Keep all artifacts, retry behavior, and output filenames from the source workflow unchanged.

This wrapper only adapts the execution workflow for Codex; it does not change the SWCC process itself.

---

$ARGUMENTS
