# concept: Context engineering

Context engineering is the discipline of deciding what information enters an agent's limited context at each
step. It includes prompts, tools, memory, external data, retrieval, message history, compaction, and
structured notes.

## Core rule

[[source-effective-context-engineering]] states the practical target: use the smallest high-signal context
set that maximizes the desired outcome. That fits this project's local-memory bias better than any approach
that dumps a whole vault or huge instruction file into every session.

## Techniques relevant to local memory

- Use lightweight references such as file paths, indexes, and links; load full content just in time.
- Treat file hierarchy, names, and timestamps as metadata agents can use for navigation.
- Use compaction for long-running sessions, but tune it for high recall before optimizing precision.
- Use structured note-taking / agentic memory for durable state outside the context window.
- Use subagents when detailed exploration would pollute the lead agent's context.

## Implication for the architecture choice

The selected product should optimize for routing and progressive disclosure: a small always-loaded map,
durable local notes/pages, and operations that let agents fetch the right page when needed.

## Transcript-backed additions

The Telegram-saved videos now add transcript-backed evidence rather than preview leads. The recurring pattern
is progressive disclosure through files: [[source-claude-managed-agents-memory]] describes managed-agent
memory mounted as files, [[source-google-okf]] uses indexes and Markdown links,
[[source-karpathy-obsidian-no-rag-wiki]] relies on a maintained index before opening deeper pages, and
[[source-anthropic-teams-claude-code]] favors short skills plus reference folders loaded only when needed.

The wider transcript set reinforces the same point from several angles. [[source-l8-principal-s-agentic-engineering-workflow]]
names global memory files and project-level memory files as practical workflow components. [[source-the-7-levels-of-using-claude-context-explained-in-24-min]]
frames Claude Code, Cowork, and Codex as surfaces that all need context infrastructure. [[source-master-all-7-levels-of-claude-code-memory]]
adds decay, promotion, multi-signal retrieval, salience, disclosure, and compaction as design axes.
[[source-creating-your-own-agentic-os-is-easy-insanely-powerful]] and
[[source-i-turned-claude-opus-4-8-into-my-entire-ai-operating-system]] translate this into AI-OS language:
context, connections, capabilities, and cadence are separate layers.

[[source-company-os-claude-code]] reinforces the same rule at team scale: a GitHub-based Company OS acts as
the durable context layer, but high-adoption delivery happens through just-in-time Slack/email workflows
rather than forcing everyone into a separate AI tab. That is strong evidence for separating stored context
from the surface where the task is triggered.

[[source-self-improving-system-claude-code]] adds a useful sequencing rule: first build the file-backed
knowledge base, then bulk-ingest historical material, then attach inflow pipelines for new information. In
other words, context infrastructure should be bootstrapped in layers rather than pretending that a loop can
improve an empty or half-populated store.

[[source-news-vacuum-agent-idea]] adds a domain-specific variant of the same rule: define the bounded signal
sources, the filtering behavior, the memory/store behavior, and the notification outputs first. That keeps a
news-ingest agent from degenerating into an unbounded "read everything" system.

[[source-ultimate-second-brain]] reinforces progressive disclosure through file structure rather than prompt
bulk. Raw data lands in the vault, the wiki organizes it, and outputs are generated from that organized
layer. Obsidian's graph and folder structure are not the point by themselves; they are navigation aids for a
markdown knowledge base the agent can keep extending.

[[source-smm-ai-hermes]] remains the clearest correction to preview-first classification. The Telegram preview
was insufficient, but the full transcript contains concrete context-engineering ideas: split broad work into
specialized agents to avoid context bloat, limit visible skills to relevant names/descriptions, use a
wiki/source-of-truth layer, and require agents to ask for missing information instead of inventing.

## Cross-links

[[source-effective-context-engineering]] · [[source-openai-harness-engineering-codex]] ·
[[source-telegram-saved-ai-youtube-videos]] · [[source-claude-managed-agents-memory]] ·
[[source-google-okf]] · [[source-karpathy-obsidian-no-rag-wiki]] · [[source-anthropic-teams-claude-code]] ·
[[source-company-os-claude-code]] ·
[[source-self-improving-system-claude-code]] ·
[[source-news-vacuum-agent-idea]] ·
[[source-ultimate-second-brain]] ·
[[source-l8-principal-s-agentic-engineering-workflow]] · [[source-master-all-7-levels-of-claude-code-memory]] ·
[[source-the-7-levels-of-using-claude-context-explained-in-24-min]] · [[source-smm-ai-hermes]] ·
[[concept-context-rot]] · [[concept-agent-legibility]] ·
[[candidate-observational-memory]]
