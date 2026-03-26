# SWCC Repo-Level Skills

This repository exposes Codex-discoverable SWCC skills under `.agents/skills/`.

## Source Of Truth

- Keep the editable workflow source in `.claude-plugin/skills/*/SKILL.md`.
- Keep the editable role prompts in `.claude-plugin/agents/*.md`.
- Treat `.agents/swcc-runtime.md` as the Codex compatibility layer that explains how to translate the Claude-side agent calls into Codex sub-agent work.

## Available Repo-Level Skills

- `zhili`
- `xieshang`
- `zhixing`
- `jicha`
- `juguo`
- `zhengyanshi`
- `zhiku`

## Usage Rule

When one of the SWCC skills is invoked in Codex:

1. Read `.agents/swcc-runtime.md`.
2. Read the matching source workflow from `.claude-plugin/skills/<skill>/SKILL.md`.
3. Keep the source workflow steps, artifact names, and pause/continue behavior.
4. Translate Claude-only `swcc:<role>` agent calls using the runtime mapping instead of treating them as literal tool names.

The repo-level skill wrappers exist only to make SWCC discoverable and callable in Codex without changing the original Claude plugin layout.
