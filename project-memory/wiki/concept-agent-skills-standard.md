# concept: Agent Skills as a delivery layer

Agent Skills are a candidate carrier for memory operations: a local folder with markdown instructions,
metadata, examples, and optional scripts that an agent can discover and invoke.

## Official structure

[[source-anthropic-guide-building-skills]] gives the strongest source-backed structure: a skill folder has a
required `SKILL.md` plus optional `scripts/`, `references/`, and `assets/`. It uses progressive disclosure:
frontmatter routes the skill, the body loads when relevant, and additional files are pulled only as needed.

## What the new source contributes

[[source-agent-skills-standard]] frames skills as organizational infrastructure rather than personal prompt
snippets. The useful ideas for this project:

- the description is a routing signal, not a label;
- outputs should be contracts that downstream agents can rely on;
- methodology should encode reasoning and quality criteria, not only linear steps;
- skills should stay lean, with examples/scripts split out when needed;
- deterministic behavior belongs in scripts, not prose;
- team rollout should distinguish org-standard skills, methodology skills, and personal workflow skills.
- [[source-harness-engineering-ai-business]] adds a security warning: community skills can contain hidden
  malicious instructions, so company-wide rollout needs review/trust controls.

## Why this is not yet a decision

The sources claim useful Claude-surface portability and broad industry momentum, but the project bar is
narrower and stricter: Claude Code CLI, OpenAI Codex CLI, and Claude Cowork. Agent Skills become a viable
company-wide delivery layer only if direct tests prove all three can install and invoke the same skill or a
generated shim from one source of truth.

[[source-anthropic-teams-claude-code]] adds secondary transcript evidence: skills work best as short,
repeatable instruction folders with specific names/descriptions and heavier examples kept in reference
files. This aligns with [[source-anthropic-guide-building-skills]], but does not add new cross-surface
proof.

[[source-company-os-claude-code]] adds the company-rollout angle: skills are not just reusable prompts but
the operational residue of audited playbooks. The useful pattern is "ontology -> playbook -> human/agent
audit -> skills", with the goal of moving the AI-native 1%'s working methods into a shared delivery layer
the rest of the company can actually use.

[[source-self-improving-system-claude-code]] adds the ingest-operations angle: each recurring data pipeline
should begin with a tested skill, not an ad hoc prompt. That matches the repo's bias toward explicit,
repeatable operations rather than invisible agent behavior.

The Telegram transcript redo adds three practical cautions. [[source-l8-principal-s-agentic-engineering-workflow]]
and [[source-smm-ai-hermes]] both warn that skills can hurt the agent when too many are loaded or when their
scope is unclear. [[source-5-skills-to-build-an-ai-operating-system-like-the-1-full-guide]] is useful as an
operation-layer example: skills can set up, operate, optimize, share, and connect a context system. [[source-introducing-visual-plan-rich-plans-for-claude-code-codex]]
is the strongest cross-surface lead because it explicitly targets Claude Code and Codex, but it still needs a
repo/install test before it can count as proof.

## Cross-links

[[source-agent-skills-standard]] · [[source-anthropic-guide-building-skills]] ·
[[source-harness-engineering-ai-business]] · [[source-anthropic-teams-claude-code]] ·
[[source-company-os-claude-code]] ·
[[source-self-improving-system-claude-code]] ·
[[source-l8-principal-s-agentic-engineering-workflow]] · [[source-smm-ai-hermes]] ·
[[source-introducing-visual-plan-rich-plans-for-claude-code-codex]] ·
[[concept-agent-harness]] · [[concept-agent-agnostic-gap]] ·
[[candidate-karpathy-llm-wiki]]
