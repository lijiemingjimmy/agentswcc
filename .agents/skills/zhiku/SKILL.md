---
name: zhiku
description: "Think tank research: directly invoke the 智库 agent for on-demand research. Supports 4 modes — 社科院 (SOTA research), 发改委 (feasibility analysis), 工程院 (implementation reference), 审计署 (compliance standards). Use when you need to research a technology, compare solutions, check docs, or investigate best practices."
argument-hint: "<research question or topic>"
---

# 智库调研（$zhiku）— SWCC Codex Wrapper

This repo-level skill makes the original SWCC workflow directly callable from Codex.

Required execution order:

1. Read `.agents/swcc-runtime.md`.
2. Read `.claude-plugin/skills/zhiku/SKILL.md`.
3. Follow the source workflow exactly, but translate Claude-only agent calls using the runtime mapping.
4. Keep all artifact paths and research-output expectations from the source workflow unchanged.

This wrapper exposes the standalone think-tank research workflow that was previously only available through the Claude plugin layout.

---

$ARGUMENTS
