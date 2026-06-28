# candidate: Google Open Knowledge Format (OKF)

- **Source status:** transcript-backed lead, not yet official-spec verified.
- **Sources:** [[source-google-okf]]

## What it is

The transcript presents OKF as an open, minimally opinionated knowledge format for agents: a folder of
plain Markdown files in Git, each describing one concept, metric, table, runbook, or playbook. It claims the
only required metadata field is `type`, with optional title, description, resource links, tags, and
timestamps. Documents link to each other with ordinary Markdown links; bundles are directory trees with
indexes and optional changelogs.

This is close to this project's preferred shape: local files, Git history, progressive disclosure, and
agent-readable institutional knowledge.

## Fit against constraints

- **(a) Agent-agnostic:** promising in concept because the transcript says it is a format rather than a
  platform, but unproven for Claude Code CLI, OpenAI Codex CLI, and Claude Cowork.
- **(b) Simplistic:** strong if the transcript is accurate: Markdown, YAML, indexes, links, no vector DB.
- **(c) Local-first:** strong if it works as a plain Git folder without Google Cloud runtime dependency.
- **(d) Company-wide installable:** unknown. We need the actual spec/repo and a tested setup path.

## Relevance to the decision

OKF may be less a complete memory product than a **schema candidate** for company knowledge pages. It could
inform the selected product's page contract: one concept per file, minimal frontmatter, indexes for routing,
and Git-managed review.

## Open verification

- Find and read the official OKF spec/repo.
- Confirm license, required fields, sample bundles, and compatibility outside Google Cloud.
- Test whether a Codex/Claude/Cowork shim can consume an OKF bundle as local context.

## Wikilinks

[[source-google-okf]] · [[concept-agent-legibility]] ·
[[concept-context-engineering]] · [[concept-agent-agnostic-gap]]
