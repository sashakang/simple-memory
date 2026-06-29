# Log

Chronological, append-only record of every operation (ingest / query / lint).
Newest at the bottom. Each entry starts with a parseable prefix so it can be grepped:

```
grep "^## \[" log.md | tail -5
```

Prefix format: `## [YYYY-MM-DD] <op> | <title>` where `<op>` is `ingest`, `query`, or `lint`.

---

## [2026-06-11] init | wiki scaffolded

Bootstrapped from Karpathy's LLM Wiki gist. Created `raw/` (empty), `wiki/index.md`,
`wiki/log.md`. Schema lives in the project `CLAUDE.md`. No sources ingested yet.

## [2026-06-15] ingest | Every Claude Code Memory System Compared (Simon Scrapes)

First substantive ingest. Created source page + 5 concept pages (six-levels, storage-injection-recall
matrix, bm25-vs-semantic, agent-agnostic-gap, context-rot) + 8 candidate pages (observational-memory,
memsearch, mempalace, openbrain, mem0, recall, john-pawel-hook-system, karpathy-llm-wiki). Source maps a
6-level taxonomy onto our 4 constraints — our bar carves at level 3; sharpens BM25 doubt and names memsearch
as OM's upgrade path. No decision recorded (deferred). Open gap: earlier Simon Scrapes clipping still
un-ingested (`source-best-claude-memory-system` dangling).

## [2026-06-27] ingest | Six new local-memory and agent-infrastructure sources

Ingested eleven raw sources: Simon Scrapes hybrid Claude memory, Nate Herk second-brain levels,
MemGraphRAG, DOX hierarchical `AGENTS.md`, Agent Skills, agent harness architecture, Anthropic's skill
guide, Anthropic context engineering, OpenAI Codex harness engineering, a harness-engineering podcast, and
loop engineering. Added `source-register.md` and `research-questions.md`; created source pages,
[[candidate-dox-agents-md]], [[concept-agent-harness]], [[concept-agent-skills-standard]],
[[concept-context-engineering]], [[concept-agent-legibility]], and [[concept-loop-engineering]]. Updated core
synthesis around storage/injection/recall, agent-agnostic shims, BM25-vs-semantic recall, context rot, OM,
memsearch, Karpathy LLM Wiki, skills, harnesses, and repo-local knowledge. Net: new sources reinforce
"lowest sufficient local markdown layer first"; no decision recorded.

## [2026-06-27] ingest | Telegram Saved AI YouTube videos

Opened Telegram Web Saved Messages and collected saved YouTube links visible through browser scrolling.
Created raw capture `Telegram Saved AI YouTube Videos 2026-06-27.md` and
[[source-telegram-saved-ai-youtube-videos]]. Ingested as a triage source, not full transcripts: 30
AI-related videos were new to memory; duplicates of [[source-every-cc-memory-system-compared]] and
[[source-best-claude-memory-system]] were skipped; two non-AI videos and four unclassifiable bare IDs were
skipped. Updated index, source register, research questions, and concept pages for context engineering,
agent legibility, loop engineering, and Karpathy LLM Wiki. No decision recorded.

## [2026-06-28] ingest | Five Telegram Saved AI YouTube priority transcripts

Fetched English auto-generated YouTube captions plus video metadata for the five highest-priority
Telegram-saved AI/local-memory videos and saved them as five individual Obsidian-style raw source files
with frontmatter, YouTube embeds, descriptions, and full timestamped transcripts. Created
[[source-claude-managed-agents-memory]], [[source-google-okf]],
[[source-self-evolving-claude-code-memory]], [[source-karpathy-obsidian-no-rag-wiki]],
[[source-anthropic-teams-claude-code]], [[candidate-google-okf]], and
[[candidate-anthropic-managed-agents-memory]]. Updated the earlier Telegram triage page, Karpathy LLM Wiki,
agent legibility, context engineering, Agent Skills, agent-agnostic gap, source register, index, and research
questions. No decision recorded; product/spec claims still need official-doc or repo verification.

## [2026-06-28] ingest | Remaining Telegram Saved AI YouTube transcripts

Saved and registered 26 additional standalone raw YouTube transcript files from the Telegram Saved Messages AI backlog. Added source pages and index/register entries for each. These are transcript-backed raw sources; detailed product claims still need source-specific review before affecting the architecture decision.

## [2026-06-28] ingest | Correct xep4LzDheAM preview miss

Reviewed the manually saved Obsidian-style raw file for `xep4LzDheAM` and corrected the earlier preview-only
classification. Updated [[source-smm-ai-hermes]], [[source-telegram-saved-ai-youtube-videos]],
[[concept-agent-harness]], and [[concept-context-engineering]]. Added a source-capture rule to `AGENTS.md`
and `CLAUDE.md`: Telegram/YouTube sources should be classified from full Obsidian-style raw captures, not
link previews or synthetic substitutes.

## [2026-06-28] ingest | Redo Telegram Saved AI YouTube transcript synthesis

Re-read the standalone raw transcript files created from the Telegram Saved Messages AI backlog and replaced
the placeholder source pages with transcript-backed summaries. Updated [[source-telegram-saved-ai-youtube-videos]],
[[concept-loop-engineering]], [[concept-context-engineering]], [[concept-agent-skills-standard]],
[[concept-agent-legibility]], [[concept-agent-harness]], [[concept-agent-agnostic-gap]],
[[concept-storage-injection-recall-matrix]], [[candidate-karpathy-llm-wiki]], [[research-questions]], and
[[index]]. Key correction: the raw transcript files are now the evidence layer; Telegram previews are only
triage metadata.

## [2026-06-29] ingest | How to Build a Company OS in Claude Code

Fetched the YouTube auto-generated transcript and metadata for Jiaona Zhang's Company OS interview, saved
the standalone raw file, and added [[source-company-os-claude-code]]. Updated [[source-register]],
[[index]], [[concept-agent-skills-standard]], [[concept-agent-harness]],
[[concept-context-engineering]], and [[concept-agent-legibility]]. Net new evidence: GitHub files +
playbooks + skills + Slack delivery can be framed as one company operating layer, with AI Ops as the
ownership function and "captains" as end-to-end feature owners.
