# candidate: intertwine/observational-memory (OM)

- **Repo:** intertwine/observational-memory · **License:** MIT
- **Level:** ~2.5 on [[concept-six-levels-of-memory]] (hook-injected + curated, BM25 recall — by design *not* L3 semantic)
- **Status:** the **baseline-to-beat** for this project. A recommendation leans toward "keep OM as-is," but the
  decision is **deferred and unrecorded** per standing instruction ("we'll document the decision when it is made").

## What it is

A plain-markdown memory store (`observations`, `reflections`, `profile`, `active` files at
`~/.local/share/observational-memory/`). Writes are **agent-decided and curated** (an observer LLM returns the
*complete, curated* observations doc — not a raw transcript append). Reads inject a **budgeted** payload
(`DEFAULT_STARTUP_BUDGET_CHARS = 24000`, with `_hard_trim` + `atomic_write_text`), under Codex's 32 KiB
`AGENTS.md` cap by design. Recall is **BM25 keyword** — no embeddings, no vector index, no cloud. **Daemon-free**
on one machine (an optional `om-relay` multi-machine sync daemon exists but stays OFF).

## The load-bearing claims (source-verified by clone in prior research)

- **(a) All three surfaces out of the box:**
  - Claude Code — static `hooks/claude/session-start.sh` (→ `om context`) + `session-end.sh` + pre-compact checkpoint.
  - Codex CLI — `om install --codex` *programmatically* writes `~/.codex/config.toml` + `hooks.json` (SessionStart → `om context`, Stop → checkpoint), with `AGENTS.md` read fallback. (README mentions a static `hooks/codex/` dir that **does not exist** — install is programmatic. Lone README-vs-source discrepancy found.)
  - Cowork — `om install --cowork` drops a plugin into `~/Library/Application Support/Claude/local-agent-mode-plugins/`; `hooks.json` runs SessionStart → `om context`, fail-closed. Claimed the **only tool of 82 surveyed** with Cowork support.
- **(b) Curation lives in `om observe`** — the write path never raw-appends; the single invariant for any future
  adapter is "call `om observe`, never write store files directly." Plus `om reflect --check-conflicts`,
  provenance + scope rules, snapshot-before-write, v0.8.0 staleness tracking → answers **doubt #2 (curation)**.
- **(c) Local-first** — filesystem markdown, git-trackable, no network to read/write.

## How it scores on our two doubts

- **Doubt #1 — retrieval (BM25):** OM deliberately stops at keyword recall to stay simple. Measured semantic
  gain is modest (~+5pp Recall@5), so the climb to L3 isn't clearly worth the complexity. **Named upgrade path
  if BM25 ever bites: [[candidate-memsearch]]** (L3, still plain markdown). New sources keep the doubt alive:
  [[source-best-claude-memory-system]] argues for hybrid search and cited answers, while
  [[source-claude-second-brain-levels]] warns that vector chunks can miss full-document tasks. See
  [[concept-bm25-vs-semantic-recall]].
- **Doubt #2 — curation:** OM is *ahead* of the simpler wiki alternatives — it ships conflict-check, provenance,
  and staleness tracking that the Karpathy-wiki repos lack. The field (L2 "reorganize", L3 "dreaming") has
  converged on primitives OM already has.

## Residual gaps (acknowledged, none yet judged fatal)

1. Req-5 (improves performance) is **mechanistically supported, not benchmarked** for OM specifically (+4% is the
   literature's number for *curated* memory generally — ETH Zurich 2026, 438 tasks).
2. **Cowork rests on an undocumented Anthropic surface** — works today, macOS-only, no fallback if the contract
   changes. Load-bearing now that Cursor is out of scope (Cowork is the only hard surface). See [[concept-agent-agnostic-gap]].
3. **Bus factor** — ~14★, single maintainer. Mitigation: fork to a company org + pin.
4. **Cross-agent concurrent writes** — narrow lost-update window in default non-cluster mode; cluster mode (append-only) closes it.
5. **BM25 vocabulary drift** — partly mitigated by reflection canonicalization.

## Net

Nothing in [[source-every-cc-memory-system-compared]] dislodges OM; it sharpens the BM25 doubt and names the
escalation. The 2026-06-27 ingest adds more support for the same shape: use the lowest sufficient local layer,
keep injection capped, preserve source grounding, and integrate through harness-specific shims. OM is still the
only surveyed tool covering all three surfaces locally; the alternatives either fail agent-agnostic
([[candidate-memsearch]], [[candidate-mempalace]], [[candidate-dox-agents-md]] as stated) or local-first
([[candidate-openbrain]], mem0, team-mode Supabase designs).

[[concept-six-levels-of-memory]] · [[concept-storage-injection-recall-matrix]] · [[concept-bm25-vs-semantic-recall]] · [[concept-agent-agnostic-gap]] · [[concept-context-rot]] · [[concept-agent-harness]] · [[candidate-memsearch]]
