# source: Hermes Agent under Claude Code Is Insane

- **Source ID:** SRC-20260606-hermes-agent-under-claude-code-is-insane
- **Type:** YouTube auto-generated transcript
- **URL:** https://www.youtube.com/watch?v=Sb96po6S67k
- **Raw:** `project-memory/raw/Hermes Agent under Claude Code Is Insane.md`

## What it is

A transcript-backed Hermes Agent setup/use-case video centered on connecting Hermes to Claude Code. The description highlights a self-evolving skill system, memory trimming, sandboxing, Skill Hub, MCP server mode, Slack-to-PRD workflows, and deployed-app health checks.

## Transcript-backed takeaways

- Hermes is presented as an always-running personal agent with persistent memory and a skill system that can save reusable workflows from chats.
- The transcript/description claims Hermes trims memory files to keep model attention focused, which is directly relevant to context rot.
- Running Hermes as an MCP server for Claude Code is a harness bridge: Claude Code can reach Hermes capabilities through a tool surface.
- The Slack workflow is a living-knowledge example: channel discussion becomes a PRD skill, not just an ephemeral chat.
- The security and maintenance claims around sandboxing and Skill Hub are important but must be verified against Hermes docs/code.

## Relevance to the memory project

Hermes is candidate-adjacent for [[concept-agent-harness]] and [[concept-agent-skills-standard]], but it is not yet a verified local-memory architecture for the three required surfaces.

## Assessment against the four hard constraints

- Claude Code plus MCP is promising but not proof for Codex CLI or Claude Cowork.
- Always-running/VPS patterns may violate the project's simplistic bias.
- Skill/memory self-evolution needs audit controls before company rollout.

## Wikilinks

[[concept-agent-harness]] · [[concept-context-engineering]] · [[concept-agent-skills-standard]] · [[concept-agent-legibility]]
