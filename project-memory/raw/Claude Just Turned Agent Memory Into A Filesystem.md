---
title: "Claude Just Turned Agent Memory Into A Filesystem"
source: "https://www.youtube.com/watch?v=EQWEAUumEAw"
author:
  - "[[Prism Labs]]"
published: 2026-04-24
created: 2026-06-28
description: "Anthropic shipped Managed Agents Memory on April 23, 2026 — a memory layer for Claude Platform agents that stores agent state as exportable, versioned text files at /mnt/memory/ in..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=EQWEAUumEAw)

Anthropic shipped Managed Agents Memory on April 23, 2026 — a memory layer for Claude Platform agents that stores agent state as exportable, versioned text files at /mnt/memory/ instead of an opaque vector database. In this breakdown we cover the files-not-vectors architecture, the Python SDK for creating and attaching memory stores, immutable versioning with memver_ prefixed entries, the redact endpoint for GDPR compliance, Rakuten's 97%-fewer-first-pass-errors result, how it stacks up against ChatGPT Memory / Mem0 / Letta / LangGraph, the prompt injection risk Anthropic explicitly flags, and the honest limitations before you adopt it.

Blog post: https://claude.com/blog/claude-managed-agents-memory
Docs: https://platform.claude.com/docs/en/managed-agents/memory
Engineering deep-dive: https://www.anthropic.com/engineering/managed-agents

## Transcript

**0:00** · Anthropic just shipped managed agents

**0:01** · memory and the architecture decision

**0:04** · they made is worth paying attention to.

**0:06** · This is not a vector database. This is

**0:08** · not an opaque managed blob like chat GPT

**0:10** · memory. Every memory is a text file

**0:12** · mounted at /mnt/memory.

**0:15** · Versioned, exportable, redactable.

**0:18** · Rakuten is already using it in

**0:19** · production. 97% fewer first pass errors,

**0:23** · 27% lower cost. Let's break down what

**0:26** · actually shipped and why the files not

**0:27** · vectors approach matters. 2-minute

**0:30** · explanation first. Managed agents is

**0:32** · Anthropic's production harness on the

**0:33** · Claude platform. It launched in public

**0:36** · beta mid-April 2026. It is distinct from

**0:39** · Claude Code and Claude Co-work. Those

**0:41** · are end-user products. Managed agents is

**0:44** · the runtime for developers building

**0:45** · their own agents on top of Claude.

**0:48** · Today's memory release is a layer added

**0:50** · on top of that. Think of it as the

**0:52** · storage primitive that turns a stateless

**0:54** · agent into a stateful one. Without you

**0:56** · having to wire up a database, a

**0:58** · checkpointer, or a vector index. Claude

**1:00** · platform handles the persistence. You

**1:02** · pay for it by the session hour. Here is

**1:04** · the architecture decision that matters.

**1:06** · When the agent session starts, a memory

**1:09** · store is mounted at /mnt/memory.

**1:12** · A regular Linux file system. Directories

**1:15** · and text files. The agent reads and

**1:17** · writes to it using the bash tool it

**1:18** · already has. There's no special memory

**1:21** · API for the model. No embedding

**1:23** · similarity search, no vector DB under

**1:25** · the hood. You can cat the agent's

**1:27** · memory. You can grep it. You can get

**1:29** · diff it. That is the key design choice.

**1:31** · Memory is just files, which means

**1:33** · everything you already know about

**1:35** · debugging file systems applies to agent

**1:37** · memory now. What does the file system

**1:39** · actually look like at runtime? You

**1:41** · decide. Anthropic deliberately does not

**1:44** · impose a directory structure. You can

**1:46** · organize by user ID, by project, by

**1:48** · date, by feature. Whatever your agent

**1:51** · needs.

**1:52** · A typical setup might have a preferences

**1:54** · directory for per-user settings, a

**1:56** · projects directory for ongoing work, and

**1:58** · a lessons learned directory that the

**2:00** · agent appends to as it works.

**2:02** · The agent discovers memory by browsing

**2:04** · the tree the same way any shell user

**2:06** · would. One catch. Each individual memory

**2:09** · file is capped at 100 kilobytes, roughly

**2:11** · 25,000 tokens.

**2:13** · Anthropic is explicit. Many small files,

**2:16** · not a few large ones. Adoption is the

**2:18** · best validation for a beta product.

**2:21** · Anthropic named three customers in the

**2:22** · announcement. Rakuten reports 97% fewer

**2:25** · first pass errors, 27% lower cost, and

**2:29** · 34% lower latency running agents with

**2:31** · memory in production.

**2:33** · WiseDocs reports 30% faster document

**2:35** · verification.

**2:37** · Endo is quoted on the workflow

**2:38** · continuity angle. The beta limits tell

**2:40** · you who this is for. 1,000 stores per

**2:43** · org, 2,000 memories per store, 100

**2:45** · megabytes total per store, eight stores

**2:48** · attachable per session. That is

**2:49** · enterprise scale numbers. Hobbyists will

**2:52** · hit none of these. Enterprise teams

**2:54** · running hundreds of agents across

**2:55** · thousands of users will need the limit

**2:57** · raise ticket workflow. The announcement

**2:59** · is on claude.com, Anthropic's

**3:01** · post-co-work rebrand blog. The deep

**3:03** · engineering write-up is over on

