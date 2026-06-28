# Index

Content-oriented catalog of every wiki page. Read this first when answering a query.
Each entry uses a wikilink to the page plus a one-line summary. Update on every ingest.

Status: **active, dual-purpose** — first substantive ingest 2026-06-15 (Simon Scrapes six-levels survey).
The vault holds two sections: **Comparison Project** (local-memory selection) and **Knowledge Base**
(general agent knowledge). For classification rules see `CLAUDE.md` → "Three concerns that must not be conflated".

---

# Comparison Project

## Candidates (one page per implementation under evaluation)

- [[candidate-observational-memory]] — OM: plain-MD store, BM25 recall, curated writes, 3-surface install; the **baseline-to-beat** (decision deferred).
- [[candidate-dox-agents-md]] — hierarchical `AGENTS.md` codebase docs; strong local routing component, but `AGENTS.md`-only as stated fails 3-surface reach.
- [[candidate-memsearch]] — Zilliz L3 plugin: semantic recall + top-3 auto-inject, plain markdown; **named upgrade path** if BM25 bites (but Claude-Code-only).
- [[candidate-mempalace]] — L4 verbatim recall via SQLite+Chroma + AAAK index; fails (b) simplistic & readable-store.
- [[candidate-openbrain]] — L6 Postgres-on-Supabase cross-tool brain via MCP; only truly cross-tool but fails (c) local-first.
- [[candidate-mem0]] — hosted L6 cross-tool SaaS; fails (c), data on their servers.
- [[candidate-recall]] — hosted Karpathy-wiki clone; fails (c), consumption- not operation-oriented.
- [[candidate-john-pawel-hook-system]] — L2 session-start hook + reorganize command; conceptual parent of OM.
- [[candidate-karpathy-llm-wiki]] — the pattern (raw/ + wiki/); this project's *method*, and a candidate the source deems research- not operational-memory.
- [[candidate-google-okf]] — transcript-backed lead for a Google plain-Markdown knowledge format; promising schema candidate, still needs official-spec verification.
- [[candidate-anthropic-managed-agents-memory]] — hosted Claude-platform memory with a filesystem interface; validates files-not-vectors, but fails local-first as stated.

## Concepts (cross-cutting ideas, patterns, definitions)

- [[concept-six-levels-of-memory]] — Simon Scrapes taxonomy; our 4 constraints carve the ladder at level 3.
- [[concept-storage-injection-recall-matrix]] — the 4-axis scoring frame (save trigger/form, injection, recall).
- [[concept-bm25-vs-semantic-recall]] — doubt #1: keyword vs semantic; gain modest (~+5pp), memsearch is the escape valve.
- [[concept-agent-agnostic-gap]] — constraint (a); shared-local-file+shims (OM) vs shared-remote-DB (OpenBrain).
- [[concept-context-rot]] — the root problem all memory systems solve; favors small capped injection.
- [[concept-agent-harness]] — separates memory store from harness-specific prompt assembly, hooks, skills, and permissions.
- [[concept-agent-skills-standard]] — Agent Skills as a possible cross-agent delivery layer; promising, but must be surface-tested.
- [[concept-context-engineering]] — context as a finite high-signal token budget; favors routing and just-in-time retrieval.
- [[concept-agent-legibility]] — repository/local knowledge must be inspectable and mechanically checkable by agents.
- [[concept-loop-engineering]] — trigger + verifiable goal loops; useful for bounded memory lint/gardening, risky when amorphous.

## Sources (one summary page per raw source in `raw/`)

