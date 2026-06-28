---
title: "Anthropic Quietly Shipped The Memory Layer Your Agent Was Missing. Build It Yourself In A Weekend."
source: "https://www.youtube.com/watch?v=mmBddcUFltU"
author:
  - "[[The AI Automators]]"
published: 2026-05-09
created: 2026-06-28
description: "👉 Access our AI Architects course & join hundreds of serious AI builders in our community: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutoria..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=mmBddcUFltU)

👉 Access our AI Architects course & join hundreds of serious AI builders in our community: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=agent-dreaming

Anthropic just announced a feature in their managed agents called Dreaming, and OpenClaw shipped something very similar last month. So what is actually happening behind the scenes, how do you build it into your own agentic system, and when should you actually use it?

Related video:
https://www.youtube.com/watch?v=YJCe8hvZrxs

In this video, I break down what this dreaming feature is, walk through OpenClaws' transparent implementation, and look at where this pattern fits and where it does not.

What's covered:
- The concept of sleep time compute and why stateful agents benefit from background memory consolidation
- How Anthropic's Dreaming research preview reads existing memory and past sessions to produce a reorganized memory store
- Downsides of managed memory layers, including cost, vendor lock-in, and memory poisoning risks
A walkthrough of OpenClaws memory core.
- When agent dreaming fits (repetitive work, recurring mistakes) and when it does not (varied work, short-lived agents)
- Storage alternatives beyond markdown

Chapters:
0:00 - What is agent dreaming
0:18 - Sleep time compute concept
1:10 - Anthropic's Dreaming feature
2:43 - OpenClaw Dreaming feature
3:32 - Memory file structure
5:16 - When dreaming fits and when it does not
6:39 - Agent memory landscape, alternatives and external platforms

## Transcript

_Caption track: English auto-generated or provided._

**0:00** · Anthropic just announced a new feature

**0:01** · in their managed agents called dreaming

**0:04** · to help their agents self-improve over

**0:06** · time. And last month, Open Claw released

**0:08** · a similar feature with the same name.

**0:10** · So, what exactly is going on behind the

**0:12** · scenes here? And importantly, how do you

**0:14** · build this feature into your own agentic

**0:16** · system? And when should you actually use

**0:18** · it? At a high level, dreaming is a

**0:20** · scheduled background process that runs

**0:22** · between your active sessions. These can

**0:24** · review your agent sessions and memory

**0:26** · stores, extract patterns, and curate

**0:28** · memories so your agents improve over

**0:30** · time. There was a good article published

**0:32** · last year on Leta's website. Leta is a

**0:34** · memory-first coding agent, and they have

**0:36** · been a bit ahead of the curve with some

**0:38** · of these concepts. As they state here,

**0:40** · agents experience prolonged periods of

**0:42** · sleep time. If these agents are

**0:43** · stateful, then sleep time is an

**0:45** · opportunity to apply compute. We have a

**0:47** · simple example here where sleep time

**0:49** · computer is used to consolidate and

**0:51** · curate memories. So, within the original

**0:53** · context of the agent, there might have

**0:55** · been entries related to a particular

**0:56** · topic, and perhaps even conflicting

**0:58** · ones, and scheduled jobs can be used to

**1:01** · create, clean, concise, and detailed

**1:03** · memories, cutting out duplication,

**1:06** · ordering information, and trying to make

**1:07** · sense of what's important and what's

**1:09** · not. Anthropic are applying the same

**1:11** · general concept here. Let Claude reflect

**1:13** · on past sessions to curate an agent's

**1:15** · memory and surface new insights. Claude

**1:17** · writes to memory stores as your

**1:19** · interaction with agents on their managed

**1:21** · agent platform. But naturally, over many

**1:23** · sessions, a memory store accumulates

**1:25** · duplicates, contradictions, and stale

**1:27** · entries. And that's what this dreams

**1:29** · feature is intended to solve. And this

**1:31** · dream process will read an existing

**1:33** · memory store alongside past session

**1:35** · transcripts, then produce a new

**1:37** · reorganized memory store. So, it doesn't

**1:39** · actually modify the original one.

**1:40** · Rather, it creates a separate one, so

**1:42** · you can discard that if you like. But

**1:44** · dreaming is a research preview feature

**1:46** · with pretty limited details on

**1:48** · implementation, and it's part of

**1:49** · Claude's managed agents, which can

**1:51** · certainly have its downsides, namely

**1:53** · cost, vendor lock-in, and not

