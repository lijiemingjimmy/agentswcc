---
name: zhengyanshi
description: "Pre-task brainstorming: explore problem space, identify ambiguities, propose approaches, get user confirmation before formal consultation. Use when you want to think through a task before committing to a plan."
argument-hint: "task description"
---

# 政研（$zhengyanshi）— SWCC Codex Wrapper

This repo-level skill makes the original SWCC workflow directly callable from Codex.

Required execution order:

1. Read `.agents/swcc-runtime.md`.
2. Read `.claude-plugin/skills/zhengyanshi/SKILL.md`.
3. Follow the source workflow exactly, but translate Claude-only agent calls using the runtime mapping.
4. Keep all artifact paths and user-confirmation pauses from the source workflow unchanged.

This wrapper exposes the standalone pre-research workflow that was previously only available through the Claude plugin layout.

---

$ARGUMENTS
