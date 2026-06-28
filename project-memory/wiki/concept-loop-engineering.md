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

## Cross-links

[[source-loop-engineering]] · [[source-stop-prompting-claude-start-loop-engineering]] ·
[[source-finally-agent-loops-clearly-explained]] · [[source-claude-code-works-better-with-loops-not-prompts]] ·
[[source-the-creators-of-claude-code-and-openclaw-don-t-prompt-their-agents-any]] ·
[[concept-agent-harness]] · [[concept-agent-legibility]]
