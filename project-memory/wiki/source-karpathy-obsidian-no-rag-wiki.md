# source: Karpathy's 400,000-Word Obsidian Wiki Has Zero RAG Infrastructure

- **Source ID:** SRC-20260406-karpathy-obsidian-no-rag-wiki
- **Type:** YouTube auto-generated transcript / pattern walkthrough
- **URL:** https://www.youtube.com/watch?v=VUnABqzrZQg
- **Raw:** `project-memory/raw/Karpathy's 400,000-Word Obsidian Wiki Has Zero RAG Infrastructure.md`

## Key claims

The transcript walks through the Karpathy-style LLM Wiki pattern: `raw/` as immutable source inbox,
`wiki/` as the LLM-owned compiled layer, and a schema file that defines ingest/query/lint operations. It
emphasizes source citations, index maintenance, wikilinks, log entries, linting for contradictions and
unsourced claims, and scale caveats.

The source strengthens the wiki as a research and synthesis method. It remains Claude-Code-heavy in the
example and does not prove the pattern as a complete company-wide operational memory product across all
three in-scope surfaces.

## Assessment against hard constraints

- **(a) Agent-agnostic:** pattern-level yes, implementation proof no.
- **(b) Simplistic:** strong below the source-count ceiling described in the transcript.
- **(c) Local-first:** strong: Markdown files and Obsidian/Git-compatible folders.
- **(d) Company-wide installable:** unknown until a specific template/repo is verified.

## Wikilinks

[[candidate-karpathy-llm-wiki]] · [[concept-context-engineering]] ·
[[concept-agent-legibility]] · [[concept-agent-agnostic-gap]]
