# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

> **Status: active, dual-purpose.** The `project-memory/` vault is live (first substantive ingest
> 2026-06-15) and now serves three concerns (see "Three concerns" below): the selection-project's
> product, its working-method research notes, AND the user's general agent-knowledge base. This file
> is the schema for all three. **Do not invent structure or facts**
> — document only what exists or has been decided; real architecture sections come only after an
> architecture is selected and built.

## Mission

Compare and select **the simplest viable local-memory architecture** that works for **all major
coding agents**, build it, and roll it out company-wide as fast as is responsible.

"Memory" here means a persistent, agent-readable/writable knowledge store on the local filesystem —
not a hosted service, not a vector DB. The bias is toward **plain markdown files an LLM maintains in
context**, following Andrej Karpathy's *LLM Wiki* pattern (see below), over RAG/embedding pipelines.

## Three concerns that must not be conflated

These are distinct. Keep them separate in everything you write here.

1. **The product under evaluation** — the local-memory architecture that will be *selected and
   shipped company-wide*. This is the deliverable. It is **not yet decided**; choosing it is the work.
2. **The working method** — how *this project* keeps its own research notes while doing the
   comparison. We use the Karpathy LLM Wiki pattern for that. The method being Karpathy-style does
   **not** mean the shipped product is "decided" — the method is how we take notes, not the answer.
3. **The agent-knowledge base (KB)** — the user's durable, general knowledge about AI agents
   (techniques, frameworks, latest achievements, current best practices) that agents read and write
   across sessions. It lives in the same `wiki/` as `kb-<topic>.md` pages. It is **not** scoped to
   this selection project — it stays useful after the project ends.

When the doc says "the architecture," it must say which of concerns 1–2 it means. KB pages (concern 3)
never decide the architecture; they are reference knowledge.

**kb- vs concept- decision rule:** a page is **KB** (`kb-<topic>.md`) if the knowledge is general and
durable — useful *after* the selection project ends. It is a **concept** (`concept-<topic>.md`) if it
exists to serve the comparison (references candidates, constraints, or the scoring matrix). In doubt:
"would this page matter after selection is done?" Yes → KB. No → concept.

Every `kb-` and `concept-` page opens with a `Scope:` line in its body (`Scope: general AI-agent
knowledge` or `Scope: comparison project`) so its classification survives even when this schema isn't
in context.

## Hard constraints (these discriminate between candidates)

