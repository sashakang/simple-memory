# concept: Agent legibility

Agent legibility is the property that the agent can inspect, validate, and modify the information it needs
without relying on human memory, private chat threads, or opaque external systems.

## Why it matters

[[source-openai-harness-engineering-codex]] says that anything Codex cannot access while running effectively
does not exist from the agent's point of view. The article's answer is repository-local, versioned knowledge:
a short `AGENTS.md` table of contents plus structured docs, plans, specs, references, generated schemas, and
mechanical freshness checks.

## Relationship to this project

Local memory should improve agent legibility, not merely store facts. That means:

- one clear local source of truth;
- small routing files that point to deeper pages;
- indexes and cross-links;
- source IDs or citations for claims;
- lint/gardening operations that find stale docs and broken links.

This is close to the Karpathy LLM Wiki method, but OpenAI's source adds an engineering-management lesson:
make the knowledge base mechanically checkable, not only readable.

[[source-google-okf]] and [[source-claude-managed-agents-memory]] convert two of those leads into
transcript-backed evidence: OKF is described as Git-tracked Markdown company knowledge with indexes and
progressive disclosure, and Anthropic managed-agent memory is described as text files mounted into agent
sessions. Both reinforce the legibility principle: agents should be able to inspect, diff, grep, route
through, and cite their knowledge. However, OKF still needs official-spec verification and Anthropic managed
memory is hosted, not local-first.

The transcript redo adds stronger operational evidence. [[source-how-this-ex-meta-l8-engineer-ships-40-prs-a-day-with-ai-agents-kun-che]]
and [[source-l8-principal-s-agentic-engineering-workflow]] show that high-throughput agent work depends on
first-class plans, validation tools, isolated worktrees, and merge criteria. [[source-introducing-visual-plan-rich-plans-for-claude-code-codex]]
adds a concrete artifact pattern: rich MDX plans and visual recaps can make agent intent and results easier
for humans to inspect than a long terminal Markdown essay.

The Nate B. Jones sources are especially relevant to ingest quality. [[source-i-built-a-deck-with-ai-then-made-a-second-ai-attack-it]]
argues for a truth layer around generated artifacts: sources, structure, creation, and hostile review.
[[source-the-one-ai-writing-hack-nobody-talks-about]] says the project room should contain source inventory,
missing-context lists, duplicate checks, and organized files before generation starts. That directly supports
the corrected rule for this vault: do not classify YouTube sources from Telegram previews when full raw
transcripts are available.

[[source-shopify-ceo-reveals-their-secret-ai-developer]] adds the company-rollout version of legibility:
private AI chats do not teach the organization. Shared, inspectable work surfaces preserve the scoping,
context loading, corrections, and judgment trail.

## Cross-links

[[source-openai-harness-engineering-codex]] · [[concept-context-engineering]] ·
[[source-telegram-saved-ai-youtube-videos]] · [[source-google-okf]] · [[source-claude-managed-agents-memory]] ·
[[source-how-this-ex-meta-l8-engineer-ships-40-prs-a-day-with-ai-agents-kun-che]] ·
[[source-l8-principal-s-agentic-engineering-workflow]] ·
[[source-i-built-a-deck-with-ai-then-made-a-second-ai-attack-it]] ·
[[source-the-one-ai-writing-hack-nobody-talks-about]] ·
[[candidate-google-okf]] · [[candidate-anthropic-managed-agents-memory]] · [[candidate-karpathy-llm-wiki]] ·
[[candidate-dox-agents-md]]
