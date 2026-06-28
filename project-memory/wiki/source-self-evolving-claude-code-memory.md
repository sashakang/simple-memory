# source: I Built Self-Evolving Claude Code Memory w/ Karpathy's LLM Knowledge Bases

- **Source ID:** SRC-20260406-self-evolving-claude-code-memory
- **Type:** YouTube auto-generated transcript / implementation walkthrough
- **URL:** https://www.youtube.com/watch?v=7huCP6RkcY4
- **Raw:** `project-memory/raw/I Built Self-Evolving Claude Code Memory w- Karpathy's LLM Knowledge Bases.md`

## Key claims

The transcript applies Karpathy's raw -> wiki -> schema pattern to internal coding-agent history. Session
logs act as raw material, hooks summarize conversations, a daily flush promotes lessons into a wiki, and
session-start loads `AGENTS.md` plus the wiki index so the agent can route into prior decisions and lessons.

This strengthens [[candidate-karpathy-llm-wiki]] as an operational-memory ingredient, but the described
implementation is Claude Code / Claude Agent SDK centered. It does not prove portability to Codex CLI or
Claude Cowork.

## Assessment against hard constraints

- **(a) Agent-agnostic:** weak until hooks and session-start loading are ported beyond Claude Code.
- **(b) Simplistic:** moderate/strong: local files and indexes, but hooks plus an SDK-driven promotion loop
  add moving parts.
- **(c) Local-first:** strong if the logs/wiki remain on disk and do not require hosted state.
- **(d) Company-wide installable:** unknown until the implementation/template is verified.

## Wikilinks

[[candidate-karpathy-llm-wiki]] · [[concept-context-engineering]] · [[concept-agent-legibility]] ·
[[concept-agent-agnostic-gap]]
