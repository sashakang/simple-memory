# candidate: Karpathy LLM Wiki

- **Gist:** https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
- **Level:** 5 (self-organizing KB) in [[concept-six-levels-of-memory]]
- **Sources:** [[source-every-cc-memory-system-compared]], [[source-claude-second-brain-levels]],
  [[source-self-evolving-claude-code-memory]], [[source-karpathy-obsidian-no-rag-wiki]] (+ the project's
  own charter / dogfooded method)

## What it is

A *pattern*, not a tool: a `raw/` folder (source docs the LLM reads but never writes) + a `wiki/` folder the
LLM owns completely (writes every file, maintains structure, updates wikilink cross-references). All plain
markdown; Obsidian gives humans a knowledge graph. Three ops: ingest / query / lint. (This project itself runs
on this pattern — see the schema in `CLAUDE.md` / `AGENTS.md`.)

Community implementations to verify against code (charter candidate landscape): Astro-Han/karpathy-llm-wiki,
Pratiyush/llm-wiki, lucasastorian/llmwiki, toolboxmd/karpathy-wiki, yologdev/yopedia. Hosted clone:
[[candidate-recall]]. Heavyweight knowledge-graph cousin: LightRAG (enterprise overkill per the source).

## The sources' key caveat (important for us)

Simon Scrapes is **explicitly lukewarm on Level 5 for *operational* memory**: he sees the LLM Wiki as a
**deep-research / second-brain** tool ("a Wikipedia on a topic," best for a "save-for-later" pile you want
interlinked), **not** for "what did we decide about client X's landing page in March." He'd skip it for casual
consumption and can't see direct operational use beyond topic research.

[[source-claude-second-brain-levels]] is more favorable: it places LLM Wiki at Level 2 and says it can work
well when the agent has clear routing, indexes, and durable markdown pages. The combined view is nuanced:
LLM Wiki is excellent for curated, evergreen synthesis and project research, but it needs an explicit
operational write/recall layer before it can be the company-wide memory product.

## Against our constraints + the two-things distinction

- **(a):** ⚠️ pattern is agent-agnostic in principle; real coverage depends on the specific implementation
  (some claim Codex/Cursor — must verify against code, not READMEs).
- **(b) ✅ / (c) ✅ / (d):** depends on implementation's install path.
- **Crucial distinction (from the charter):** the LLM Wiki is **both** (1) the *method* this project uses for
  its own notes **and** (2) a *candidate product*. The source's caveat lands on (2): as the shipped
  *operational* memory for a coding-agent fleet, a wiki is the wrong shape — that role wants the curated,
  injected, recall-on-demand design of [[candidate-observational-memory]], not a research wiki. The method (1)
  remains how we take these very notes.

Agent Skills may be one way to package the operation layer. See [[concept-agent-skills-standard]].
[[source-openai-harness-engineering-codex]] adds one requirement if this pattern becomes the selected product:
the wiki needs mechanical health checks (freshness, links, ownership/source coverage), not only agent-written
markdown.

Two Telegram-saved leads are now transcript-backed. [[source-self-evolving-claude-code-memory]] describes
an internal-memory variant where Claude Code hooks capture session summaries as raw material, then a daily
flush promotes lessons into the wiki; session-start loads `AGENTS.md` and the wiki index.
[[source-karpathy-obsidian-no-rag-wiki]] gives a fuller walkthrough of raw/wiki/schema, ingest/query/lint,
source citations, index maintenance, and scale caveats.

[[source-ultimate-second-brain]] adds a newer, more operator-facing walkthrough of the same pattern. The
useful reinforcement is practical rather than theoretical: Obsidian is presented as an optional local UI for
plain markdown, the raw/wiki split is explicit, graph view helps human navigation, and Kanban sits as an
operations layer beside the wiki rather than replacing it. That strengthens the pattern as a real workflow,
though it still does not by itself prove the pattern as the final operational memory product across all
required surfaces.

This strengthens the pattern as a research and synthesis system, and it strengthens hooks+logs as a possible
operational-memory layer. It does **not** close the product decision: the described implementations are still
Claude Code / Claude Agent SDK centered, not proven across Codex CLI and Claude Cowork.

The full Telegram redo sharpens the process lesson. [[source-i-built-a-deck-with-ai-then-made-a-second-ai-attack-it]]
and [[source-the-one-ai-writing-hack-nobody-talks-about]] both support the wiki method's insistence on raw
sources before synthesis: the source inventory and truth layer are the work, not administrative overhead.
[[source-master-all-7-levels-of-claude-code-memory]] supports the evaluation method itself: clone/audit
candidate memory repos, extract building blocks, and write a lightweight spec instead of copying a memory
system whole. [[source-l8-principal-s-agentic-engineering-workflow]] adds a practical bridge from wiki-style
knowledge to coding work: global/project memory files, skills, validation, and worktrees are the harness
pieces that determine whether the knowledge is actually used.

[[concept-six-levels-of-memory]] · [[candidate-observational-memory]] · [[candidate-recall]] ·
[[concept-agent-skills-standard]] · [[concept-agent-legibility]] ·
[[source-telegram-saved-ai-youtube-videos]] · [[source-self-evolving-claude-code-memory]] ·
[[source-karpathy-obsidian-no-rag-wiki]] · [[source-master-all-7-levels-of-claude-code-memory]] ·
[[source-l8-principal-s-agentic-engineering-workflow]] · [[source-ultimate-second-brain]]
