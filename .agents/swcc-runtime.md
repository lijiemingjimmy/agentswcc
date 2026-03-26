# SWCC Codex Runtime

This file explains how the repo-level Codex skills should execute the original SWCC workflows that live under `.claude-plugin/`.

## Core Translation Rule

The source skills under `.claude-plugin/skills/*/SKILL.md` are written for Claude Code and use `subagent_type: "swcc:<role>"`.

In Codex, translate each such step like this:

1. Read `.claude-plugin/agents/<role>.md`.
2. Spawn a Codex sub-agent with the mapped `agent_type`.
3. Put the role prompt content first in the spawned agent message.
4. Append the phase-specific task from the source workflow after that role prompt.
5. Save the returned report to the exact file path required by the source workflow before continuing.

Do not preserve the literal `swcc:<role>` namespace. Preserve the workflow semantics instead.

## Role Mapping

| Role | Codex `agent_type` | Prompt Source |
|------|--------------------|---------------|
| `zhongban` | `explorer` | `.claude-plugin/agents/zhongban.md` |
| `zhengyanshi` | `default` | `.claude-plugin/agents/zhengyanshi.md` |
| `zuopai` | `default` | `.claude-plugin/agents/zuopai.md` |
| `youpai` | `default` | `.claude-plugin/agents/youpai.md` |
| `zhongjian` | `default` | `.claude-plugin/agents/zhongjian.md` |
| `dangwei` | `default` | `.claude-plugin/agents/dangwei.md` |
| `guowuyuan` | `explorer` | `.claude-plugin/agents/guowuyuan.md` |
| `buwei` | `worker` | `.claude-plugin/agents/buwei.md` |
| `jiwei` | `default` | `.claude-plugin/agents/jiwei.md` |
| `zhiku` | `default` | `.claude-plugin/agents/zhiku.md` |

## Skill Name Translation

- Treat source references like `/zhili` or `/xieshang` as Codex skill calls such as `$zhili` and `$xieshang`.
- Keep the original seven skill names: `zhili`, `xieshang`, `zhixing`, `jicha`, `juguo`, `zhengyanshi`, `zhiku`.

## Parallelism Rule

- If the source workflow says multiple roles should run in parallel, spawn them before waiting.
- Keep write scopes disjoint for parallel `buwei` workers whenever possible.

## Artifact Rule

- Keep all run artifacts under `.tmp/swcc/`.
- Preserve the exact filenames expected by the source workflow so downstream steps can read them.

## Worker Integration Rule

When a `buwei` worker returns code changes or file guidance:

1. Review the worker output.
2. Apply or integrate the accepted changes in the coordinator workspace.
3. Record the result in the requested `buwei-*.md` artifact.
4. Only then continue to the next SWCC phase.

## Research Rule

- `zhiku` may browse when the current Codex session has web access.
- `zuopai` may also browse if the source workflow calls for SOTA research.
- If browsing is unavailable, continue with local repository evidence plus model knowledge and state that limitation explicitly in the artifact.
