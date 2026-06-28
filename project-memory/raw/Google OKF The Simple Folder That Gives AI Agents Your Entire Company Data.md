---
title: "Google OKF: The Simple Folder That Gives AI Agents Your Entire Company Data"
source: "https://www.youtube.com/watch?v=fI7hZap7mZ4"
author:
  - "[[Cloud Codes]]"
published: 2026-06-27
created: 2026-06-28
description: "How do you give an AI agent your company's exact context without building an expensive RAG pipeline or Vector Database? Enter Google OKF (Open Knowledge Format v0.1)—a new open sta..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=fI7hZap7mZ4)

How do you give an AI agent your company's exact context without building an expensive RAG pipeline or Vector Database? Enter Google OKF (Open Knowledge Format v0.1)—a new open standard that packages your organizational knowledge as a simple, version-controlled directory of markdown files.

In this video, Cloud Codes provides a practical guide on how to structure company knowledge for AI agents using OKF. We break down the anatomy of an OKF file (YAML frontmatter + Markdown body), how markdown links create a navigable graph for agents, and how "progressive disclosure" keeps your LLM context window clean. 

We also explore how Google's BigQuery enrichment agent can auto-draft these files for you, why this "LLM Wiki" approach beats traditional human-only wikis like Notion or Confluence, and exactly how OKF pairs perfectly with MCP (Model Context Protocol). If MCP is the socket, OKF is the data flowing through it.

⏱️ TIMESTAMPS:
0:00 - The AI Agent Context Problem (Data Silos)
0:47 - What is Google OKF (Open Knowledge Format)?
1:07 - Why AI Agents Need Structured Memory
1:48 - Andrej Karpathy's "LLM Wiki" Concept
1:63 - The Anatomy of an OKF File (YAML + Markdown)
2:21 - Building a Knowledge Graph (Links & Bundles)
2:46 - Progressive Disclosure & Log Files
2:87 - Google's BigQuery Enrichment Agent
3:64 - OKF vs. Wikis & RAG (Vector Databases)
3:94 - OKF vs. MCP (Model Context Protocol)
4:20 - The Honest Verdict on v0.1


#googleokf #aiagents #systemdesign #rag #mcp #softwareengineering #googlecloud #cloudcodes

👇 SUBSCRIBE & WATCH NEXT
Subscribe for a new systems deep-dive every week: https://www.youtube.com/channel/UCoJT6Ip2dIqcDK_hM_v6Jcw?sub_confirmation=1

📱 CONNECT WITH US
Twitter/X:  x.com/cloud_codes
Join our developer community: discord.gg/HVnH9SY48

User Queries: 
what is google okf
open knowledge format tutorial
how to structure data for ai agents
google okf vs mcp
model context protocol vs okf
okf vs rag vector database
how to build an llm wiki
google cloud okf markdown explained
give ai agents company context
replace confluence with ai wiki

## Transcript

**0:00** · Your AI agent can write code, query a

**0:02** · database, and send an email, but ask it

**0:05** · one simple thing. What is our official

**0:07** · definition of an active user? And it has

**0:09** · no idea. It is brilliant, and it knows

**0:11** · nothing about your company, because that

**0:13** · knowledge is not in one place. It is

**0:16** · scattered across a Confluence page, a

**0:18** · Notion doc, a Slack thread, a comment

**0:21** · buried in some code, a schema in

**0:23** · BigQuery, and a dozen things that only

**0:25** · live inside someone's head. So, every

**0:27** · agent you build has to go find it, read

**0:30** · it, and figure it out all over again.

**0:32** · Same documents, same guesswork every

**0:34** · single time. Google calls this solving

**0:36** · context assembly from scratch. But what

**0:39** · if you wrote it down just once, in one

**0:41** · shared format every agent could read?

**0:43** · All of those scattered sources would

**0:45** · collapse into a single tidy folder. That

**0:47** · is the Open Knowledge Format, OKF, an

**0:50** · open specification from Google Cloud,

**0:52** · released this month under the Apache

**0:54** · license, and it is almost shockingly

**0:56** · simple. There is no database, no

**0:59** · vectors, no platform to log into.

**1:02** · An OKF knowledge base is just a folder

**1:04** · of plain Markdown files sitting in a Git

