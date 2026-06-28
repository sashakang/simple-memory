# concept: The agent-agnostic gap

Our hardest constraint — **(a) reach all three surfaces: Claude Code CLI, OpenAI Codex CLI, and Claude
Cowork** (desktop local-agent mode) — and the dimension on which most candidates silently fail.

## The gap, stated

Almost every memory tool in the field is built **Claude-Code-first**. [[source-every-cc-memory-system-compared]]
is the cleanest example: its entire six-level taxonomy ([[concept-six-levels-of-memory]]) is scored on Claude
Code alone and **never asks** whether a system also reaches Codex CLI or Cowork. A `CLAUDE.md`-only design
fails by construction — Codex reads `AGENTS.md`, not `CLAUDE.md`.

The 2026-06-27 sources sharpen this rather than closing it. [[source-claude-second-brain-levels]] suggests
copying or routing `CLAUDE.md` into `AGENTS.md` for Codex, and [[source-dox-agents-md-framework]] shows an
`AGENTS.md`-first tree. Both help with Claude/Codex routing, but neither proves Cowork support. [[source-agent-harness]]
explains why: each harness has different prompt assembly, hook, session, and permission surfaces.

## The two ways to close it (and their cost)

1. **Shared remote DB + MCP front door** — e.g. [[candidate-openbrain]] (L6). Reaches *every* tool, but pays
   with **local-first** (constraint c): hosted Postgres, network query per read. Our charter rejects this.
2. **Shared local file + per-agent shims/hooks** — one source of truth on disk, with a thin adapter per
   surface (Claude session-start hook, Codex `config.toml`/`hooks.json` + `AGENTS.md` fallback, Cowork plugin).
   Keeps local-first *and* cross-surface. This is [[candidate-observational-memory]]'s approach and the only
   one observed to cover all three out of the box.
3. **Agent Skills as shared operation layer** — [[concept-agent-skills-standard]] may let one local skill define
   ingest/query/lint operations and then be installed across surfaces. This is promising, but it is not yet
   evidence until the three in-scope surfaces are tested directly. [[source-anthropic-guide-building-skills]]
   supports Claude-surface portability, not Codex/Cowork proof.

[[source-google-okf]] and [[source-claude-managed-agents-memory]] add two useful but non-closing leads. OKF
is described as a format any agent can read, which may help the shared-local-file side if verified.
Anthropic managed-agent memory is file-shaped but Claude-platform-specific and hosted, so it does not close
the gap for this local product.

The Telegram transcript redo adds one stronger cross-surface lead and one useful taxonomy. [[source-introducing-visual-plan-rich-plans-for-claude-code-codex]]
explicitly targets both Claude Code and Codex with a shared skill/repo artifact, but it still needs an install
test. [[source-the-7-levels-of-using-claude-context-explained-in-24-min]] names Claude Code, Cowork, and
Codex together as context-infrastructure surfaces; that matches this project's scope, but it remains a
training-video claim until verified directly.

## Why it's load-bearing now

With Cursor out of scope, **Cowork is the only "hard" surface** — it rests on an undocumented Anthropic
local-agent-mode plugin contract that OM is claimed to uniquely support. If that contract changes, the
fallback is the per-surface shim model above (re-target the Cowork adapter), not a re-platforming. This is the
single biggest residual risk in the OM case — see [[candidate-observational-memory]].

[[concept-six-levels-of-memory]] · [[candidate-observational-memory]] · [[candidate-openbrain]] ·
[[concept-agent-harness]] · [[concept-agent-skills-standard]] · [[candidate-dox-agents-md]] ·
[[candidate-google-okf]] · [[candidate-anthropic-managed-agents-memory]] ·
[[source-introducing-visual-plan-rich-plans-for-claude-code-codex]] ·
[[source-the-7-levels-of-using-claude-context-explained-in-24-min]]
