# candidate: John & Paweł hook system (Level 2)

- **Source article:** youngleaders.tech "how I finally sorted my Claude Code memory" (John Connolly,
  implementing Paweł Huryn's "how to give Claude code memory")
- **Level:** 2 (reliable recall) in [[concept-six-levels-of-memory]]
- **Source:** [[source-every-cc-memory-system-compared]]

## What it is

A `CLAUDE.md`-pasted memory-management prompt + a **session-start hook**. Structure rooted at `.claude/memory/`:
`general.md` (cross-project facts/prefs/env), `domain/<topic>.md` (one file per domain), `tools/<tool>.md`
(per-tool config + edge cases), all indexed by `memory.md`. The hook injects only the **index** (not full
content) before the first tool call of every session, including sub-agents. A "**reorganize memory**" command
dedups / merges / prunes empties / resolves stale threads / adds cross-references / re-sorts by date. Optional
team-sharing of domain files via a shared folder.

## Against our constraints

- **(a):** ⚠️ Claude-Code hook–specific as written; the *pattern* (shared `.md` + per-agent session-start shim)
  is portable, which is exactly how [[candidate-observational-memory]] generalizes it to 3 surfaces.
- **(b):** ✅ plain markdown + one shell hook — passes cleanly.
- **(c):** ✅ local. **(d):** ✅ two-prompt setup.

## Relevance

This is the **conceptual parent of OM**: hook-injected index + manual curation command. OM productizes it
(curation moved *inside* `om observe`, budgeted injection, conflict/staleness automation, 3-surface install)
rather than relying on a user-run "reorganize" prompt. The closest thing in the field to "OM minus the
packaging." See [[concept-storage-injection-recall-matrix]].

[[concept-six-levels-of-memory]] · [[candidate-observational-memory]]
