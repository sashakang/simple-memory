# source: I Built The Best Claude Memory System (Beats Hermes)

- **Source ID:** SRC-20260610-best-claude-memory-system
- **Type:** YouTube video transcript
- **Author:** Simon Scrapes
- **URL:** https://www.youtube.com/watch?v=H9BUkgDf5Y4
- **Published:** 2026-06-10 · **Clipped:** 2026-06-11
- **Raw:** `project-memory/raw/I Built The Best Claude Memory System (Beats Hermes).md`

## What it is

A practitioner architecture talk that decomposes AI memory into three jobs: **storage**, **injection**,
and **recall**. The author argues no single surveyed framework handles all three well, so his system
combines pieces from memsearch/memarch, Hermes, and GBrain-style cited-answer retrieval.

## Key claims

- Claude Code's baseline memory is framed as agent-decided summarized storage, always-loaded but
  unbounded injection, and weak/no search recall.
- The proposed storage layer is automatic summarized capture: a hook summarizes each turn into daily
  memory files with a cheap model, avoiding reliance on the main agent noticing what matters.
- The proposed injection layer borrows Hermes' frozen startup snapshot: identity/profile/recent memories,
  capped around a small token budget and cached per session.
- The proposed recall layer combines local vector indexing, hybrid keyword+semantic search, a reranker,
  and a cited written answer rather than returning raw chunks.
- For teams, the source presents two modes: per-person local indexes built only from synced allowed files,
  or a shared Supabase/Postgres store with row-level security for a true shared brain.
- The source claims the stack can be used with Claude Code, Codex, and "any other harness," but does not
  show a public repo or surface-specific install proof in the transcript.

## Assessment against the four hard constraints

- **(a) Agent-agnostic:** conceptually aware of multiple harnesses, but the transcript does not prove support
  for Claude Code CLI, OpenAI Codex CLI, and Claude Cowork. Treat as **unverified**.
- **(b) Simplistic:** weaker fit. The personal architecture adds hooks, summarization, a vector index,
  hybrid retrieval, reranking, and answer synthesis. This is a coherent system, but not "plain markdown
  files an LLM maintains in context."
- **(c) Local-first:** mixed. The personal vector index is described as local; the scalable team design
  moves to Supabase/Postgres and fails local-first for the selected-product bar.
- **(d) Company-wide installable:** the author claims a one-line install in his operating system, but the
  transcript alone is not enough evidence.

## Relevance to this project

This source reinforces [[concept-storage-injection-recall-matrix]] as the right scoring frame. It also
strengthens the semantic-recall side of [[concept-bm25-vs-semantic-recall]]: the author explicitly values
finding memories when the user cannot remember the exact words. But it does **not** dislodge
[[candidate-observational-memory]], because it pays more complexity than this project wants and its
cross-surface support is not source-verified.

The team-mode discussion is important but cuts against the charter: a shared remote DB solves access
control and collaboration, while this project is intentionally looking for a local-first, git-trackable
filesystem architecture.

## Wikilinks

[[concept-storage-injection-recall-matrix]] · [[concept-bm25-vs-semantic-recall]] ·
[[concept-agent-agnostic-gap]] · [[candidate-observational-memory]] · [[candidate-memsearch]] ·
[[candidate-openbrain]]