**1:55** · necessarily as much control as you might

**1:57** · want. And Daniel went through the

**1:59** · landscape of managed platforms in a

**2:00** · recent video on our channel. Also, by

**2:02** · using generalized memory systems, you

**2:05** · run the risk of running into many

**2:06** · different memory anti-patterns. One of

**2:09** · the worst ones being memory poisoning,

**2:11** · where injected instructions survive

**2:13** · across sessions and might execute days

**2:15** · or weeks later. If you want to build the

**2:17** · best memory system for your agent, it's

**2:19** · generally best to be deliberate about

**2:21** · its design. In fact, we have a lesson

**2:23** · dedicated to this specifically within

**2:25** · our AI Architect's course. One of the

**2:27** · biggest downsides of using managed agent

**2:29** · platforms is that generally the memory

**2:31** · will get locked into that platform

**2:33** · specifically, which can make it

**2:34** · difficult to switch to other providers.

**2:36** · But the good news is that you can

**2:37** · absolutely build this type of memory

**2:39** · layer into your own agentic system. So,

**2:41** · the question is, how would you do that?

**2:43** · For a more concrete example of how

**2:45** · dreaming works, how this memory

**2:46** · consolidation layer works, we jump to

**2:48** · OpenClaw because they make the process

**2:50** · extremely transparent. If you clone the

**2:52** · OpenClaw repo, if you go to the memory

**2:54** · core folder, you can see all of the

**2:56** · files related to this dreaming feature.

**2:58** · And you can point your Claude an agent,

**3:00** · be it Claude code or Codex, at these

**3:02** · files and get it to analyze the

**3:04** · implementation and then build a similar

**3:06** · memory system into your own AI system.

**3:09** · So, let's have a look at how OpenClaw

**3:10** · stores memories overall because there

**3:12** · are some useful insights in here.

**3:14** · OpenClaw remembers things by writing

**3:16** · plain markdown files in your agent's

**3:18** · workspace. The model only remembers what

**3:20** · gets saved to disk. And by the way, you

**3:22** · can still analyze and pick from this

**3:24** · architecture and then write and retrieve

**3:26** · from a different form of storage, such

**3:28** · as vector databases or SQL databases or

**3:31** · graph databases, especially if markdown

**3:33** · files don't work particularly well for

**3:35** · your use case. But markdown can actually

**3:38** · scale surprisingly well. Within

**3:39** · OpenClaw, there are three memory-related

**3:41** · files. We have the memory.md. This is

**3:43** · long-term memory, durable facts,

**3:45** · preferences, and decisions, and these

**3:47** · are loaded at the start of every DM

**3:48** · session. Then we have daily notes

**3:50** · markdown files, and this is running

**3:52** · context and observations. Today and

**3:54** · yesterday's notes are loaded

**3:55** · automatically. And then we have the

**3:57** · dreams markdown file, which is what

**3:58** · we're interested in here. When dreaming

**4:00** · is enabled on an Open Claw instance, it

**4:02** · stores two kinds of files. The machine

**4:05** · state is stored within this folder, and

**4:07** · then we have human-readable output in

**4:09** · this dreams markdown file. And as the

**4:11** · dreams process is running, it may

**4:13** · promote specific items to the memory.md

**4:16** · file, which is loaded at the start of

**4:18** · every DM session. When Open Claw goes

**4:20** · through a dreaming sweep, it runs them

**4:22** · in phases. So, it goes between light,

**4:24** · REM, and deep. So, it really leans

**4:26** · pretty heavily into this dream idea.

**4:28** · Within the light phase, it sorts and

**4:30** · stages recent short-term material.

**4:32** · Within REM, it reflects on themes and

**4:34** · recurring ideas. And then finally, at

**4:37** · the deep stage, it scores and promotes

**4:39** · the durable candidates, and then writes

**4:41** · those to the memory.md file, if

**4:43** · necessary. And those most important

**4:45** · memories will get loaded into the

**4:47** · context of every session with Open Claw.

**4:50** · This deep phase may update the memory.md

**4:52** · file, as well as add information to the

**4:54** · dreams.md file. Deep ranking signals are

**4:57** · used to determine what's actually worth

**4:59** · saving. So, for example, we have

**5:00** · frequency, how many short-term signals

**5:02** · the entry accumulated, and relevance,

**5:05** · average retrieval quantity for the

**5:06** · entry. And as this REM phase of the

**5:09** · sleep cycle is run, it records REM

**5:11** · reinforcement signals used by this deep

