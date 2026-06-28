# source: One markdown file just fixed AI coding forever

- **Source ID:** SRC-20260608-dox-agents-md-framework
- **Type:** YouTube video transcript / repo overview
- **Author:** Agent Zero
- **URL:** https://www.youtube.com/watch?v=NVkRkioBXQc&t=28s
- **Repo claimed by source:** https://github.com/agent0ai/dox
- **Published:** 2026-06-08 · **Clipped:** 2026-06-27
- **Raw:** `project-memory/raw/One markdown file just fixed AI coding forever..md`

## What it is

An overview of DOX, a self-documenting `AGENTS.md` framework. DOX attaches concise markdown docs to
meaningful folders in a codebase, creating a tree of local `AGENTS.md` files that an agent follows before
editing code.

## Key claims

- The root problem is context awareness, not raw model intelligence or larger context windows.
- DOX uses local markdown only: no package, server, database, vector store, or install step beyond copying
  the root instructions into `AGENTS.md`.
- Each folder-level doc records purpose, ownership, local rules/contracts, work guidance, verification, and
  child docs.
- The agent reads the applicable doc chain from root to target folder, edits the code, then updates relevant
  docs so the map stays current.
- The author demonstrates initialization with Codex CLI: paste the framework into `AGENTS.md`, ask Codex to
  initialize the index, and it writes subordinate docs.
- The source claims compatibility with any agent that supports `AGENTS.md`.

## Assessment against the four hard constraints

- **(a) Agent-agnostic:** fails as stated for this project if it is truly `AGENTS.md`-only. Claude Code uses
  `CLAUDE.md`, and Cowork needs its own local-agent path. It could become agent-agnostic only with shims or
  mirrored root instructions.
- **(b) Simplistic:** very strong. Plain markdown, local folder docs, no daemon or retrieval infrastructure.
- **(c) Local-first:** strong. State is filesystem markdown and git-trackable.
- **(d) Company-wide installable:** potentially strong for repos that accept a paste/init workflow; not yet
  a tested one-step company installer.

## Relevance to this project

DOX is not a full personal/company memory system. It is closer to **codebase routing memory**: it tells the
agent where to look and how to behave in a repository. That makes it relevant to [[concept-context-rot]] and
the local shim layer, but it does not replace a persistent user/project memory store.

It may be a useful component or adjacent candidate if the selected architecture needs hierarchical local
instructions. See [[candidate-dox-agents-md]].

## Wikilinks

[[candidate-dox-agents-md]] · [[concept-context-rot]] · [[concept-agent-agnostic-gap]] ·
[[concept-agent-harness]]
