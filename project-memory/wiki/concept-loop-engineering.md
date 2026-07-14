# concept: Loop engineering

Loop engineering is the practice of designing agent loops with a trigger, a verifiable goal, and repeated
agent execution until the goal is met.

## Why it matters here

[[source-loop-engineering]] is not a memory-system source, but it points at a likely maintenance mechanism:
recurring lint/gardening loops for memory. The risk is cost and drift. A memory loop should run only when
the goal is bounded and testable, such as:

- broken wikilinks are repaired;
- source-register coverage matches raw files;
- stale pages are flagged, not silently rewritten;
- index entries exist for durable pages.

Amorphous goals such as "make the wiki better" should stay human-triggered until they can be made
verifiable.

## Transcript-backed loop lessons

The Telegram videos are now transcript-backed rather than preview-only. [[source-stop-prompting-claude-start-loop-engineering]]
and [[source-claude-code-works-better-with-loops-not-prompts]] both make memory/output part of the loop
contract: every iteration should leave durable state that a later iteration can inspect. [[source-finally-agent-loops-clearly-explained]]
adds the strongest guardrail: verification and done criteria matter more than the loop's shape. A loop is
worth running only when the agent can check the target state.

[[source-the-creators-of-claude-code-and-openclaw-don-t-prompt-their-agents-any]] is the cautionary source:
parallel loops need observability, run history, cost controls, and human gates because hallucinations can
compound. For this wiki, that means no invisible "make the wiki better" loop. Good loop targets are
mechanical and auditable: raw/register coverage, dangling wikilinks, missing index rows, stale questions, and
source-backed claim checks.

[[source-self-improving-system-claude-code]] adds a practical framing that fits the same caution: the loop
should learn from real usage and explicit feedback, not from a fantasy of total autonomy. Its strongest
useful idea is to couple loops to tested ingest skills and concrete pipelines first, then compress feedback
cycles once the system is in use.

[[source-four-levels-of-loop-engineering]] sharpens the feedback model. Not all checks are equal:
computational checks (tests, linters, type checks, structural analysis) are cheap and deterministic, while
inferential checks are slower and model-based. The source also makes three governance points explicit: weak
checkers make `/goal` look smarter than it is, concurrent work needs isolation such as worktrees, and loop
design is incomplete if it ignores soft caps, token cost, and where a human should stay in the loop.

## Cross-links

[[source-loop-engineering]] · [[source-stop-prompting-claude-start-loop-engineering]] ·
[[source-finally-agent-loops-clearly-explained]] · [[source-claude-code-works-better-with-loops-not-prompts]] ·
[[source-the-creators-of-claude-code-and-openclaw-don-t-prompt-their-agents-any]] ·
[[source-self-improving-system-claude-code]] ·
[[source-four-levels-of-loop-engineering]] ·
[[concept-agent-harness]] · [[concept-agent-legibility]]