**3:04** · anthropic.com/engineering.

**3:07** · Both are worth reading. The engineering

**3:09** · post gets into the session container

**3:11** · architecture, how memory stores mount

**3:13** · into isolated workspaces, and the

**3:15** · privacy model.

**3:16** · One subtle but important detail. Memory

**3:19** · stores are workspace scoped, not session

**3:21** · scoped. A single shared read-only store

**3:24** · can be attached to every session your

**3:25** · agent runs. That is how you distribute

**3:27** · updated reference material to a fleet of

**3:29** · agents without retraining or

**3:31** · re-embedding anything. If Anthropic

**3:33** · publishes a new onboarding doc, update

**3:35** · one file, and every agent in every

**3:37** · customer workspace sees the new copy on

**3:40** · next session start. The audit trail is

**3:42** · the feature that turns this from a

**3:43** · convenience layer into an enterprise

**3:45** · credible one.

**3:46** · Every write to a memory file creates an

**3:48** · immutable version with a member prefix.

**3:51** · Versions are retained for 30 days,

**3:53** · longer for recent ones. If legal or

**3:55** · compliance asks what the agent knew on

**3:57** · Tuesday, you can answer. For GDPR,

**4:00** · specifically right to be forgotten

**4:01** · requests, there is a redact endpoint

**4:04** · that scrubs the content of a specific

**4:05** · version while preserving the audit

**4:07** · record that a write happened. The audit

**4:09** · log stays intact. The sensitive content

**4:12** · is gone.

**4:13** · So C2 evidence is intact without

**4:15** · retaining personally identifiable

**4:17** · information indefinitely. Worth

**4:19** · comparing against the alternatives.

**4:21** · ChatGPT memory is a consumer feature,

**4:23** · per-user blob, no programmatic export,

**4:25** · no versioning. Mem0 is open source,

**4:28** · vector plus graph hybrid, scores 66.9%

**4:31** · on the Loco benchmark versus OpenAI's

**4:34** · 52.9. But it is SDK level. You bring

**4:37** · your own storage. Leda, formerly MemGPT,

**4:40** · is a full agent platform with core and

**4:42** · archival memory blocks, richer than

**4:44** · Claude's offering. But it is the whole

**4:46** · runtime, not just a memory API.

**4:49** · LangGraph ships persistent memory via

**4:51** · checkpointer plus store, but it is

**4:53** · framework bound to LangGraph. Claude

**4:55** · managed agents memory sits in a

**4:57** · different space. Managed enterprise

**4:59** · memory API with version control

**5:01** · primitives baked in. The differentiator

**5:03** · is operational simplicity. You do not

**5:06** · run a vector DB. You do not run a

**5:07** · checkpointer. You just call an API. One

**5:10** · limitation Anthropic calls out directly

**5:12** · in the docs is prompt injection. The

**5:15** · default access level for a memory store

**5:17** · is read-write, which means if your agent

**5:20** · processes untrusted input, a malicious

**5:22** · user can inject instructions that cause

**5:24** · the agent to write poisoned content into

**5:26** · memory. Next session, the agent reads

**5:29** · that memory and treats the poisoned

**5:30** · content as its own prior learning.

**5:32** · Anthropic's recommendation, use

**5:34** · read-only access for any shared

**5:36** · reference store, and keep read-write

**5:38** · scoped to trusted inputs only. This is

**5:40** · not a hypothetical. It is a warning box

**5:42** · in the docs for a reason. A few honest

**5:44** · limitations before you adopt it. One,

**5:47** · public beta, not GA. The beta header is

**5:49** · mandatory and limits are binding. Two,

**5:52** · no semantic search built in. It is a

**5:54** · file system. If you want embedding

**5:56** · similarity, you build it yourself on

**5:58** · top. Three, vendor lock-in. Your memory

**6:01** · files live in Anthropic's managed

**6:02** · infrastructure. Export is possible, but

**6:05** · there is no import from Mem0 or Leda.

**6:07** · Four, prompt injection is a real risk,

**6:10** · especially with the read-write default.

**6:12** · Five, versions evaporate after 30 days

**6:15** · unless you actively export them. If you

**6:17** · need long-term audit evidence, that is

**6:19** · your responsibility, not Anthropic's.

**6:21** · Six, memory stores attach at session

**6:24** · creation only. You cannot hot mount a

**6:26** · new store mid-session. Worth budgeting

**6:28** · for all of this before you commit to it

**6:30** · as your agent's memory layer. Managed

**6:32** · agents memory is the cleanest enterprise

**6:34** · memory API on the market today.

**6:37** · The files not vectors decision is a

**6:39** · meaningful architectural bet. It trades

**6:42** · semantic search convenience for

**6:43** · operational simplicity and auditability.

**6:46** · For teams building production agents

**6:48** · where the memory layer has to pass

**6:49** · compliance review, that trade is worth

**6:51** · making.

**6:52** · For hobbyists and researchers, Mem0 or

**6:55** · Leda still win on flexibility. Pick your

**6:57** · primitive based on who asks the

**6:59** · questions when things go wrong. If this

**7:01** · breakdown helped, subscribe at prism

**7:03** · labs AI. We cover every Anthropic,

**7:06** · OpenAI, and open source AI drop as it

**7:08** · ships. Blog post and docs link in the

**7:11** · description. See you in the next one.
