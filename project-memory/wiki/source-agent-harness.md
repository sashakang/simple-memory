# source: What is an Agent Harness? and How to build a great one

- **Source ID:** SRC-20260430-agent-harness
- **Type:** YouTube video transcript / architecture explainer
- **Author:** Prompt Engineering
- **URL:** https://www.youtube.com/watch?v=nWzXyjXCoCE
- **Published:** 2026-04-30 · **Clipped:** 2026-06-27
- **Raw:** `project-memory/raw/What is an Agent Harness? and How to build a great one!.md`

## What it is

A conceptual architecture explanation of agent harnesses: the fixed runtime around a model that lets it
act, observe results, and iterate. It distinguishes harnesses from frameworks like LangChain/LangGraph:
frameworks are assembled by humans; harnesses ship a working agent loop.

## Nine components named by the source

1. outer while-loop engine,
2. context management and compaction,
3. tools and skills registry,
4. subagent management,
5. built-in skills/primitives,
6. session persistence/memory,
7. dynamic system prompt assembly from files such as `CLAUDE.md` or `AGENTS.md`,
8. lifecycle hooks,
9. permissions and safety.

## Key claims

- Coding agents such as Codex, Cursor, Claude Code, and similar tools are harnesses.
- Modern harnesses assemble prompts dynamically by walking directories for instruction files.
- Hooks are the extensibility point that lets organizations add behavior before/after tool calls without
  changing the harness.
- Session persistence can be append-only JSON or markdown, making resume/crash recovery possible.
- Permission systems must classify commands dynamically and ask for approval before dangerous operations.

## Assessment against the four hard constraints

- **(a) Agent-agnostic:** useful vocabulary. It explains why each target surface may need different hooks,
  prompt files, and permission behavior.
- **(b) Simplistic:** supports keeping memory outside the harness as files where possible, but also shows
  why lifecycle integration matters.
- **(c) Local-first:** compatible with local session/memory files; not a product recommendation.
- **(d) Company-wide installable:** implies installability depends on harness integration points, especially
  hooks and prompt assembly.

## Relevance to this project

The key takeaway is separation of layers. The selected memory architecture is **not** the harness; it is
state plus operations that must fit each harness's prompt assembly, hook, skill, and permission model.

This source strengthens [[concept-agent-agnostic-gap]]: a design that only works because one harness reads
one file name is fragile. A robust rollout needs either an open standard such as [[concept-agent-skills-standard]]
or explicit per-harness shims.

## Wikilinks

[[concept-agent-harness]] · [[concept-agent-agnostic-gap]] · [[concept-agent-skills-standard]] ·
[[candidate-observational-memory]]
