# source: Как собрать SMM AI-агента в Hermes для контента и соцсетей

- **Source ID:** SRC-20260621-smm-ai-hermes
- **Type:** YouTube auto-generated transcript
- **URL:** https://www.youtube.com/watch?v=xep4LzDheAM
- **Raw:** `project-memory/raw/Как собрать SMM AI-агента в Hermes для контента и соцсетей.md`

## What it is

A Russian-language Hermes walkthrough showing the construction of an SMM/content agent from a real task,
not from a generic "install more agents" impulse. The raw file was saved in the Obsidian-style shape:
frontmatter, YouTube embed, description text, chapter list, and full timestamped transcript.

This source is important because it was initially skipped from Telegram previews as "insufficient to
classify"; the full transcript proves that preview-only classification can miss substantial agent
architecture material.

## Key claims and ideas

- Build agents from concrete tasks, not from curiosity about what an agent might do. The speaker says a
  useful agent starts with a real need, role, boundaries, tools, memory, sources, checks, and expected output.
- A skill can grow into an agent when the work needs its own role, memory, scaling path, or sub-skills. In
  this example, SMM text production is split out from the marketing agent because keeping audience strategy,
  tone of voice, anti-AI-text checks, platform formats, and writing rules in one agent bloats context.
- Too many installed skills are harmful. The transcript argues that agents should see only relevant skill
  names/descriptions or allowed skill sets, because broad skill catalogs add context load and can create
  conflicting instructions.
- The speaker describes a Hermes-style team architecture with a wiki/source-of-truth layer, per-agent
  memory/context, agent-to-agent handoff for quick questions, and Kanban for heavier multi-agent tasks. One
  agent should own Kanban writes to avoid messy duplicated task context.
- To reduce hallucination, agents need stop rules, escalation-to-user rules, explicit sources of truth, and
  evidence reports: what was read, what changed, what was checked, where the agent is uncertain, and what
  decision is needed from the user.
- The source reinforces a context-engineering pattern: divide work into semantic pieces, give each agent the
  context it owns, and let agents request missing specialized context from the right teammate instead of
  loading everything into one context window.

## Why it affects this project

This is stronger evidence for [[concept-agent-harness]] and [[concept-context-engineering]] than the Telegram
preview suggested. It also adds a process lesson for this wiki: classify YouTube sources from full raw
captures/transcripts, not link previews.

## Assessment against the four hard constraints

- **(a) Agent-agnostic:** not established by this source alone.
- **(b) Simplistic:** supports bounded, role-specific context and smaller allowed skill sets; Hermes itself
  may still be heavier than this project's preferred local-markdown baseline.
- **(c) Local-first:** mixed. The speaker describes local Mac usage and a wiki/source-of-truth layer, but this
  is not a repo/spec proof of local-first storage.
- **(d) Company-wide installable:** not established; this is a walkthrough, not a tested installer.

## Wikilinks

[[concept-agent-harness]] · [[concept-context-engineering]] · [[concept-agent-skills-standard]] ·
[[concept-agent-legibility]] · [[source-telegram-saved-ai-youtube-videos]]