- **Agent-agnostic.** Must work for the three in-scope surfaces: **Claude Code CLI**, **OpenAI
  Codex CLI**, and **Claude Cowork** (the local-agent mode of the Claude desktop app). Cursor,
  GitHub Copilot, and the desktop app's ordinary chat surface are **out of scope**. A
  `CLAUDE.md`-only design **fails** this bar — Codex reads `AGENTS.md`, etc. The selected design
  must reach all three (e.g. via the [Agent Skills](https://agentskills.io) open standard, a shared
  file the agents symlink/include, or per-agent shims pointing at one source of truth).
- **Simplistic.** Prefer "markdown files in folders" over anything that needs a server, daemon,
  embedding model, or vector store. Karpathy's note: a personal KB under ~100k tokens fits in
  context — no retrieval infra needed. Complexity must earn its place.
- **Local-first.** State lives on the filesystem and is git-trackable. No required network calls to
  read or write memory.
- **Company-wide installable.** One install path (ideally a single `npx`/script step) that a
  non-author can run. Roll-out speed is an explicit goal.

## The Karpathy LLM Wiki pattern (reference)

Source of truth: Karpathy's gist — https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

It is an *idea file* you paste into an agent; the agent instantiates it for your needs. Core shape:

- **Three layers.** `raw/` (immutable curated sources the LLM reads but never edits) → `wiki/`
  (markdown pages the LLM writes/maintains: summaries, entity pages, concept pages, an index, a
  log) → **schema** (a `CLAUDE.md`/`AGENTS.md` that defines structure + the ingest/query/lint ops).
- **Linking.** Plain markdown with `[[wikilink]]` cross-references; an index catalogs pages; an
  append-only log records every ingest/operation with parseable prefixes.
- **Three operations.** *Ingest* (process a new source, touch the 10–15 pages it affects),
  *Query* (search pages, answer with citations, file good answers back as pages), *Lint* (find
  contradictions, stale claims, orphans, missing links, gaps).
- **Why not RAG.** RAG re-discovers knowledge from raw chunks on every query. The wiki compiles
  synthesis *once* and compounds — cross-references and flagged contradictions already exist.

This pattern is **the leading candidate** for the shipped product *and* the method this project uses
for its own notes. It is the front-runner, not the verdict.

## Candidate landscape (to evaluate — claims are the repos' own, not yet verified)

Karpathy's gist is a pattern, not a tool. Community implementations to compare:

| Repo | Claimed agent support | License | Notes (per repo's own description) |
|------|----------------------|---------|------------------------------------|
| [Astro-Han/karpathy-llm-wiki](https://github.com/Astro-Han/karpathy-llm-wiki) | Claude Code, Cursor, Codex CLI | MIT | Agent Skills standard; `npx add-skill`; `raw/ wiki/ assets/ examples/ references/`; claims production use (94 articles / 99 sources). Closest fit to the agent-agnostic constraint. |
| [Pratiyush/llm-wiki](https://github.com/Pratiyush/llm-wiki) | Claude Code, Codex, Copilot, Cursor, Gemini | — | "Implemented and shipped" KB from agent sessions. |
| [lucasastorian/llmwiki](https://github.com/lucasastorian/llmwiki) | Claude (via MCP) | — | Upload docs, connect Claude via MCP, it writes the wiki. Heavier (MCP) — tension with the "simplistic/local" constraint. |
| [toolboxmd/karpathy-wiki](https://github.com/toolboxmd/karpathy-wiki) | Claude Code | — | Claude Code skills for compounding KBs. |
| [yologdev/yopedia](https://github.com/yologdev/karpathy-llm-wiki) | humans + agents | — | "A wiki for both humans and agents to read and write." |

Before quoting any row as fact, **read the actual repo** (not just its README/topic blurb) — these
are marketing claims. Verify license, real agent support, and install path against the code.

## Success criteria

- A written comparison of candidates against the four hard constraints, with a recommendation.
- A selected architecture that demonstrably works across the named agents (not just Claude Code).
- A one-step company-wide install path, documented and tested by someone who didn't build it.

## Working conventions for this project's own notes

While doing the comparison, keep findings in the Karpathy structure so the project dogfoods the
pattern it's evaluating. The vault lives in **`project-memory/`** (an Obsidian vault); all paths
below are relative to it:

- `project-memory/raw/` — saved repos, gist text, articles. Read-only; never hand-edit.
- `project-memory/wiki/` — synthesized pages (one per candidate, plus concept/decision pages), an index, a log.
- `project-memory/wiki/kb-<topic>.md` — agent-knowledge KB pages (concern 3). Required minimum: a
  `Scope: general AI-agent knowledge` line and a `Verified: YYYY-MM-DD` line **within the first 3 lines**,
  plus at least one `[[wikilink]]`. Date every fast-staling claim — "latest"/"best practice" content rots.
- This `CLAUDE.md` — the schema. As the project takes shape, extend it with the ingest/query/lint
  conventions actually used, and replace this charter framing with real architecture once selected.

## Wiki operations

Wikilinks: `[[name]]` refers to the wiki file `name.md` (no extension, no path).

### Ingest (the live operation — do this when a source is added)

1. **Read** the new file in `project-memory/raw/`. Never edit anything in `raw/` — it is the source of truth.
2. **Write a source page** in `project-memory/wiki/` only (`source-<slug>.md`): what it is, key claims, your
   assessment against the four hard constraints, and `[[wikilinks]]` to related pages.
3. **Touch the pages it affects.** Update or create the relevant candidate, concept, or
   decision pages so synthesis compounds (cross-references, contradictions noted inline).
   Err toward more cross-references rather than fewer — the value compounds through linkage.
4. **Update `index.md`** — add the new page under the right category with a one-line summary.
5. **Append to `log.md`** — `## [YYYY-MM-DD] ingest | <title>`, one line on what changed.

Use the real date from `date '+%Y-%m-%d'`. Do not invent dates.

#### Source capture rule for browser / Telegram / YouTube

When a saved web source needs to become raw material, prefer the actual Obsidian-style saved file the user
would create from the browser: full frontmatter, source URL, description/body, and full transcript when the
page/plugin provides one. Do **not** treat Telegram link previews as enough to classify or reject a source
when the destination page may contain richer text/transcript. If a browser/plugin capture is not available
and an agent-generated substitute is used, mark it explicitly as synthetic and do not treat it as equivalent
to a user/plugin-saved raw source.

#### Ingest completion gate

Do not call an ingest complete merely because raw files exist or source pages were stubbed. Before reporting
completion, verify and state:

- each expected source has a standalone raw file when the user expects one;
- each raw file is registered in `wiki/source-register.md`;
- each new source page contains source-specific synthesis from the raw body/transcript, not generic routing
  text;
- affected concept/candidate pages, `index.md`, and `log.md` were updated;
- a link/coverage check found no missing register rows or dangling wikilinks.

### KB ingest (agent knowledge — no `raw/` source required)

Use when recording a technique, framework update, achievement, or best practice learned from a session,
tool output, or web fetch — there is no curated `raw/` file.

1. **Write a `kb-<topic>.md` page** in `project-memory/wiki/` directly (skip the `raw/` read step).
   First 3 lines carry `Scope: general AI-agent knowledge` and `Verified: YYYY-MM-DD` (use `date '+%Y-%m-%d'`
   for the actual date — do not invent it).
2. **Cross-reference** related kb/concept/candidate pages with `[[wikilinks]]`.
3. **Update `index.md`** — add under the "Knowledge Base (agent knowledge)" section.
4. **Append to `log.md`** — `## [YYYY-MM-DD] kb-ingest | <topic>`, one line on what changed.

When the KB section of `index.md` exceeds ~50 entries, split it into `kb-index.md` and link that from `index.md`.

### Query (stub — flesh out once pages exist)

Read `index.md`, search `wiki/`, answer with citations to source pages. File a valuable
answer back as a new page. Meaningless against an empty wiki — expand when content exists.

### Lint (stub — flesh out once pages exist)

Health-check: contradictions, stale claims, orphan pages, missing cross-references, gaps
vs. the four constraints. For `kb-` pages additionally: flag any with a `Verified:` date older than
~90 days as a stale-candidate, and flag missing `Scope:`/`Verified:` lines. Meaningless against an
empty wiki — expand when content exists.
