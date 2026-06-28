# concept: The storage × injection × recall matrix

The scoring frame this project uses to compare memory systems. Every candidate decomposes into independent
choices on these axes — the same lens that [[source-every-cc-memory-system-compared]],
[[source-best-claude-memory-system]], and [[source-claude-second-brain-levels]] all converge on: where
memory lives, how it is written, how it enters context, and how it is recalled.

| Axis | Question | Range |
|------|----------|-------|
| **Save trigger** | who decides to write? | hook/automatic ↔ agent-decided |
| **Save form** | what gets stored? | verbatim transcript ↔ curated summary |
| **Injection** | how does it enter context? | hook-loaded (passive) ↔ agent-pulled (MCP/tool); capped ↔ unbounded |
| **Recall** | how is the right memory found? | keyword/BM25 ↔ semantic ↔ hybrid |

## Where the candidates land

- **[[candidate-observational-memory]] (OM):** agent-decided · **curated summary** · hook-loaded + **capped (~24 KB)** · **BM25 keyword**.
- **[[candidate-memsearch]] (L3):** automatic · summarized (OpenClaude daily notes) · hook-loaded passive (top-3) · **semantic**.
- **[[candidate-mempalace]] (L4):** hook (session-end) · **verbatim** · RAG-pulled · semantic (two DBs).
- **[[candidate-openbrain]] (L6):** agent/automatic · chunked+embedded · MCP-pulled · semantic, **remote**.
- **Simon hybrid stack:** automatic summarized capture · Hermes-style capped snapshot injection · hybrid
  keyword+semantic recall + reranking/cited answer · team mode may become remote Supabase. See
  [[source-best-claude-memory-system]].
- **[[candidate-dox-agents-md]]:** mostly a routing/instruction layer, not memory recall: agent-maintained
  folder docs tell the harness where to look before editing.

The two axes the OM decision turns on: **save form / curation** (doubt #2 — OM curates via `om observe` +
`om reflect`) and **recall** (doubt #1 — OM is BM25; see [[concept-bm25-vs-semantic-recall]]). On injection,
OM's *capped passive* design is the anti-[[concept-context-rot]] choice the literature favors.

The Telegram transcript redo adds design vocabulary, not a new scoring axis. [[source-master-all-7-levels-of-claude-code-memory]]
names decay, promotion, multi-signal retrieval, salience, disclosure, compaction, and three injection
approaches: behavior files, hooks, and agent-scoped memory. [[source-l8-principal-s-agentic-engineering-workflow]]
adds the practical split between global memory and project-level memory files. [[source-anthropic-quietly-shipped-the-memory-layer-your-agent-was-missing-buil]]
adds background consolidation/dreaming as a save-form maintenance strategy: useful for repetitive work, risky
if opaque or hosted.

[[concept-six-levels-of-memory]] · [[concept-bm25-vs-semantic-recall]] ·
[[candidate-observational-memory]] · [[concept-agent-harness]] ·
[[source-master-all-7-levels-of-claude-code-memory]] · [[source-l8-principal-s-agentic-engineering-workflow]]
