# source: The Complete Guide to Building Skills for Claude

- **Source ID:** SRC-20260627-anthropic-guide-building-skills
- **Type:** PDF guide
- **Author:** Anthropic
- **URL:** https://resources.anthropic.com/hubfs/The-Complete-Guide-to-Building-Skill-for-Claude.pdf?hsLang=en
- **Published:** not stated in raw · **Clipped:** 2026-06-27
- **Raw:** `project-memory/raw/Anthropic Guide to Building Skills.md`

## What it is

An official Anthropic guide to building Claude Skills. The local raw clipping contains only metadata, so this
summary is based on the linked PDF source.

## Key claims

- A skill is a folder with required `SKILL.md` plus optional `scripts/`, `references/`, and `assets/`.
- Skills use progressive disclosure: frontmatter is always visible for routing, the body loads when relevant,
  and linked files are discovered only as needed.
- Anthropic claims skills are portable across Claude.ai, Claude Code, and the API when dependencies are
  supported. This is **Claude-surface portability**, not proof of Codex or Cowork interoperability.
- Good skills start from concrete use cases, define triggers, list needed tools, and establish success
  criteria.
- Skill descriptions must specify what the skill does and when to use it; Anthropic emphasizes trigger
  quality because frontmatter is the first routing layer.
- Testing should cover triggering, functional behavior, and edge cases; more widely deployed skills need more
  rigorous validation.

## Assessment against the four hard constraints

- **(a) Agent-agnostic:** useful but insufficient. The guide supports Claude surfaces, not the three-surface
  project bar that includes Codex CLI and Cowork.
- **(b) Simplistic:** strong for an operation layer: plain folders and markdown, with optional scripts/assets.
- **(c) Local-first:** compatible when skills are local files, though the guide is about Claude product
  behavior rather than a filesystem memory store.
- **(d) Company-wide installable:** promising for Claude enterprise/team rollout, but not yet a tested
  company-wide installer across this project's target harnesses.

## Relevance to this project

This source is stronger evidence than [[source-agent-skills-standard]] for skill structure and progressive
disclosure. It does not decide the memory-store architecture, but it supports packaging ingest/query/lint
operations as a small, testable skill or skill-like shim.

## Wikilinks

[[concept-agent-skills-standard]] · [[concept-context-engineering]] · [[concept-agent-agnostic-gap]]
