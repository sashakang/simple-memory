# Research Questions

Open questions discovered during ingest. Keep these separate from decisions; close them only with
source evidence or direct tests.

## Candidate verification

- Verify `agent0ai/dox` against the code, not only the transcript: license, exact install path,
  whether it has an `AGENTS.md`-only assumption, and whether it can be mirrored into `CLAUDE.md` /
  Cowork plugin instructions without drift. Source: [[source-dox-agents-md-framework]].
- Verify whether Agent Skills are a real cross-vendor install target for the three in-scope surfaces:
  Claude Code CLI, OpenAI Codex CLI, and Claude Cowork. The source claims broad vendor convergence, but
  this project needs surface-by-surface install proof. Sources: [[source-agent-skills-standard]],
  [[source-anthropic-guide-building-skills]].
- Verify Simon Scrapes' "best memory system" implementation or academy package if it becomes a candidate:
  one-line install, local files vs vector index location, Codex/harness support, and team-mode Supabase
  requirements. Source: [[source-best-claude-memory-system]].
- Verify Google's OKF against official materials: spec/repo, license, exact schema, sample bundles,
  whether Google Cloud is optional, and whether a local OKF bundle can be consumed by Claude Code CLI,
  OpenAI Codex CLI, and Claude Cowork. Source: [[source-google-okf]].
- Verify Anthropic managed-agent memory against official docs and engineering posts: `/mnt/memory` mount,
  limits, versioning/redaction/export, access controls, beta status, and whether exports can seed a local
  memory store. Source: [[source-claude-managed-agents-memory]].
- Verify the self-evolving Claude Code memory implementation/template described in the transcript: exact
  hooks, Claude Agent SDK dependency, local file layout, install path, and portability beyond Claude Code.
  Source: [[source-self-evolving-claude-code-memory]].

## Architecture questions

- Does a hierarchical `AGENTS.md` documentation tree solve enough of the "agent knows where to look"
  problem to reduce the required memory system scope, or is it only codebase documentation? Source:
  [[source-dox-agents-md-framework]].
- Should the selected architecture include an explicit "routing file" layer (`AGENTS.md`/`CLAUDE.md`
  shims) separate from the memory store, so each harness can find the same local source of truth? Sources:
  [[source-agent-harness]], [[source-claude-second-brain-levels]], [[source-agent-skills-standard]].
- What direct recall failures would justify adding semantic/hybrid retrieval over BM25? Sources:
  [[source-best-claude-memory-system]], [[source-claude-second-brain-levels]], [[source-memorygraphrag]].
- Should the selected installer include mechanical checks for wiki health, source-register coverage, stale
  pages, and broken links, following OpenAI's repo-local knowledge pattern? Source:
  [[source-openai-harness-engineering-codex]].
- What trust/review model is needed before installing community skills company-wide, given the malicious
  skill risk? Source: [[source-harness-engineering-ai-business]].
- Verify the strongest Telegram-saved implementation leads against primary repos/docs before using them for
  product selection: Builder.io `/visual-plan`, Kun Chen's Lavish/Treehouse/No Mistakes/Firstmate tools,
  Hermes Agent/Workspace, OpenClaw memory/dreaming, and the Ben van Sprundel OS skills/templates. The
  transcript redo produced source-backed summaries, but most product claims are still secondary commentary.
  Sources: [[source-introducing-visual-plan-rich-plans-for-claude-code-codex]],
  [[source-l8-principal-s-agentic-engineering-workflow]],
  [[source-hermes-agent-under-claude-code-is-insane]],
  [[source-anthropic-quietly-shipped-the-memory-layer-your-agent-was-missing-buil]],
  [[source-5-skills-to-build-an-ai-operating-system-like-the-1-full-guide]].
