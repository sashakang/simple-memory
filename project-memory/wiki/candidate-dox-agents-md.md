# candidate: DOX / hierarchical AGENTS.md docs

- **Source:** [[source-dox-agents-md-framework]]
- **Repo claimed by source:** agent0ai/dox
- **Status:** adjacent candidate/component, not a full memory-store candidate until repo-verified.

## What it is

DOX is a hierarchical local documentation pattern for codebases. A root `AGENTS.md` teaches the agent to
read and maintain folder-level `AGENTS.md` files. Each file maps a domain of the codebase: purpose,
ownership, rules/contracts, work guidance, verification, and child docs.

## Against our four constraints

- **(a) Agent-agnostic:** as presented, it is `AGENTS.md`-centric and therefore **fails** the three-surface
  bar unless mirrored/generated into `CLAUDE.md` and Cowork-compatible instructions.
- **(b) Simplistic:** excellent. It is local markdown coupled to the repository tree.
- **(c) Local-first:** excellent. Markdown files are git-trackable and require no service.
- **(d) Company-wide installable:** plausible but not proven. The source shows a paste/init flow with Codex,
  not a tested one-step company rollout.

## Where it fits

DOX solves codebase orientation and context routing, not personal/project memory recall. It may reduce
memory pressure by making repository conventions discoverable, but it does not answer "what did we decide
about a client or project six months ago?" unless those decisions are deliberately represented in the doc
tree.

The likely role is a **component** in the shim/routing layer, especially if the selected memory architecture
needs agents to navigate a shared local store without dumping it into context.

[[source-openai-harness-engineering-codex]] is an important comparison point: OpenAI reports that one giant
`AGENTS.md` failed and that a short `AGENTS.md` table of contents plus structured docs and mechanical checks
worked better. That suggests DOX's local-doc-tree idea is directionally right, but the selected architecture
should avoid letting nested instruction files become an unchecked second memory system.

## Cross-links

[[source-dox-agents-md-framework]] · [[source-openai-harness-engineering-codex]] ·
[[concept-agent-harness]] · [[concept-agent-agnostic-gap]] · [[concept-context-rot]] ·
[[concept-agent-legibility]]
