# source: Claude Code Works Better With Loops, Not Prompts

- **Source ID:** SRC-20260624-claude-code-works-better-with-loops-not-pr
- **Type:** YouTube auto-generated transcript
- **URL:** https://www.youtube.com/watch?v=D7TIvqtSZQE
- **Raw:** `project-memory/raw/Claude Code Works Better With Loops, Not Prompts.md`

## What it is

A transcript-backed loop-engineering tutorial for Claude Code workflows. The description names the loop as orchestrator -> executioner -> reviewer and lists trigger, worktree, skills, connectors, memory, and subagents as building blocks.

## Transcript-backed takeaways

- The useful operational pattern is a self-correcting loop with separate execution and review roles rather than one long prompt.
- The source explicitly includes memory/state as a loop component, with GitHub Issues suggested as a state layer so iterations are logged and resumable.
- Worktrees matter because parallel or repeated agent work needs isolated state to avoid corrupting the main workspace.
- The Loopmaker skill is presented as a portable scaffold with a human gate, which is the right shape for high-risk automation.
- For this wiki, the natural loop targets are mechanical: raw/register drift, broken links, missing index entries, stale questions, and source coverage checks.

## Relevance to the memory project

Directly updates [[concept-loop-engineering]]. It supports loops as a maintenance mechanism for memory, not as the memory architecture itself.

## Assessment against the four hard constraints

- Claude Code focus means agent-agnostic support is not proven.
- GitHub Issues as state is legible but may be heavier than a plain local markdown log for this project.
- Human gates are necessary before any loop rewrites durable wiki synthesis.

## Wikilinks

[[concept-loop-engineering]] · [[concept-agent-harness]] · [[concept-agent-legibility]]
