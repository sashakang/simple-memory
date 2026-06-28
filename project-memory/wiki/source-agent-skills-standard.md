# source: Anthropic, OpenAI, and Microsoft Just Agreed on One File Format

- **Source ID:** SRC-20260330-agent-skills-standard
- **Type:** YouTube video transcript / strategy commentary
- **Author:** AI News & Strategy Daily / Nate B Jones
- **URL:** https://www.youtube.com/watch?v=0cVuMHaYEHE&t=1s
- **Published:** 2026-03-30 · **Clipped:** 2026-06-27
- **Raw:** `project-memory/raw/Anthropic, OpenAI, and Microsoft Just Agreed on One File Format. It Changes Everything..md`

## What it is

A strategic commentary source arguing that agent skills have shifted from personal prompt/config files to
organizational infrastructure. It focuses on how to design agent-readable skills that trigger reliably and
compose across agent workflows.

## Key claims

- A skill is a folder with a markdown file: metadata at the top and methodology/instructions below.
- Skills are increasingly called by agents rather than humans, so descriptions act as routing signals and
  outputs should be treated as contracts.
- Good skills are lean, have specific one-line descriptions, encode reasoning and quality criteria, specify
  output format, include edge cases/examples, and should be tested quantitatively when used by agents.
- Teams should think in three tiers: standard org skills, methodology/craft skills, and personal workflow
  skills.
- The source claims skills are becoming a broad cross-vendor infrastructure layer involving Claude,
  ChatGPT/OpenAI, Microsoft Copilot, and community repositories.
- It explicitly warns that deterministic behavior should be hardwired with scripts rather than plain-English
  skill prose.

## Assessment against the four hard constraints

- **(a) Agent-agnostic:** promising but unverified. If Agent Skills truly work across the in-scope surfaces,
  they may be a better carrier for shared memory instructions than per-agent bespoke docs. This needs direct
  surface verification.
- **(b) Simplistic:** strong as an instruction-delivery layer: markdown folder + optional scripts. Weak if a
  skill ecosystem becomes a package-management dependency.
- **(c) Local-first:** compatible if skills are local files and scripts; not guaranteed by the source.
- **(d) Company-wide installable:** promising because skills can be versioned and rolled out, but this source
  does not establish a tested one-step installer.

## Relevance to this project

This source strengthens the idea that the selected product may need two separable parts:

1. a local memory store, and
2. an agent-readable instruction/operation layer that tells each harness how to ingest, query, and lint it.

That maps directly to the charter's warning not to conflate product architecture with working method. Agent
Skills may be the delivery vehicle for the operation layer, but only after proving support in Claude Code
CLI, Codex CLI, and Cowork.

## Wikilinks

[[concept-agent-skills-standard]] · [[concept-agent-agnostic-gap]] · [[concept-agent-harness]] ·
[[candidate-karpathy-llm-wiki]]