**1:06** · repository. Each file describes exactly

**1:09** · one thing, one table, one metric, one

**1:12** · runbook. Here's the canonical definition

**1:15** · of your orders table written as a single

**1:17** · Markdown file. At the very top sits a

**1:19** · tiny block of YAML, and the only field

**1:22** · that OKF actually requires is one word,

**1:25** · type. Every other field is optional.

**1:27** · Now, when an agent needs to understand

**1:29** · your business, it just opens the file

**1:31** · and reads it like a new hire reading the

**1:33** · handbook. No retrieval pipeline

**1:35** · required. Think of it this way. If MCP

**1:38** · is the socket that connects an agent to

**1:40** · your tools, then OKF is the knowledge

**1:42** · that flows through it. Write it once,

**1:45** · and every agent simply knows. Let us

**1:47** · slow down and look at why this matters

**1:49** · so much. Modern agents are genuinely

**1:51** · great at doing things. What they are bad

**1:53** · at is just knowing things, the

**1:55** · institutional memory a tenured employee

**1:57** · carries around without even thinking and

**2:00** · that memory is made of small specific

**2:02** · facts. Which metric definition is the

**2:04** · canonical one?

**2:06** · What this column actually means? Which

**2:08** · run book applies in the EU region? Which

**2:10** · API endpoint is quietly deprecated? The

**2:13** · exact join path between two tables?

**2:16** · Today every team rebuilds that context

**2:18** · by hand. Every agent project resolves

**2:20** · the same problem. Every catalog vendor

**2:23** · reinvents the same data model and the

**2:25** · knowledge stays locked behind whatever

**2:27** · tool happened to create it. So why not

**2:29** · just keep a wiki? Because humans abandon

**2:31** · them. As Andre Karpathy put it,

**2:34** · "Language models do not get bored, do

**2:36** · not forget to update a cross-reference,

**2:38** · and can touch 15 files in one pass." The

**2:40** · bookkeeping we hate is exactly what they

**2:42** · are good at. So here's how a single OKF

**2:45** · document is actually built. It has two

**2:47** · parts, a block of structured metadata at

**2:50** · the top and a free-form markdown body

**2:52** · underneath. That is the entire file. The

**2:55** · metadata is YAML and the one required

**2:57** · field is type. It is a short label,

**3:00** · BigQuery table, metric, run book, play

**3:03** · book, and agents use it to route, to

**3:06** · filter, and to decide what they are even

**3:07** · looking at. You invent the types you

**3:10** · need. Nothing is centrally registered.

**3:12** · Five more fields are recommended and all

**3:14** · of them are optional. A title, a

**3:17** · one-line description, a resource link to

**3:19** · the real asset, a few tags, and a

**3:21** · timestamp. You can add your own keys,

**3:24** · too. And a good reader keeps the ones it

**3:26** · does not recognize. Below the metadata,

**3:28** · the body is just plain markdown. For a

**3:31** · table, that is the schema. For a metric,

**3:33** · the exact formula. For a run book, the

**3:35** · steps. Whatever a human would want to

**3:38** · read, written for both humans and

**3:40** · machines at once. And the documents link

**3:42** · to each other using ordinary markdown

**3:44** · links. A foreign key points to the

**3:46** · customer's file. A metric points to the

**3:48** · table it is built on. Together, they

**3:50** · form a navigable graph of your whole

**3:52** · business. A whole collection of these is

**3:54** · called a bundle, and a bundle is simply

**3:56** · a directory tree. Data sets, tables, and

**3:59** · metrics, each in its own folder. The

**4:01** · structure mirrors how your team already

**4:03** · thinks, not some rigid schema. Each

**4:06** · folder can hold an index file, a simple

**4:09** · table of contents. And this is the

**4:11** · clever part. An agent reads the index

**4:13** · first and decides what is worth opening,

**4:15** · instead of pulling every single file

**4:17** · into its context window. They call it

**4:19** · progressive disclosure. There is also an

**4:22** · optional log file, a change log, with

**4:24** · the newest entries first. Because this

**4:26** · knowledge base is managed exactly like

**4:28** · code, kept in version control, reviewed

**4:31** · in pull requests, with a history of

**4:33** · every change. And the spec is

