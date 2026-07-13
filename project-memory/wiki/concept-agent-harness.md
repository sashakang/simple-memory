# concept: Agent harness

An agent harness is the runtime around a model that lets it act, observe results, and keep iterating. The
term matters here because "memory" reaches an agent only through harness-specific surfaces: prompt assembly,
hooks, skills, tools, session persistence, and permissions.

## Why it matters to local memory

[[source-agent-harness]] names dynamic prompt assembly from `CLAUDE.md`/`AGENTS.md`, lifecycle hooks, and
session persistence as core harness components. Those are exactly where a local-memory architecture plugs
in. A markdown store alone is not enough; each target harness must know when to load, write, search, and
respect that store.

[[source-openai-harness-engineering-codex]] shows the Codex-specific version at scale: a short `AGENTS.md`
map, structured repo docs as the system of record, mechanical checks, and recurring cleanup. [[source-harness-engineering-ai-business]]
adds the skill/toolkit angle: a harness should reveal only the relevant tools/instructions instead of
showing the agent a huge flat tool list.

[[source-smm-ai-hermes]] adds a practitioner example of a multi-agent harness: one main agent creates a
specialized SMM agent from a concrete task brief; agents have roles, memories, allowed skills, and
specialized context; quick cross-agent questions use handoff, while heavier work uses Kanban. The source is
not product-selection proof, but it is useful harness vocabulary.

The broader Telegram transcript redo reinforces that a memory store is only one harness component.
[[source-l8-principal-s-agentic-engineering-workflow]] names terminal/editor ergonomics, global/project
memory files, skills, validation, long-running tasks, and worktrees as one system. [[source-hermes-agent-under-claude-code-is-insane]],
[[source-hermes-agent-zero-to-personal-ai-assistant-1-hour-course]], [[source-hermes-workspace-the-openclaw-killer-that-runs-10-ai-agents-at-once]],
and [[source-the-new-hermes-agent-update-has-me-speechless]] show the heavier Hermes direction: always-on
agents, profiles, background agents, Skills Hub, cron jobs, Telegram, VPS, and MCP bridges. That is useful
architecture vocabulary, but it is probably too heavy to be the default memory product under the simplicity
constraint.

[[source-company-os-claude-code]] adds a practical company harness pattern: GitHub as the durable operating
system, playbooks as the audited workflow layer, skills/agents as the executable layer, and Slack/email as
the user-facing surface. That is useful because it separates storage from delivery while keeping the human
entrypoint inside the tools people already use.

[[source-news-vacuum-agent-idea]] adds a smaller-scale but useful harness lesson: start from the incoming
signal sources and required outputs first, then derive documentation, specs, and only then the technical
architecture. That is a cleaner harness-design sequence than starting from the agent runtime and searching
for a purpose afterward.

## Implication for this project

The product under evaluation should be described as:

- a **local memory store** (the durable filesystem state),
- an **operation layer** (ingest/query/lint/write rules), and
- **per-harness shims** (Claude Code, Codex CLI, Cowork) or a verified shared standard.

This keeps the charter's two layers separate. The working wiki method is not the shipped architecture; it is
one operation pattern being dogfooded while candidates are evaluated.

## Cross-links

[[source-agent-harness]] · [[source-openai-harness-engineering-codex]] ·
[[source-company-os-claude-code]] ·
[[source-news-vacuum-agent-idea]] ·
[[source-smm-ai-hermes]] ·
[[source-l8-principal-s-agentic-engineering-workflow]] · [[source-hermes-agent-under-claude-code-is-insane]] ·
[[source-hermes-agent-zero-to-personal-ai-assistant-1-hour-course]] ·
[[source-hermes-workspace-the-openclaw-killer-that-runs-10-ai-agents-at-once]] ·
[[concept-agent-agnostic-gap]] · [[concept-agent-skills-standard]] · [[concept-context-engineering]] ·
[[candidate-observational-memory]] · [[candidate-dox-agents-md]]