- [[source-every-cc-memory-system-compared]] — Simon Scrapes YouTube survey; six levels of CC memory; frames (doesn't dislodge) the OM decision.
- [[source-best-claude-memory-system]] — Simon Scrapes hybrid stack: automatic summarized storage, Hermes-style capped injection, hybrid semantic recall + cited answers.
- [[source-claude-second-brain-levels]] — Nate Herk five-level second-brain taxonomy; choose the lowest level that solves the pain.
- [[source-memorygraphrag]] — research explainer for ontology/fact/passage graph memory; useful evidence-grounding ideas, too complex for our bar.
- [[source-dox-agents-md-framework]] — DOX hierarchical `AGENTS.md` docs; local routing/map layer, not a full persistent memory system.
- [[source-agent-skills-standard]] — Agent Skills as organizational infrastructure; descriptions as routing signals, outputs as contracts.
- [[source-agent-harness]] — harness architecture; memory reaches agents through prompt assembly, hooks, skills, session state, and permissions.
- [[source-anthropic-guide-building-skills]] — official Anthropic guide to skill structure, progressive disclosure, and testing.
- [[source-effective-context-engineering]] — official Anthropic context-engineering article; just-in-time retrieval, compaction, notes, subagents.
- [[source-openai-harness-engineering-codex]] — official OpenAI Codex article; short `AGENTS.md` map plus structured repo docs as system of record.
- [[source-harness-engineering-ai-business]] — practitioner discussion of harnesses, skills/toolkits, MCP limits, and malicious skill risk.
- [[source-loop-engineering]] — loop engineering: triggers, verifiable goals, schedules/events, and cost risk.
- [[source-telegram-saved-ai-youtube-videos]] — Telegram Saved Messages YouTube triage; all 30 AI videos now have standalone raw transcripts and source summaries.
- [[source-claude-managed-agents-memory]] — Prism Labs commentary on Anthropic managed-agent filesystem memory.
- [[source-google-okf]] — Cloud Codes commentary on Google's OKF Markdown/Git knowledge format.
- [[source-self-evolving-claude-code-memory]] — Cole Medin walkthrough of Claude Code hooks plus Karpathy-style memory promotion.
- [[source-karpathy-obsidian-no-rag-wiki]] — Josh Pocock walkthrough of Karpathy-style Obsidian wiki, ingest/query/lint, and no-RAG tradeoffs.
- [[source-anthropic-teams-claude-code]] — Simon Scrapes commentary on Anthropic team Claude Code practices, skills, and context files.
- [[source-5-skills-to-build-an-ai-operating-system-like-the-1-full-guide]] — five-skill AI OS setup/operator/optimizer/team/MCP workflow; useful as skills-as-operation-layer evidence.
- [[source-anthropic-quietly-shipped-the-memory-layer-your-agent-was-missing-buil]] — Anthropic/OpenClaw dreaming and background memory consolidation; useful but risky if hosted or opaque.
- [[source-claude-code-works-better-with-loops-not-prompts]] — orchestrator/executioner/reviewer loops with trigger, worktree, skills, memory, subagents, and human gates.
- [[source-claude-just-made-notebooklm-10x-more-powerful-new-skill]] — NotebookLM automation skill; useful source-ingest ergonomics, not a local-memory candidate.
- [[source-claude-bloomberg-factset]] — Russian transcript on finance agents/plugins; provenance-heavy analyst workflows, not architecture evidence.
- [[source-creating-your-own-agentic-os-is-easy-insanely-powerful]] — agentic OS walkthrough: static context, memory, repeatable processes, and project/client structure.
- [[source-finally-agent-loops-clearly-explained]] — loop primer emphasizing reason/act/observe/repeat, verification, and concrete done criteria.
- [[source-hermes-agent-under-claude-code-is-insane]] — Hermes + Claude Code harness bridge: self-evolving skills, memory trimming, MCP mode, Slack-to-PRD workflows.
- [[source-hermes-agent-zero-to-personal-ai-assistant-1-hour-course]] — Hermes setup course: VPS, Telegram, first skill, cron, GitHub backup, and multi-agent scaling.
- [[source-hermes-workspace-the-openclaw-killer-that-runs-10-ai-agents-at-once]] — Hermes Workspace multi-agent orchestration; useful contrast but likely heavy for the simplicity bar.
- [[source-how-i-d-start-a-1-person-business-with-claude-ai-sign-my-first-client]] — peripheral Claude business workflow; useful for packaging repeatable services, not memory architecture.
- [[source-how-this-ex-meta-l8-engineer-ships-40-prs-a-day-with-ai-agents-kun-che]] — Kun Chen interview: plan/code/validate, rich planning artifacts, parallel agents, and independent code review.
- [[source-i-built-a-deck-with-ai-then-made-a-second-ai-attack-it]] — AI office-file workflow: source layer, structure, creation, hostile review, and truth-layer discipline.
- [[source-i-stopped-building-ai-agents-and-did-this-instead]] — simple Atlas/Projects/End Products folder system; file structure as cognitive architecture.
- [[source-i-turned-claude-opus-4-8-into-my-entire-ai-operating-system]] — personal AI OS using context, connections, capabilities, and cadence.
- [[source-introducing-visual-plan-rich-plans-for-claude-code-codex]] — Builder.io `/visual-plan` skill for Claude Code + Codex; rich MDX plans and visual recaps as legibility artifacts.
- [[source-l8-principal-s-agentic-engineering-workflow]] — Kun Chen workflow: global/project memory files, skills, validation, worktrees, and agent ergonomics.
- [[source-master-all-7-levels-of-claude-code-memory]] — memory design method: repo audits, lightweight specs, decay/promotion, retrieval, compaction, and injection modes.
- [[source-shopify-ceo-reveals-their-secret-ai-developer]] — Shopify River commentary; public agent work as organizational learning and legibility.
- [[source-stop-prompting-claude-start-loop-engineering]] — loop building blocks: context, skills, goal/verification, output, and memory.
- [[source-the-7-levels-of-using-claude-context-explained-in-24-min]] — context-infrastructure taxonomy spanning Claude Code, Cowork, Codex, second brain, and team OS.
- [[source-the-creators-of-claude-code-and-openclaw-don-t-prompt-their-agents-any]] — loop-engineering caution: orchestrator/worker control plane, observability, run history, cost, and compounding hallucination risk.
- [[source-the-karpathy-claude-md-file-that-43-000-developers-installed-in-1-week]] — viral one-file `CLAUDE.md` behavior layer; attractive install surface but Claude-only unless shimmed.
- [[source-the-one-ai-writing-hack-nobody-talks-about]] — project-room workflow: source inventory, missing-context lists, duplicate checks, and files as reasoning canvas.
- [[source-the-new-hermes-agent-update-has-me-speechless]] — Hermes update: desktop app, background agents, profile builder, Skills Hub, and self-improvement risks.
- [[source-smm-ai-hermes]] — Telegram-saved YouTube transcript: Как собрать SMM AI-агента в Hermes для контента и соцсетей.
- [[source-register]] — stable source IDs and raw-file tracking for ingests.
- [[research-questions]] — open verification questions created during ingest.

## Decisions (rationale for choices made during the comparison)

- _none recorded yet_ — OM recommendation exists but is **deferred** per standing instruction ("document the decision when it is made").

---

# Knowledge Base (agent knowledge)

Durable, general agent knowledge — techniques, frameworks, achievements, best practices — across sessions.
Not scoped to the comparison. Pages are `kb-<topic>.md`. Add via the **KB ingest** op in `CLAUDE.md`.

- _none yet_ — populated by agents as real agent-knowledge is recorded.
