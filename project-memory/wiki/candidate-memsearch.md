# candidate: memsearch (Zilliz)

- **Repo:** https://github.com/zilliztech/memsearch
- **Level:** 3 (search by meaning) in [[concept-six-levels-of-memory]]
- **Source:** [[source-every-cc-memory-system-compared]]

## What it is

A Claude Code **plugin** (two-line install) by Zilliz — the team behind the Milvus vector DB — that ports
**OpenClaude's** memory architecture into Claude Code. Keeps OpenClaude's markdown-first design: a durable
`memory.md` + per-date daily notes, same chunking strategy, all **readable markdown on disk**. Adds:

- **Semantic recall**: chunks everything you write into vectors; searches by *meaning*, not keywords.
- **Auto-injection**: a `user-prompt-submit` hook feeds the **top-3 semantic matches** into context as you
  type — no need to ask Claude to search. Installs a `memory recall` skill / slash command too.

## Against our four constraints

- **(a) Agent-agnostic:** ❌ as-shipped — it's a **Claude Code plugin**. No native Codex CLI or Cowork path.
  Would need shimming to reach the other two surfaces. This is its main loss vs [[candidate-observational-memory]].
- **(b) Simplistic:** ⚠️ adds an **embedding model + vector index** — the L2→L3 cost. But stays plain markdown
  and is a 2-line install, so it's the *least-invasive* way to buy semantic recall.
- **(c) Local-first:** ✅ local files, local vectors.
- **(d) Installable:** ✅ `/plugin marketplace add zilliztech memsearch` + `/plugin install memsearch`.

## Why it matters to the OM decision

This is the **named upgrade path** if OM's BM25 keyword recall proves insufficient
([[concept-bm25-vs-semantic-recall]], doubt #1). It answers "what if keyword search isn't good enough?"
while preserving the markdown-readability we care about. The price is constraint (a): you'd have to add
Codex/Cowork reach yourself. **Strongest single alternative** surfaced for doubt #1.

Contrast **claude-mem** (also L3-ish): MCP-based (pull, not passive inject), opaque background store (not
readable markdown), more features (dashboard/team/cost) — judged overkill by the source.

[[source-best-claude-memory-system]] strengthens memsearch's case on recall: the source argues that semantic
or hybrid search is what lets a user find a memory when they cannot remember the exact wording. But
[[source-claude-second-brain-levels]] adds a counterweight: vector chunk retrieval can miss tasks that require
reading a whole source document. Net: memsearch remains the escalation path for observed vocabulary-drift
misses, not the default.

[[candidate-observational-memory]] · [[concept-bm25-vs-semantic-recall]] · [[concept-six-levels-of-memory]]
