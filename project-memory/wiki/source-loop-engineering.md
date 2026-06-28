# source: Only the best are using them

- **Source ID:** SRC-20260609-loop-engineering
- **Type:** YouTube transcript
- **Author:** Matthew Berman
- **URL:** https://www.youtube.com/watch?v=dMrm2jAyrKM&t=79s
- **Published:** 2026-06-09 · **Clipped:** 2026-06-27
- **Raw:** `project-memory/raw/Only the best are using them....md`

## What it is

A practitioner video about "loop engineering": designing recurring or self-continuing agent loops instead of
manually prompting coding agents step by step.

## Key claims

- A loop needs a trigger and a goal.
- The goal must be verifiable, either deterministically through tests/CI or non-deterministically through an
  LLM judge.
- Triggers can be events, schedules, or human kickoff.
- A loop differs from a simple automation because it decides whether the goal has been reached and continues
  until completion.
- Loops become risky when goals are amorphous, specs are incomplete, or token budgets are large.
- The source claims Claude Code has `/loop`, Cursor has automations, and agent-publishing skills can be used
  inside loops; these tool-specific claims are not verified here.

## Assessment against the four hard constraints

- **(a) Agent-agnostic:** loop concepts are harness-agnostic, but named examples are tool-specific.
- **(b) Simplistic:** not a memory architecture. It adds automation complexity.
- **(c) Local-first:** not addressed.
- **(d) Company-wide installable:** not addressed.

## Relevance to this project

Loop engineering is not a candidate memory architecture, but it matters for maintenance. A selected
company-wide memory product will need linting, gardening, and stale-claim cleanup. Those can be implemented
as loops only when the goal is verifiable and bounded; otherwise, they risk expensive unattended churn.

## Wikilinks

[[concept-loop-engineering]] · [[concept-agent-harness]] · [[concept-agent-legibility]]
