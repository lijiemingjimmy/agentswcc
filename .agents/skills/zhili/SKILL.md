---
name: zhili
description: "Full pipeline democratic centralism orchestration: task triage → brainstorming → CPPCC consultation → Party Committee decision → inspection → execution → multi-dimensional review. Use when you have a coding task that needs multi-agent planning and execution."
argument-hint: "[--scale 小|中|大] task description"
---

# 治理（$zhili）— SWCC Codex Wrapper

This repo-level skill makes the original SWCC workflow directly callable from Codex.

Required execution order:

1. Read `.agents/swcc-runtime.md`.
2. Read `.claude-plugin/skills/zhili/SKILL.md`.
3. Follow the source workflow exactly, but translate Claude-only agent calls using the runtime mapping.
4. Keep all artifacts, pause points, retry rules, and output filenames from the source workflow unchanged.

Do not redesign the workflow in this wrapper. This wrapper only adapts the Claude plugin skill into a Codex repo-level skill.

---

$ARGUMENTS
