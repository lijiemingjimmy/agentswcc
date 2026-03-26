---
name: juguo
description: "Emergency mode: skip all consultation, execute all agents in maximum parallelism, fast verification only. Use for urgent bug fixes or tasks where the solution is already clear."
argument-hint: "task description"
---

# 举国体制（$juguo）— SWCC Codex Wrapper

This repo-level skill makes the original SWCC workflow directly callable from Codex.

Required execution order:

1. Read `.agents/swcc-runtime.md`.
2. Read `.claude-plugin/skills/juguo/SKILL.md`.
3. Follow the source workflow exactly, but translate Claude-only agent calls using the runtime mapping.
4. Keep all artifact paths, emergency-mode constraints, and retry limits from the source workflow unchanged.

This wrapper only adapts the existing emergency workflow into a Codex repo-level skill.

---

$ARGUMENTS
