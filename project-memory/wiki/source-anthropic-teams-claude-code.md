# source: How Anthropic Teams ACTUALLY use Claude Code day to day

- **Source ID:** SRC-20260605-anthropic-teams-claude-code
- **Type:** YouTube auto-generated transcript / practice commentary
- **URL:** https://www.youtube.com/watch?v=l4mSSN6exGg
- **Raw:** `project-memory/raw/How Anthropic Teams ACTUALLY use Claude Code day to day (for non-engineers).md`

## Key claims

The transcript describes context/memory files, skills, reference folders, narrow repeatable tasks, focused
sub-agents, checkpoints, and fresh starts. It treats context files and skills as operational routing: define
who the user is, how they work, what repeatable process should run, and what reference material should load
only when needed.

This is secondary commentary about Anthropic team practice. It reinforces [[concept-context-engineering]] and
[[concept-agent-skills-standard]], but official Anthropic material should remain the stronger source for
specific claims.

## Assessment against hard constraints

- **(a) Agent-agnostic:** weak; Claude Code practice does not prove Codex/Cowork support.
- **(b) Simplistic:** strong as a practice pattern: small context files, short skills, reference folders.
- **(c) Local-first:** compatible with local files, but not itself a memory architecture.
- **(d) Company-wide installable:** suggests repeatable workflows, but no tested installer.

## Wikilinks

[[concept-context-engineering]] · [[concept-agent-skills-standard]] · [[concept-agent-legibility]]