**5:14** · ranking feature. Before we go any

**5:16** · further, let's take a step back and

**5:17** · determine where does this actual dream

**5:20** · dreaming memory consolidation feature

**5:22** · fit into your process and where it does

**5:24** · not. One good example is where your

**5:26** · agent has the same shape of work over

**5:28** · and over again. So, legal drafting or

**5:31** · support ticket triage or where your

**5:33** · agent is making the same mistakes and

**5:35** · missing the same context over and over

**5:37** · again. That repetition is really good

**5:39** · raw material as a consolidation pass in

**5:43** · a memory dream feature. Also, when your

**5:45** · agent spends the first 20 minutes of

**5:47** · every run rediscovering what it needs to

**5:50** · do or what conventions to follow, and if

**5:52** · skills have not been created for those

**5:54** · particular tasks, and if you want that

**5:56** · information to be picked up slowly and

**5:58** · continuously by the agent, then again,

**6:00** · this is a good use case. And you can

**6:02** · also have pretty sophisticated versions

**6:03** · of these memory consolidation systems

**6:06** · working across multiple users, which can

**6:08** · be very useful, but also bring in its

**6:10** · own challenges. This kind of feature

**6:12** · doesn't fit so well if you have widely

**6:14** · varied work and if you have one-off or

**6:16** · short-lived agents. And also, if you

**6:19** · need to know exactly what your agent

**6:20** · knows without having to go through the

**6:23** · process of examining all of the memory

**6:25** · consolidation, which can sometimes take

**6:27** · up more time than it saves, then it

**6:30** · might not fit the process. Also, memory

**6:32** · can bloat and contradict itself and bake

**6:35** · in the wrong lessons, and that could be

**6:37** · one of the many failure modes that I

**6:38** · showed earlier. Memory is a very deep

**6:40** · concept in AI engineering, and it takes

**6:42** · so many different shapes and so many

**6:43** · different forms, and the landscape is

**6:45** · huge. Markdown files in a file system

**6:48** · can go a lot further than most people

**6:49** · realize, but there are a lot of other

**6:51** · options. You can store data in a

**6:53** · standard relational database, or you can

**6:55** · use external platforms and services like

**6:57** · M0, which uses hybrid vector and a graph

**7:00** · memory layer, or you can use services

**7:02** · like Zap. We've included Zap in some

**7:04** · previous systems that we demonstrated on

**7:06** · this channel, and that uses this

**7:08** · Graffiti library under the hood, which

**7:09** · you can also use separately. When you

**7:11** · look at Hermes, a popular open claw

**7:13** · alternative, this has its own

**7:15** · persistence memory layer out of the box,

**7:17** · which you can also dig into within their

**7:19** · GitHub repo. This system can also easily

**7:21** · integrate out of the box with external

**7:23** · memory providers such as Honcho or M0

**7:26** · that I talked about a minute ago.

**7:27** · There's a steady move in the AI industry

**7:29** · to build systems so that agents can

**7:32** · actually improve over time. And what

**7:34** · Anthropic have shipped here essentially

**7:35** · seems to be a managed harness wrapper

**7:37** · around a pattern that the open source

**7:39** · ecosystem has been settling on for quite

**7:41** · a while. And these patterns have been

**7:43** · pushed in order to try to overcome all

**7:45** · of the familiar problems that we're used

**7:47** · to dealing with, such as when you have

**7:48** · to say the same thing to agents over and

**7:50** · over again, and when they forget

**7:52** · important information over time. But

**7:54** · there's still quite a long way to go,

**7:55** · and memory systems in general can

**7:57** · introduce more problems than they intend

**7:59** · to solve. If a bad memory gets baked in,

**8:01** · the agent can be confidently wrong over

**8:03** · the long term, and stale information can

**8:06** · get treated as current. Memory

**8:07** · consolidation can be extremely useful,

**8:10** · and it does not need to be isolated just

**8:12** · to markdown files. But it's only part of

**8:14** · the answer, and a generalized dream

**8:16** · layer very rarely beats one that's

**8:18** · designed for a specific agent for your

**8:21** · specific domain. And if you want to go

**8:23** · deep into learning how to build

**8:24** · expert-level specialized AI systems,

**8:27** · then make sure to check out the link in

**8:28** · the description below to the AI

**8:30** · Architects course in our community. We

**8:32** · currently have over 15 hours of footage,

**8:35** · and new lessons are getting added

**8:36** · regularly. Thanks for watching.
