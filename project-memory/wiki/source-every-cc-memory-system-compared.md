# source: Every Claude Code Memory System Compared (So You Don't Have To)

- **Type:** YouTube video transcript
- **Author:** Simon Scrapes ([[source-best-claude-memory-system]] is by the same author)
- **URL:** https://www.youtube.com/watch?v=UHVFcUzAGlM
- **Published:** 2026-04-23 · **Clipped:** 2026-06-15
- **Raw:** `raw/Every Claude Code Memory System Compared (So You Don't Have To).md`

## What it is

A survey video that frames every Claude Code memory system as answering one question — *"when you
give Claude a task, how does it pull the right context at the right time?"* — and sorts the field
into **six levels** that build on each other. Each level is distinguished by just two axes: **where
memory lives** (storage) and **how Claude gets it** (retrieval). This is the same storage×retrieval
lens used in [[concept-storage-injection-recall-matrix]].

## The six levels (the spine of the source)

| Level | Name | Storage | Retrieval | Representative tool |
|-------|------|---------|-----------|---------------------|
| 1 | Native | `CLAUDE.md` + `memory.md` (markdown, indexed) | always-loaded / agent-read | ships with Claude Code |
| 2 | Reliable recall | `.claude/memory/` (general + domain + tools `.md`) | **session-start hook** injects the index | [[candidate-john-pawel-hook-system]] |
| 3 | Search by meaning | OpenClaude 3-layer markdown (memory.md + daily notes + dreaming) | **semantic vectors**, `user-prompt-submit` hook auto-injects top-3 | [[candidate-memsearch]] |
| 4 | Verbatim recall | SQLite (entities) + Chroma vector DB; symbolic "AAAK" index over wing/room/drawer | RAG, session-end / pre-compact hooks | [[candidate-mempalace]] |
| 5 | Self-organizing KB | `raw/` + `wiki/` plain markdown (read-vs-write split) | agent reads wiki; Obsidian graph for humans | [[candidate-karpathy-llm-wiki]], [[candidate-recall]], LightRAG |
| 6 | One brain for all tools | **Postgres on Supabase** (`thoughts` table: text+embedding+tags) | MCP server + edge functions; any tool queries | [[candidate-openbrain]], [[candidate-mem0]] |

## Key claims

- **Context rot is the core problem.** LLMs can't reliably recall 100% of a large loaded context, so
  the win is loading the *right* context at the *right time*, not loading more. Rule of thumb: keep
  `CLAUDE.md` under ~200 lines; push bulky context to referenced files loaded on demand.
- **Level 1 is underused, not absent.** Claude Code already ships `CLAUDE.md` *and* an auto `memory.md`
  that quietly indexes per-project notes. Anthropic's leaked-source "**Kairos**" is an unreleased
  always-on daemon that consolidates notes in the background — i.e. Anthropic is actively closing this gap.
- **Level 2 = hook-injected index.** John Connolly's implementation of Pawel Huryn's pattern adds a
  big memory-management prompt to `CLAUDE.md` + a session-start hook that injects only the `memory.md`
  *index* (not full content). Supports a "reorganize memory" command that dedups/merges/prunes/re-sorts.
- **Level 3 = OpenClaude architecture ported to Claude Code by `memsearch` (Zilliz, the Milvus team).**
  Two-line plugin install; chunks markdown into semantic vectors; `user-prompt-submit` hook auto-injects
  top-3 semantic matches; keeps everything in **readable markdown**. Contrast **claude-mem**: MCP-based
  (pull, not passive-inject), stores opaquely in the background, more features (dashboard, team, cost
  tracking) — judged "overkill" and *not* plain-markdown-readable.
- **Level 4 = `mempalace`**: verbatim, never-summarized recall; "highest benchmark of any memory system
  ever published" (the source's hedge: "apparently"). Two DBs (SQLite + Chroma). **Downside: not
  readable markdown** — the verbatim text lives behind the index, not on disk as prose.
- **Level 5 = Karpathy LLM Wiki** (and hosted clone **Recall**, and heavyweight **LightRAG**). The author
  is explicitly **lukewarm on level 5 for *operational* memory** — sees it as a *deep-research / second-brain*
  tool ("a Wikipedia on a topic"), not for "what did we decide about client X in March." Recall = zero-setup
  hosted but you don't own the data + it's consumption-oriented, not operational. LightRAG = enterprise overkill.