**4:35** · deliberately forgiving. A consumer must

**4:37** · tolerate a broken link, an unknown

**4:39** · field, or a type it has never seen

**4:41** · before. Real knowledge is always

**4:43** · half-finished. So, OKF is built to keep

**4:46** · working while it grows. Now, you are not

**4:48** · writing hundreds of these by hand.

**4:50** · Google ships a reference enrichment

**4:52** · agent. You point it at a big query data

**4:55** · set, and it walks every table and every

**4:57** · view, and drafts an OKF document for

**4:59** · each one automatically. Then a second

**5:01** · pass goes further. It reads your actual

**5:04** · documentation and fills each draft in

**5:06** · with schemas, join paths, and citations

**5:09** · back to the source. You review and

**5:11** · curate. The machine does the typing. It

**5:14** · even comes with three ready-made sample

**5:15** · bundles: Google Analytics, Stack

**5:18** · Overflow, and Bitcoin data. Plus a

**5:20** · little HTML viewer, so you can browse a

**5:22** · whole bundle like a tiny website. And

**5:25** · Google's knowledge catalog can ingest a

**5:27** · bundle and serve it straight to your

**5:28** · agents. So, the very same files you keep

**5:31** · in Git become live context at runtime.

**5:33** · The wiki and the runtime are one thing.

**5:36** · Underneath all of it sit three rules. It

**5:39** · is minimally opinionated, exactly one

**5:41** · required field. The producer and the

**5:43** · consumer are fully independent. And it

**5:45** · is a format, not a platform. No SDK, no

**5:49** · account, no lock-in. So, how do you

**5:51** · actually start? Pick one painful domain,

**5:54** · draft the documents by hand or with the

**5:56** · agent, curate them with the people who

**5:58** · really know, link them together, commit

**6:01** · it all to a repo, then point an agent at

**6:03** · it and watch. So, how is this different

**6:06** · from a wiki? A wiki is written for

**6:08** · humans in prose and locked inside

**6:10** · Confluence or Notion. OKF is written for

**6:13** · agents in plain text and it travels

**6:15** · anywhere. Same knowledge, just a

**6:17** · machine-first shape. And what about RAG,

**6:20** · embeddings and a vector database? That

**6:22** · is fuzzy search over chunks you hope are

**6:24** · relevant. OKF is the opposite, curated,

**6:27** · structured facts that an agent navigates

**6:30** · on purpose. You can still do both, but

**6:32** · here the truth is hand-kept and it does

**6:34** · not replace MCP. It completes it. MCP

**6:38** · gives an agent the connections, the

**6:39** · tools, and the live data. OKF gives it

**6:42** · the meaning, what those things are and

**6:44** · how your company actually uses them. The

**6:46** · socket and the content. This is the

**6:48** · quiet genius of the whole idea. It is

**6:50** · just files. You can read them in any

**6:52** · editor, render them on GitHub, ship them

**6:55** · as a zip, and diff them in a pull

**6:57** · request. No vendor owns your company's

**6:59** · knowledge. Now, let us be honest about

**7:01** · where this stands. It is version 0.1, a

**7:04** · starting point in Google's own words,

**7:07** · not a finished standard. Adoption is

**7:09** · still early and the format does not

**7:11** · magically keep itself fresh. For

**7:13** · anything that changes more than once a

**7:15** · month, live inventory, today's prices,

**7:18** · keep it behind an API, not a document.

**7:21** · OKF is for stable expertise, the

**7:23** · definitions, the schemas, the hard-won

**7:26** · how it really works that humans used to

**7:27** · carry in their heads.

**7:29** · But the core idea is right and it is

**7:31** · overdue. Stop re-explaining your company

**7:34** · to every new agent. Write the knowledge

**7:36** · down once in a format any of them can

**7:38** · read and manage it like the asset that

**7:40** · it actually is. So, to recap, OKF is a

**7:44** · folder of markdown files. Each file is

**7:47** · one concept with a required type. They

**7:49** · link into a graph and they live in Git.

**7:52** · Write it once and every agent finally

**7:54** · knows your business. If that was useful,

**7:56** · subscribe. We go deep on exactly this

**7:58** · kind of thing every single week. I will

**8:01** · see you in the next one.
