# candidate: OpenBrain (OB1, Nate Jones)

- **Repo:** https://github.com/NateBJones-Projects/OB1
- **Level:** 6 (one brain for all tools) in [[concept-six-levels-of-memory]]
- **Source:** [[source-every-cc-memory-system-compared]]

## What it is

A cross-tool memory layer: **one Postgres database on Supabase** with a single `thoughts` table (each row =
text + embedding vector + tags + timestamp), semantic search via Postgres extensions. An **MCP server** plus
Supabase **edge functions** act as a front door so Claude Code, ChatGPT, Codex, Cursor, and Claude desktop all
read/write the *same* brain. You own the Supabase project (exportable Postgres), ~$0–0.30/mo on the free tier,
~30–45 min AI-assisted setup, companion prompts to migrate from existing CC memory systems.

## Against our four constraints

- **(a) Agent-agnostic:** ✅✅ the **only** level that is genuinely cross-tool by design — and it covers more
  than our three surfaces. This is its one real strength for us.
- **(b) Simplistic:** ❌ Postgres + Supabase + MCP server + edge functions; longest setup of any level.
- **(c) Local-first:** ❌ **fails outright** — state lives in a hosted DB; every read is a network query (adds
  latency). Directly violates our charter's local-first bar.
- **(d) Installable:** ⚠️ 30–45 min, non-trivial for a non-author.

## Verdict for us

The clearest illustration of the central tension: **the only truly cross-tool option pays for it by abandoning
local-first.** Our charter resolves this the other way — reach all three surfaces via a *shared local file +
per-agent shims* (the [[candidate-observational-memory]] approach), not a shared remote DB. So OpenBrain is the
instructive anti-pattern for constraint (c), not a contender. **mem0** is the hosted-SaaS cousin (data on their
servers permanently) — same disqualification, less ownership.

[[concept-six-levels-of-memory]] · [[concept-agent-agnostic-gap]] · [[candidate-mem0]]
