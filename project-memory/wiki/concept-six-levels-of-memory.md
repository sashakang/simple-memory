# concept: The Six Levels of Coding-Agent Memory

A taxonomy from [[source-every-cc-memory-system-compared]] (Simon Scrapes), now cross-checked against
[[source-claude-second-brain-levels]] (Nate Herk). Every memory system answers one question — *how does the
agent pull the right context at the right time?* — and differs on storage, routing/injection, and retrieval.
The levels build on each other; higher is not better, just more capable at more cost.

| Level | What it adds | Storage | Retrieval | Local? | Plain MD? | Our verdict |
|-------|-------------|---------|-----------|--------|-----------|-------------|
| **1 Native** | what ships with Claude Code | `CLAUDE.md` + auto `memory.md` index | always-loaded + agent-read | ✅ | ✅ | passes a–d; underused, not a product |
| **2 Reliable recall** | hook-injected index, reorganize cmd | `.claude/memory/*.md` (general/domain/tools) | session-start hook injects index | ✅ | ✅ | passes a–d; [[candidate-john-pawel-hook-system]] |
| **3 Search by meaning** | semantic recall + auto-inject | OpenClaude 3-layer MD + vector index | `user-prompt-submit` hook, top-3 semantic | ✅ | ✅ | **adds embedding model → strains (b)**; [[candidate-memsearch]] |
| **4 Verbatim recall** | word-for-word, nothing summarized | SQLite + Chroma, symbolic AAAK index | RAG, session-end/pre-compact hooks | ✅ | ❌ | **two DBs + opaque store → fails (b)**; [[candidate-mempalace]] |
| **5 Self-organizing KB** | interconnected second brain | `raw/`+`wiki/` MD (or hosted) | agent reads wiki; Obsidian graph | ✅* | ✅* | research tool, **not operational memory**; [[candidate-karpathy-llm-wiki]] |
| **6 One brain, all tools** | cross-tool shared memory | Postgres on Supabase | MCP + edge functions, any tool | ❌ | ❌ | **only truly cross-tool, but fails (c)**; [[candidate-openbrain]] |

\* Level 5 is local + markdown for the Karpathy/Obsidian path; hosted clone [[candidate-recall]] is neither.

## Why this taxonomy matters to *our* selection

- **Our 4 constraints carve the ladder at level 3.** L1–L2 pass cleanly. From L3 up, each rung trades a
  constraint for recall quality: L3 spends "simplistic" on an embedding model, L4 spends it on two
  databases + a non-readable store, L6 spends "local-first" on Postgres. This is the [[concept-bm25-vs-semantic-recall]]
  tradeoff stated as a ladder.
- **The source's axis is Claude-Code-only.** It never scores candidates on Codex CLI / Cowork reach — our
  hardest constraint (a). So the taxonomy is necessary but not sufficient for us; see [[concept-agent-agnostic-gap]].
- **OM is "Level 2.5":** hook-injected like L2, curated+summarized+budgeted store, but BM25 keyword recall
  instead of L3 semantic vectors — by design, to stay at L2's simplicity while adding L2's missing curation
  discipline. The named escalation if BM25 bites is **[[candidate-memsearch]]** (L3, still plain markdown).
- **Nate Herk's five-level version reinforces restraint.** [[source-claude-second-brain-levels]] puts
  routing files at L1, LLM Wiki at L2, semantic lookup at L3, knowledge graphs at L4, and always-on brains
  at L5. Its strongest contribution is the rule "choose the lowest level that solves the pain," which aligns
  with this project's simplicity constraint.

See [[candidate-observational-memory]] for where OM lands on this ladder and why the decision (deferred)
leans toward not climbing past 2.5.
