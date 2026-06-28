# concept: Context rot

The inability of LLMs to reliably recall 100% of loaded context as the amount of loaded context grows.
Named explicitly in [[source-every-cc-memory-system-compared]] as **the problem every memory system exists to
solve**.

## Why it's the root motivation

If models recalled everything perfectly, you'd just dump all memory into context and be done. Because they
don't, the goal flips from *load more* to *load the **right** context at the **right** time*. Every level in
[[concept-six-levels-of-memory]] is a different bet on how to do that selective loading.

## Practical rules it implies

- Keep always-loaded files small (the source's heuristic: `CLAUDE.md` < ~200 lines); push bulky context to
  referenced files pulled on demand.
- **Injection beats storage:** a small always-loaded payload + on-demand recall outperforms one giant dumped
  file. This is why [[candidate-observational-memory]] budgets its startup injection (~24 KB) rather than
  loading the whole store — directly aligned with the anti-rot principle.
- Anthropic's unreleased "**Kairos**" daemon (from leaked Claude Code source) targets exactly this: background
  consolidation/pruning so the working set stays small.

## New evidence

[[source-dox-agents-md-framework]] frames the same problem as codebase context awareness: agents fail by
editing the wrong place, duplicating functionality, or missing conventions because they lack a map. Its
hierarchical `AGENTS.md` tree is a local routing answer to context rot.

[[source-claude-second-brain-levels]] adds a second practical rule: not all data should be ingested. Durable,
evergreen context belongs in memory; transient Slack/email/customer chatter should usually stay queryable at
the source so it does not become noise.

[[source-agent-harness]] explains the harness side of the same issue: compaction, prompt assembly, and hooks
decide what survives in context and what is loaded on demand.

[[source-effective-context-engineering]] is the strongest official source for the underlying principle:
context is finite, has diminishing returns, and should be curated into the smallest high-signal token set.
It explicitly favors just-in-time retrieval through file paths, stored queries, links, and tools.

[[source-openai-harness-engineering-codex]] shows the same principle in Codex practice: one giant
`AGENTS.md` failed, so the team moved to a short map plus structured local docs and mechanical freshness
checks.

[[concept-six-levels-of-memory]] · [[candidate-observational-memory]] · [[candidate-dox-agents-md]] ·
[[concept-agent-harness]] · [[concept-context-engineering]]