- **Level 6 = OpenBrain (Nate Jones)**: Postgres-on-Supabase brain, one `thoughts` table, MCP front door so
  ChatGPT/Codex/Cursor/Claude all share one memory. ~$0–0.30/mo, but **not local**, adds query latency,
  longest setup. **mem0** = the well-funded hosted cross-tool alternative (data lives on their servers).
- **The author's own pick: Level 3 (memsearch).** He runs levels 1+2+3 stacked in his "Agentic OS" —
  OpenClaude conventions + semantic search + injection hooks. Notes levels 1–3 stack cleanly (similar
  folder structure). Verdict heuristic: start L1 → L2 ("most should stop here") → L3/L4 only at scale →
  L5/L6 only for research / cross-tool needs.

## Assessment against the four hard constraints

This source is the most useful map yet for *placing* candidates on our constraints — and several of its
levels are **disqualified by our own bar**, which sharpens the OM case:

- **(a) Agent-agnostic (3 surfaces).** The source is **Claude-Code-centric**; levels 1–5 are all framed
  around Claude Code only. *Only* level 6 (OpenBrain/mem0) is genuinely cross-tool — and it gets there by
  abandoning local-first (constraint c). This is the source's blind spot vs. our charter: it never asks
  "does this also work in Codex CLI / Cowork?" → see [[concept-agent-agnostic-gap]].
- **(b) Simplistic.** The source's own complexity ladder maps almost 1:1 onto our "complexity must earn
  its place" bar. L1–L2 (plain markdown + a hook) pass cleanly. L3 (memsearch) adds an embedding model;
  L4 (mempalace) adds **two databases**; L6 adds **Postgres**. Each step buys recall quality at the cost
  of our simplicity constraint — the central tradeoff in [[concept-bm25-vs-semantic-recall]].
- **(c) Local-first.** L1–L5 are local; **L6 fails** (Supabase, network query every read). Recall (L5
  hosted) also fails. This confirms cross-tool reach and local-first are in tension *unless* you use a
  shared local file + per-agent shims (OM's approach) rather than a shared remote DB.
- **(d) Company-wide installable.** L2 two-prompt setup, L3 two-line plugin install = easy. L6 = "30–45
  min, non-trivial." The simpler levels win the install bar too.

## Relevance to the OM decision (the live question)

This source **does not mention [[candidate-observational-memory]]** (OM) by name, but it strongly
*frames* the OM tradeoff:

1. **OM sits at "Level 2.5."** It is hook-injected (L2) with a curated, summarized store and a budgeted
   context payload — but its recall is **BM25 keyword**, deliberately *not* the L3 semantic vectors. This
   source is the clearest articulation of what OM gives up: the L2→L3 jump is exactly "keyword search
   starts falling apart as you scale." → feeds doubt #1 in [[concept-bm25-vs-semantic-recall]].
2. **memsearch is the named L3 upgrade path** if BM25 proves insufficient — and it stays plain-markdown,
   the least-invasive way to add semantic recall. Strongest single alternative this source surfaces for
   our doubt #1. But it's Claude-Code-only (plugin), so it fails constraint (a) without extra work.
3. **Curation (doubt #2):** the source's L2 "reorganize memory" and L3 "dreaming" (promote recurring
   notes, forget stale ones) are the *same* primitives OM ships as `om reflect` + staleness tracking +
   conflict-check. So on curation the field has converged — OM is not behind here.

**Net:** nothing here dislodges OM; it sharpens the one real doubt (BM25 vs semantic) and names
**memsearch** as the concrete, markdown-preserving escalation if that doubt ever bites. Decision itself
stays unrecorded per the standing instruction.

## Wikilinks

[[source-best-claude-memory-system]] · [[candidate-observational-memory]] · [[candidate-memsearch]] ·
[[candidate-mempalace]] · [[candidate-openbrain]] · [[candidate-mem0]] · [[candidate-recall]] ·
[[candidate-john-pawel-hook-system]] · [[candidate-karpathy-llm-wiki]] ·
[[concept-six-levels-of-memory]] · [[concept-storage-injection-recall-matrix]] ·
[[concept-bm25-vs-semantic-recall]] · [[concept-agent-agnostic-gap]] · [[concept-context-rot]]
