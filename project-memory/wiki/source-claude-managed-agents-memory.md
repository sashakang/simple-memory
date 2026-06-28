# source: Claude Just Turned Agent Memory Into A Filesystem

- **Source ID:** SRC-20260424-claude-managed-agents-memory
- **Type:** YouTube auto-generated transcript / product commentary
- **URL:** https://www.youtube.com/watch?v=EQWEAUumEAw
- **Raw:** `project-memory/raw/Claude Just Turned Agent Memory Into A Filesystem.md`

## Key claims

The transcript says Anthropic managed-agent memory mounts a regular filesystem at `/mnt/memory`, with
directories and text files read and written through normal shell tools instead of a special model memory API
or vector database. It emphasizes versioning, export/redaction, workspace-scoped shared stores, and
auditability.

The same transcript names important limitations: beta status, Anthropic infrastructure lock-in, no built-in
semantic search, prompt-injection risk for writable memory, and session-start-only mounts.

## Assessment against hard constraints

- **(a) Agent-agnostic:** weak. The source is Claude-platform-specific and distinguishes managed agents from
  Claude Code / Claude Cowork.
- **(b) Simplistic:** strong at the agent interface because it is file-shaped; weaker operationally because
  the storage is a managed platform API.
- **(c) Local-first:** fails as a shipped local-memory product because the transcript says the files live in
  Anthropic managed infrastructure, even if export is possible.
- **(d) Company-wide installable:** unknown for this project's scope.

## Wikilinks

[[candidate-anthropic-managed-agents-memory]] · [[concept-agent-legibility]] ·
[[concept-context-engineering]] · [[concept-agent-agnostic-gap]]
