# source: Harness engineering: leveraging Codex in an agent-first world

- **Source ID:** SRC-20260211-openai-harness-engineering-codex
- **Type:** OpenAI engineering article
- **Author:** Ryan Lopopolo
- **URL:** https://openai.com/index/harness-engineering/
- **Published:** 2026-02-11 · **Clipped:** 2026-06-27
- **Raw:** `project-memory/raw/Harness engineering leveraging Codex in an agent-first world.md`

## What it is

An OpenAI engineering article about building an internal software product with Codex agents and no
manually-written code. The most relevant parts for this project are the repository-local knowledge system,
short `AGENTS.md` router, structured docs, mechanical checks, and recurring cleanup.

## Key claims

- Human work shifts from writing code to designing environments, specifying intent, and building feedback
  loops agents can use.
- A "one big `AGENTS.md`" failed: it crowded out relevant context, became non-guidance, rotted quickly, and
  was hard to verify.
- The working pattern is a short `AGENTS.md` treated as a table of contents, with structured `docs/` as the
  system of record.
- The repository knowledge base includes design docs, execution plans, generated schemas, product specs,
  references, quality/security/reliability docs, and indexes.
- Progressive disclosure lets agents start from a small stable entry point and follow pointers to deeper
  sources only when needed.
- Lints and CI validate freshness, cross-links, ownership, and structure; recurring doc-gardening agents open
  fixes for stale or obsolete docs.
- Agent legibility is the goal: knowledge that lives only in chat threads, Google Docs, or people's heads is
  invisible to agents unless moved into accessible local artifacts.

## Assessment against the four hard constraints

- **(a) Agent-agnostic:** Codex-specific evidence, but the pattern is local files and should be portable with
  shims.
- **(b) Simplistic:** strong for knowledge architecture: short router + markdown docs + linters. It does add
  process/tooling for verification.
- **(c) Local-first:** strong. Repository-local, versioned artifacts are central.
- **(d) Company-wide installable:** not a packaged memory product, but it shows what a mature rollout needs:
  structure plus mechanical checks.

## Relevance to this project

This source directly supports [[concept-agent-legibility]]. It also aligns with [[candidate-dox-agents-md]]
but is more mature: DOX proposes a hierarchical `AGENTS.md` tree, while OpenAI's pattern keeps `AGENTS.md`
short and puts durable knowledge in structured docs with validation.

For the local-memory architecture, the key implication is that the install path should create a **map plus
source-of-truth docs**, not one giant instruction/memory file.

## Wikilinks

[[concept-agent-legibility]] · [[concept-context-engineering]] · [[concept-agent-harness]] ·
[[candidate-dox-agents-md]] · [[candidate-karpathy-llm-wiki]]
