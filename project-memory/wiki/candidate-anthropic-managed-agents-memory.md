# candidate: Anthropic Managed Agents Memory

- **Source status:** transcript-backed lead, not yet official-doc verified.
- **Sources:** [[source-claude-managed-agents-memory]]

## What it is

The transcript describes Anthropic managed-agent memory as a hosted Claude-platform memory layer where a
memory store is mounted into an agent session as a regular filesystem at `/mnt/memory`. The agent reads and
writes directories and text files with shell tools; the transcript explicitly contrasts this with vector
databases, opaque consumer memory blobs, and special model memory APIs.

The design is important evidence for the broader architectural direction: even a managed enterprise memory
product is being described as **files first**, with auditability and versioning as primary benefits.

## Fit against constraints

- **(a) Agent-agnostic:** weak. The source is Claude-platform-specific and distinguishes managed agents from
  Claude Code / Claude Cowork.
- **(b) Simplistic:** strong at the agent interface because it is file-shaped; weaker operationally because
  the storage is a managed platform API.
- **(c) Local-first:** fails as a shipped company-wide local-memory product because the transcript says the
  memory files live in Anthropic managed infrastructure, even if export is possible.
- **(d) Company-wide installable:** unknown for our scope; likely not the same class of install as a local
  repo or skill.

## Relevance to the decision

This is not currently a replacement for the selected local product. It is more useful as validation that
plain text files, versioning, auditability, and shared read-only reference stores are the right primitives.
It also adds a security requirement: shared memory should default to read-only when processing untrusted
input, because prompt injection can poison writable memory.

## Open verification

- Read official Anthropic docs and engineering posts for managed-agent memory.
- Verify the claimed `/mnt/memory` mount, limits, versioning, redaction, export, and access controls.
- Decide whether any local product should mirror the read-only shared store / read-write trusted store split.

## Wikilinks

[[source-claude-managed-agents-memory]] · [[concept-context-engineering]] ·
[[concept-agent-legibility]] · [[concept-agent-agnostic-gap]]
