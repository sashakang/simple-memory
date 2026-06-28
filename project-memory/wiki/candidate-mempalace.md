# candidate: mempalace

- **Repo:** https://github.com/MemPalace/mempalace · site: mempalace.official.com
- **Level:** 4 (verbatim recall) in [[concept-six-levels-of-memory]]
- **Source:** [[source-every-cc-memory-system-compared]]

## What it is

A **local RAG** system for word-for-word conversation recall. Nothing is ever summarized, so (in theory)
nothing is lost. Uses the "memory palace" metaphor — wings (people/projects/topics) → rooms (sessions/threads)
→ closets (topics/bundles) → **drawers** (verbatim text). A dense symbolic index language ("**AAAK**") lets the
LLM scan thousands of drawers in one pass; retrieval is claimed at ~42 ms. Two databases: **SQLite** (entities
+ relationships) + **Chroma** (vector chunks). Hooks fire on **session-end** and **pre-compact** to file/index
silently; a `mine` function back-fills from past sessions. One-command install registers the hooks.

Claimed "**highest benchmark of any memory system ever published**" (source hedges: "apparently").

## Against our four constraints

- **(a) Agent-agnostic:** ❌ Claude-Code hook–oriented; no Codex/Cowork path described.
- **(b) Simplistic:** ❌ **two databases (SQLite + Chroma) + a symbolic index DSL** — well past "markdown in folders."
- **(c) Local-first:** ✅ fully local.
- **(d) Installable:** ✅ one command, but heavier footprint.
- **Readable store:** ❌ verbatim text lives behind the index, not as on-disk prose.

## Verdict for us

Disqualified on (b): it solves a problem (verbatim recall) we don't have, at a complexity cost our charter
forbids. Relevant only as the field's answer to "I need the *exact words* from a past decision" — orthogonal
to OM's curated-summary approach. Not a contender against [[candidate-observational-memory]].

[[concept-six-levels-of-memory]] · [[concept-bm25-vs-semantic-recall]]
