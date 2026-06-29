# source: How to Build a Company OS in Claude Code

- **Source ID:** SRC-20260624-company-os-claude-code
- **Type:** YouTube auto-generated transcript / company-operating-system walkthrough
- **URL:** https://www.youtube.com/watch?v=qsDX0PMKcaE
- **Raw:** `project-memory/raw/How to Build a Company OS in Claude Code - Jiaona Zhang - Product Growth.md`

## What it is

A transcript-backed interview with Jiaona Zhang of Laurel showing a GitHub-based "Company OS" for how
teams work with Claude, plus concrete examples of Slack automations, long-form playbooks turned into
skills, end-to-end feature ownership, and an AI Ops function responsible for spreading working patterns
from the AI-native 1% to the rest of the company.

## Transcript-backed takeaways

- The "Company OS" is described as a company-wide GitHub structure organized by function and workflow, so
  people can open a known place and find the right playbook or skill instead of relying on private prompt
  lore.
- The build order is explicit: map the ontology of work first, then write playbooks, then audit which
  steps require humans versus automation, and only then turn the repeatable residue into skills and agent
  flows.
- Adoption depends on surface placement. The source repeatedly argues that separate AI interfaces create
  friction, so the highest-leverage workflows should show up inside Slack or email where people already
  work.
- Laurel's "captain" model reframes end-to-end ownership: the captain is the person whose skill is most
  critical for the hardest part of the initiative, not automatically an engineer.
- AI rollout is treated as an operating function, not a side hobby. The source argues for a dedicated AI
  Ops team because "everyone owns AI" usually degenerates into no one owning it.
- The interview ends with a four-level maturity model: chat usage, then wider practical use, then
  workflow/skill infrastructure, then broad company operating leverage.

## Relevance to the memory project

Useful mostly as organization-design evidence rather than product evidence. It strengthens
[[concept-agent-skills-standard]], [[concept-agent-harness]], [[concept-context-engineering]], and
[[concept-agent-legibility]] by showing one way a file-based operating layer, skill layer, and delivery
surfaces can fit together. It is weaker on the actual selection question because this is a practitioner
interview, not a tested cross-surface repo or official spec.

## Assessment against the four hard constraints

- Agent-agnostic delivery is not proven; the walkthrough is centered on Claude plus Slack/email-facing
  workflows.
- Simplistic/local-first is directionally strong because the OS is shown as GitHub files and playbooks,
  but the actual runtime/integration stack is not fully audited.
- Company-wide installability is conceptually strong here: shared workflows are the point. But the source
  is still secondary commentary, not a reproducible installer or repo audit.

## Wikilinks

[[concept-agent-skills-standard]] · [[concept-agent-harness]] · [[concept-context-engineering]] ·
[[concept-agent-legibility]] · [[source-5-skills-to-build-an-ai-operating-system-like-the-1-full-guide]] ·
[[source-anthropic-teams-claude-code]] · [[source-openai-harness-engineering-codex]]
