# source: Harness Engineering for AI Agents

- **Source ID:** SRC-20260312-harness-engineering-ai-business
- **Type:** YouTube transcript / podcast discussion
- **Author:** Cyril Imhof
- **URL:** https://www.youtube.com/watch?v=uAhWHu3WdUw&t=1477s
- **Published:** 2026-03-12 · **Clipped:** 2026-06-27
- **Raw:** `project-memory/raw/Harness Engineering for AI Agents (Why Every AI Business Will Need It).md`

## What it is

A practitioner discussion of context engineering, skills/toolkits, MCP, harness engineering, and business
pricing for agent products.

## Key claims

- As agents gain more tools and markdown context, they need a structured harness so they can orchestrate the
  right capability at the right time.
- Skills/toolkits group tools plus instructions so the agent does not need to inspect a huge flat tool list.
- One speaker suggests not showing more than roughly 30 tools at once; skills reveal smaller toolsets on
  demand.
- MCP provides tool access, but the source argues MCP alone is insufficient: agents also need workflow
  instructions, preferences, governance, and domain context.
- Publicly shared skills can be malicious; skills may hide instructions that exfiltrate data or misuse tools.
- A good harness should be model-agnostic enough to swap models without rebuilding the whole workflow.

## Assessment against the four hard constraints

- **(a) Agent-agnostic:** conceptually supportive through model/harness modularity, but not product evidence.
- **(b) Simplistic:** supports skill/tool grouping and markdown context, but it is about broader agent products.
- **(c) Local-first:** not addressed directly.
- **(d) Company-wide installable:** not addressed.

## Relevance to this project

This source reinforces [[concept-agent-harness]] and adds a security caution to [[concept-agent-skills-standard]]:
skills are a powerful delivery layer, but a company-wide install path needs trust, review, and possibly
deterministic scripts for high-risk behavior.

## Wikilinks

[[concept-agent-harness]] · [[concept-agent-skills-standard]] · [[concept-context-engineering]] ·
[[concept-agent-agnostic-gap]]
