# source: Effective context engineering for AI agents

- **Source ID:** SRC-20260627-effective-context-engineering
- **Type:** Anthropic engineering article
- **Author:** Anthropic Applied AI team
- **URL:** https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents
- **Published:** not stated in raw · **Clipped:** 2026-06-27
- **Raw:** `project-memory/raw/Effective context engineering for AI agents.md`

## What it is

An official Anthropic article defining context engineering as the work of curating the tokens available to an
LLM at each step of an agent run.

## Key claims

- Context engineering is broader than prompt engineering: it includes system instructions, tools, MCP,
  external data, message history, retrieved context, and notes.
- Context is finite and has diminishing returns because of attention scarcity and context rot.
- The goal is the smallest high-signal context set that maximizes the desired outcome.
- Just-in-time context is often better than preloading everything. Agents can keep lightweight identifiers
  such as file paths, stored queries, and links, then retrieve data at runtime.
- File hierarchy, names, and timestamps provide useful metadata for agent navigation.
- Long-horizon work needs compaction, structured note-taking/agentic memory, and sometimes subagents.
- Claude Code is described as using a hybrid model: `CLAUDE.md` is loaded up front, while tools like glob/grep
  retrieve files just in time.

## Assessment against the four hard constraints

- **(a) Agent-agnostic:** mostly conceptual; examples are Claude-heavy.
- **(b) Simplistic:** strongly supports simple references, files, and notes before heavier retrieval.
- **(c) Local-first:** compatible with local files and note-taking, though the article is not a product design.
- **(d) Company-wide installable:** not addressed.

## Relevance to this project

This is the strongest official support for [[concept-context-rot]] and [[concept-context-engineering]]. It
backs the local-memory bias: store durable knowledge externally, load only the right slice, and let agents
navigate structured files instead of dumping a giant memory into context.

## Wikilinks

[[concept-context-engineering]] · [[concept-context-rot]] · [[concept-agent-harness]] ·
[[concept-agent-legibility]] · [[candidate-observational-memory]]
