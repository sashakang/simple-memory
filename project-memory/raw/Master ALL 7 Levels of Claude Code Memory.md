---
title: "Master ALL 7 Levels of Claude Code Memory"
source: "https://www.youtube.com/watch?v=OMkdlwZxSt8"
author:
  - "[[Mark Kashef]]"
published: 2026-04-22
created: 2026-06-28
description: "Master Claude Code: https://www.skool.com/earlyaidopters/about  Grab the Memory Architect Kit (FREE): https://markkashef.gumroad.com/l/claude-memory-architect-kit  ---  There are 3..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=OMkdlwZxSt8)

Master Claude Code: https://www.skool.com/earlyaidopters/about

Grab the Memory Architect Kit (FREE): https://markkashef.gumroad.com/l/claude-memory-architect-kit

---

There are 35+ open source memory systems for Claude Code. Every one of them says "this is the best approach." But memory is like a fingerprint. No two should look the same.

In this video, I walk you through how to plan, design, and build your own memory system that's tailored to how you work. I show you the technique of cloning repos, auditing them with Claude Code, and cherry-picking the patterns that fit. Then I hand you a skill that interviews you, teaches you the memory building blocks, and builds the whole thing for you.

Whether you're technical or not, this will change how you think about memory.

---

0:00 - This is Your Brain
0:58 - The Problem with Memory
1:52 - Memory is a Fingerprint
2:43 - Memory is an Infinite Game
3:05 - The 3-Step Technique
3:43 - Demo: Clone & Audit Repos
5:01 - Comparing the Frameworks
6:10 - Extracting What Matters
7:25 - Your Lightweight Memory Spec
8:15 - The Memory Building Blocks
9:28 - Decay & Promotion
9:55 - Multi-Signal Retrieval
10:29 - The Memory Architect Skill
10:45 - Salience, Disclosure & Compaction
11:50 - Skill Demo: /memory-architect
13:17 - Memory Stack Education
14:40 - Your Memory Recipe
14:56 - How to Inject Memory
15:52 - Approach 1: CLAUDE.md
16:08 - Approach 2: Hooks
16:33 - Approach 3: Agent-Scoped
18:16 - Build Complete
18:43 - Wiring Hooks
19:31 - The Payoff: "Who Am I?"
19:55 - Closing

---

Book a Consultation: https://calendly.com/d/crfp-qz3-m4z

#claudecode #memory #obsidian #claudecodememory #memorypalace #claudecodeskills #aimemory #claudecodeai #secondbrain #aiproductivity #claudecodetutorial #memoryarchitect #agenticmemory #claudecodeobsidian

## Transcript

_Caption track: English auto-generated or provided._

**0:00** · So, this is your brain. Well, not

**0:02** · exactly your brain, but some version of

**0:04** · it. In reality, your brain and my brain

**0:07** · are very similar, but they're not the

**0:08** · same. They're wired differently. [music]

**0:10** · They shoot signals at different times

**0:12** · for different reasons. And when it comes

**0:14** · to memory, even that isn't exactly the

**0:17** · same, which is why when it comes to

**0:18** · Claude Code, even though there are tons

**0:21** · of open repositories claiming to be

**0:23** · [music] the king of memory, there will

**0:25** · be no perfect fit for everybody. The

**0:28** · perfect memory system that's tailored to

**0:30** · what you do day in and day out doesn't

**0:32** · exist off the shelf. But, this is

**0:34** · something that with the right strategy,

**0:36** · you could build yourself. So, the goal

**0:38** · of this video isn't to show you some

**0:39** · shiny new framework that will apply to

**0:41** · everybody. Instead, I'm going to show

**0:43** · you how you can plan, design, and build

**0:45** · the perfect memory system that is

**0:47** · tailored to your day-to-day workflows.

**0:49** · [music] And even if you're

**0:50** · non-technical, as long as you have a

**0:52** · Claude Code account and an open mind,

**0:54** · you can do this, too. If I piqued your

**0:56** · interest, then let's get into it. So,

**0:57** · this here is the crux of the problem.

**1:00** · You have a variety, you have a surplus

**1:02** · of different ways to implement memory in

**1:04** · Claude Code because out of the box,

**1:06** · Claude Code does have memory, it can

**1:08** · even dream. But, even when it comes to

**1:10** · transactional stuff, it's not the best.

**1:13** · And as you'd expect, the Claude Code

**1:14** · team builds for the masses, they don't

**1:17** · build for you. So, if you want something

**1:18** · perfectly sculpted to your

**1:20** · specifications, then we can build it and

**1:22** · layer it on top of the existing memory.

**1:25** · So, instead of trying to replace the

**1:26** · Claude Code memory, which naturally will

**1:28** · get better over time, we are always

**1:30** · trying to complement it in a way that

**1:32** · your framework doesn't become obsolete.

**1:35** · And instead of getting tribal and

**1:36** · saying, "I am team Mem Palace." or "I am

**1:38** · team Claud Mem." or "I'm even team Claud

**1:42** · Sidian." the intersection of Claude Code

**1:45** · and Obsidian, you can have it all. And

**1:48** · really, when it comes down to it, you

**1:49** · might not need 90% of what is in these

**1:52** · repos. Now, some of these use vector

**1:54** · databases, others use graphs, and others

**1:57** · just use markdown files. And again, it's

**1:59** · about what modalities make sense for

**2:01** · you. And I've already alluded to the

**2:03** · fact that memory is like a fingerprint.

**2:05** · No two memory systems look exactly the

**2:08** · same. So, if we take someone that runs a

**2:10** · high-volume e-comm business, what

**2:13** · they're worried about are seasonal

**2:14** · patterns, consumer demand, the

**2:16** · performance of things like meta ads. And

**2:19** · when it comes to someone else, like a

**2:20** · wealth manager, they'll be concerned

**2:22** · with very different things, very deep

**2:24** · relationships that are much fewer in

**2:26** · quantity, but much deeper in value. And

**2:29** · a lawyer would be concerned with a whole

**2:31** · different set of things, like precedent

**2:32** · recall, case history, examples of things

**2:35** · that have worked and have not worked for

**2:37** · their clients before. So, the question

**2:39** · isn't what repo should I adopt, it

**2:42** · should be, "What does my memory system

**2:44** · need to look like?" And I find a lot of

**2:46** · misleading advice on YouTube telling you

**2:48** · that once you figure out this one memory

**2:50** · system, it will unlock superpowers

**2:52** · forever. In reality, memory is an

**2:55** · infinite game, it's not a finite one.

**2:57** · So, the moment you finish it, the job is

**3:00** · to maintain and iterate on it as you

**3:02** · evolve, your business evolves, and your

**3:04** · day-to-day evolves as well. This is why

**3:06** · I'm going to go through the very simple

**3:07** · process that only takes three steps to

**3:09** · get started. And these steps are to

**3:11** · clone existing GitHub repositories, then

**3:14** · feed them to Claude Code to audit them,

**3:17** · compare them, contrast them in full, and

**3:19** · once you really convey what your use

**3:21** · cases are and what your memory palace

**3:23** · should look like, then Claude Code can

**3:26** · extract all the design patterns, all the

**3:28** · code necessary to start building your

**3:30** · memory system. And then it really comes

**3:32** · down to, how do you inject this memory

**3:34** · into your day-to-day Claude use? So,

**3:36** · let's take this technique for a spin.

**3:38** · All we need are these three existing

**3:40** · repos right here. Theoretically, you

**3:42** · could add five, 10, 15 all at once. And

**3:45** · all we're going to do is, we're going to

**3:46** · take each GitHub repository URL, give it

**3:49** · to Claude Code, and say, "Do a full deep

**3:52** · dive and do a compare and contrast on

**3:55** · all of these repos." So, I've added all

**3:57** · three links right here, and I've asked

**3:59** · Claude Code to clone the following

**4:01** · repositories. And all we have to do is

**4:03** · add one additional line.

**4:05** · Spin up a series of explore sub-agents

**4:08** · to go through each and every one of

**4:10** · these repos, pull out all the design

**4:12** · patterns, all the interesting code, and

**4:14** · anything that you find consequential or

**4:16** · novel about managing memory with agentic

**4:18** · tools.

**4:20** · So, it could be more than one line,

**4:21** · maybe a couple lines if you zoom in. And

**4:23** · then we send that over, and now what it

**4:25** · will do is, it will not only clone using

**4:28** · bash each one of these repositories, and

**4:30** · then it will populate, as you see here,

**4:32** · immediately, each folder with the

**4:34** · associated code. And once that's ready

**4:36** · to go, it will then spin up its

**4:38** · sub-agents to take a very close look as

**4:41** · to what's happening underneath the hood.

**4:43** · And moments later, we have three

**4:44** · background agents that are launched.

**4:46** · They'll take anywhere between 1 to 5 to

**4:48** · 10 minutes to do a full deep dive

**4:50** · exploration, and the best part is,

**4:53** · because these are sub-agents, all of

**4:54** · this context, all this exploration will

**4:57** · happen elsewhere, and all we'll have in

**4:59** · our context window are the core results.

**5:01** · In 5 minutes into the future, we have

**5:03** · all the agents return with full

**5:05** · completion, and we have a report below

**5:08** · that compares and contrasts each one of

**5:10** · these frameworks. So, if we scroll down,

**5:11** · you can see right away, between Mem

**5:13** · Palace, Claud Sidian, and Mem Zero, Mem

**5:16** · Zero is very vector database-based.

**5:19** · Claud Sidian is just purely markdown

**5:21** · files, while Mem Palace is also a

**5:24** · version of vector database memory, but

**5:26** · it's using a very light database called

**5:28** · Chroma DB. And naturally, as you scroll

**5:30** · down, there will be infinitely

**5:32** · detail that I won't run you through

**5:34** · since you can do this on your own, but

**5:36** · the whole point is that you can get the

**5:37** · full lay of the land for each one of

**5:39** · these frameworks. But then, what do we

**5:41** · do next? And by the way, if you enjoy

**5:43** · the way I walk through these concepts on

**5:45** · YouTube and it leaves you craving more

**5:47** · and more depth, then you want to make

**5:49** · sure you check out my Claude Code Magic

**5:51** · Course. That's a living course, meaning

**5:53** · as things get deprecated or as things

**5:55** · get obsolete, I keep replacing them and

**5:58** · adding more exclusive content. You'll be

**6:00** · able to find this and all of my other

**6:01** · courses, including my personal assistant

**6:04** · Claude Code system, in my early

**6:06** · adopter's [music] community. So, if that

**6:07** · interests you, check out the first link

**6:09** · in the description below. All right,

**6:10** · back to the video. Now that we know

**6:12** · exactly what these frameworks are and

**6:14** · how they work, the next step is deciding

**6:16** · what matters and extracting that. So,

**6:19** · this is the part where you jump in and

**6:21** · you add some context. So, in Claude

**6:23** · Code, I'm going to use a very mini

**6:24** · version of this, but ideally, you should

**6:26** · vent between 3, 5, 10 minutes all of the

**6:30** · context of your day-to-day, all of the

**6:32** · things that you wish could be remembered

**6:33** · and how you'd like them to be

**6:34** · remembered. So, I can say something like

**6:36** · this.

**6:37** · Okay, so I want to design this memory

**6:39** · that ideally runs very light on my

**6:41** · computer. It could be something like a

**6:43** · SQL Lite. But, the main thing is, I want

**6:45** · to have some memories that fade over

**6:47** · time, some that persist, and I want to

**6:49** · be able to always look up a memory using

**6:51** · semantics. But, I don't want it to be

**6:53** · too in-depth. I don't need a nuclear

**6:56** · bomb for a fist fight. So, can you come

**6:57** · up with the most simple and elegant

**7:00** · series of memory frameworks or memory

**7:03** · paradigms that you can derive from all

**7:05** · of these repos that you explored? Now, a

**7:08** · little bit verbose, you could say this

**7:09** · in any permutation you want, but the

**7:11** · TLDR is, can you explore everything you

**7:14** · just analyzed and apply it to my

**7:16** · scenario?

**7:17** · So, once we send this off, Claude will

**7:18** · think through, "What is the path of

**7:20** · least resistance to create our own

**7:22** · derivative memory system?" And then we

**7:24** · get back a very simplistic plan, and

**7:27** · it's labeled a lightweight memory spec,

**7:29** · and it says pulling only what fits a

**7:31** · laptop and a fist fight. It walks you

**7:33** · through the stack and it says you

**7:35** · probably only need some form of small,

**7:37** · local embedding framework for the vector

**7:38** · database. It walks through what the

**7:40** · memory table would look like, the core

**7:42** · paradigms, maybe a two-tier memory

**7:45** · system with some form of decay of some

**7:47** · memories. And then as you go down, it

**7:50** · walks through how it's going to add

**7:51** · memories over time and clean them up,

**7:54** · and then some form of synthesis roll-up.

**7:56** · And then you can go back and forth until

**7:57** · it sounds like something that would make

**7:59** · sense for you. The best part of this is,

**8:01** · if you build V0, V1, V2, and you're

**8:04** · still unhappy, you can always go and

**8:06** · explore other repos, bring them into

**8:08** · context, see what's missing until you

**8:10** · get to the perfect formula for you. Now,

**8:12** · what if you don't even know what to ask

**8:14** · Claude Code because this whole memory

**8:16** · concept is newer to you? There are a

**8:18** · series of building blocks that you can

**8:20** · combine together that make up a good

**8:22** · memory system. The first building block

**8:24** · is identity, and this is everything from

**8:26** · what your name is to your occupation, to

**8:28** · your age, to anything that should

**8:30** · persist over time no matter what. So,

**8:32** · these memories remain forever unless you

**8:34** · change them yourself. And then we have

**8:36** · critical context, which is somewhat

**8:38** · associated to identity. If you are now

**8:40** · running a business, if you work in a

**8:41** · company, anything that is contextually

**8:44** · important to that position or that point

**8:46** · in life should be part of the context

**8:49** · here. And then you have on-demand

**8:51** · working memory. And this is likely

**8:53** · something you're working on right now

**8:55** · that might not actually be worth

**8:56** · persisting in the future. So, you can

**8:58** · think of this as a messy desk of

**9:00** · thoughts. And these thoughts might be

**9:02** · all for this work-in-progress task, but

**9:04** · once it's done, they might not matter.

**9:06** · And then we have long-term and episodic

**9:09** · memory. Episodic memory focuses on the

**9:11** · why. So, not just the what of the

**9:13** · memory, but why did you care to store

**9:16** · this memory? And then the long-term

**9:17** · knowledge are things that are not

**9:19** · foundational to you as a person or to

**9:21** · your day-to-day, but something that's

**9:23** · worth persisting over time. Maybe the

**9:25** · outcome of a litigation, a big event,

**9:28** · something that deserves to be looked

**9:29** · back on at a future point. And then we

**9:31** · have things that happen in the

**9:32** · background. One of them is called decay,

**9:35** · where over time, you can choose for

**9:37** · memories to degrade in importance,

**9:40** · especially if it's very temporal in

**9:41** · nature. And the inverse of that are

**9:43** · promotions, and these are not promotions

**9:45** · at work, but more so promoting memories

**9:47** · in importance that eventually become

**9:49** · persistent because you keep calling on

**9:51** · those memories over and over again. And

**9:53** · the best part about memory systems is

**9:55** · that you can always mix and match. So,

**9:57** · if you want some level of semantic

**9:59** · meaning look up, you can integrate that

**10:01** · to also go along with keyword matching

**10:03** · and then with entity. So, in one

**10:05** · sentence, you can have three different

**10:07** · layers of memory do the work to try to

**10:09** · connect the dots and really understand

**10:11** · what it is that matters to you. So,

**10:13** · instead of brute forcing 25,000 tokens

**10:16** · for a single memory look up, you could

**10:19** · break it down by as much as five to six

**10:21** · times to something like 7,000 tokens,

**10:23** · but using these different signal

**10:25** · mechanisms as ways to pre-filter your

**10:27** · memory data. Now, I'm going to show you

**10:30** · and give you a memory architect skill to

**10:32** · help you through the process of coming

**10:34** · up with your best blueprint for your

**10:36** · memory system. But, before we get to

**10:38** · that, a couple key concepts that we

**10:40** · haven't gone over are ones called

**10:42** · salience and another one called

**10:44** · compaction survival and one more called

**10:46** · progressive disclosure. Very fancy

**10:48** · words, but very simple meanings.

**10:50** · Salience is basically a proxy for

**10:53** · memories that are revisited very often

**10:55** · versus others that are pretty much never

**10:57** · visited after the first time. So, you

**10:59** · can think of this as a very oftenly

**11:01** · crossed path versus one that is

**11:03** · overgrown with tons of shrubs, weeds, et

**11:06** · cetera. If we go back to that initial

**11:08** · building block image, progressive

**11:10** · disclosure is about loading the most

**11:12** · important things first. So, the number

**11:13** · one thing that will be loaded is your

**11:15** · identity, then some form of knowledge,

**11:17** · and then rarely accessed is your full

**11:19** · history. Typically, you're looking for 1

**11:22** · to 2% of your entire history, especially

**11:24** · as you log more over time. And

**11:27** · compaction survival is something that

**11:28** · 90% of people don't know about, where if

**11:31** · you choose to compact in Claude Code,

**11:33** · you can actually auto inject memories in

**11:36** · that compacted version of the session to

**11:38** · make sure it still knows the most

**11:40** · important things moving forward. And

**11:42** · yes, I'll show you a sneak peek on how

**11:43** · you could do this. But first, let me

**11:45** · show you this amazing skill that I've

**11:47** · put together for you. It's meant to

**11:49** · interview you on who you are, your

**11:52** · recipe, and then come up with the

**11:54** · ingredients for the perfect meal so you

**11:56** · can actually build your memory system

**11:58** · and ideally actually implement it. But

**12:00** · before we get to that, I'm going to walk

**12:02** · you through this skill that's fully

**12:03** · designed to interview you on what you

**12:06** · want your memory system to look like,

**12:07** · and then its job is to come up with all

**12:09** · the parameters and all the ingredients,

**12:11** · and I actually trained it on all of the

**12:13** · repos that I could find. So, you can go

**12:15** · from ideating about memory to actually

**12:17** · building the framework, and near the end

**12:19** · of this video, I'll show you how to

**12:21** · inject it. So, if we clear our last

**12:23** · session, let's write memory architect

**12:26** · right here. And this will walk through

**12:28** · the process of the interview. So, upon

**12:30** · starting, you have a fork in the road.

**12:32** · Do you want to go through the full

**12:33** · walk-through, which will teach you how

**12:35** · memory works as well as actually guide

**12:37** · you through it step by step, or do you

**12:38** · want the fast track? Basically, you know

**12:41** · what you want and you just want it to

**12:42** · implement it for you. If we pick full

**12:44** · walk-through, it'll come up with some

**12:46** · more multiple-choice questions that I'm

**12:48** · provoking using the ask user input tool.

**12:51** · So, in this case, it asks you what best

**12:53** · describes your role. And you can always

**12:54** · type something different if it applies

**12:56** · to you, but in my case, I will just say

**12:58** · content creator, knowledge worker. And

**13:00** · then it will ask you how technical are

**13:02** · you with infrastructure. If you say

**13:04** · something like config light or CLI

**13:06** · comfortable, it'll give it an idea.

**13:08** · You'll submit those, and then it will

**13:10** · ask you for more information. And not

**13:12** · only does it interrogate you, but it

**13:14** · educates you. So, it walks you through

**13:16** · what the layers of a memory stack look

**13:18** · like so you can actually understand

**13:19** · what's happening. And then you can go to

**13:21** · the next set of questions. Which memory

**13:23** · layers do you want in your system? And

**13:25** · this is meant to be a multi-select. So,

**13:27** · I can click identity, critical context,

**13:30** · long-term knowledge, hit next, and then

**13:33** · it asks you, do you want any of these

**13:34** · advanced layers? And it then defines

**13:36** · each one of them. In this case, let's

**13:37** · say I say none of these. And I do

**13:39** · submit. And then I do submit again. It

**13:42** · will keep going until it realizes, okay,

**13:44** · do we have enough to build Mark's

**13:46** · perfect memory system? So, it walks

**13:48** · through the next set of layers that we

**13:50** · selected. And then some hypotheticals on

**13:52** · how it would look like. And then we have

**13:54** · a few more questions. So, we'll go

**13:56** · through and let's keep going, and I'm

**13:57** · going to jump to the penultimate step.

**13:59** · So, given that I use Obsidian in my

**14:01** · day-to-day, I have biased this skill to

**14:04** · basically walk you through what an

**14:05** · Obsidian plus Claude Code system would

**14:07** · look like. So, once you go through more

**14:09** · questions, it drafts what a possible

**14:11** · back-end could look like. So, in this

**14:12** · case, telling you you could use Obsidian

**14:15** · with the Claude Code CLI for Obsidian,

**14:17** · and it should walk you through, do you

**14:19** · want to use a plain markdown folder in

**14:21** · general and not use Obsidian at all, or

**14:23** · do you want to use Obsidian? In this

**14:25** · case, I will just write Obsidian. And

**14:27** · then if you don't have the command line

**14:29** · interface, it will tell you to go and

**14:31** · actually install it and use it. So,

**14:33** · after some more interrogation, it goes

**14:34** · through your final recipe. So, this is

**14:37** · your proposed memory architecture,

**14:39** · exactly how it searches, how it deals

**14:41** · with working memory, all the components,

**14:43** · all the layers, everything that we had

**14:46** · in the back and forth. And then finally

**14:47** · tells you, where should the memory live?

**14:50** · So, you can say in this folder, in the

**14:52** · dot memory folder, in an existing

**14:53** · Obsidian folder, and anywhere from

**14:55** · there. So, while this builds out our

**14:57** · entire memory system, how are we going

**14:59** · to inject this into our Claude Code

**15:01** · tactically? Now, there's many ways to

**15:03** · implement this elegantly. One simple

**15:06** · workflow is imagine you start up your

**15:08** · Claude Code, your session starts, and

**15:10** · when that session starts, you can fire

**15:12** · off what's called a hook. That hook will

**15:14** · inject memory, or you can write in your

**15:17** · Claude MD to refer to a certain place in

**15:19** · your repo. And then as you work, not

**15:21** · only do you have Claude Code have its

**15:23** · own memory, but now you can have this

**15:25** · additional layer that's always injecting

**15:27** · the parts that matter. And if you choose

**15:29** · to compact, then you can always auto

**15:31** · inject more memories or existing

**15:33** · memories to make sure that if Claude

**15:35** · Code has done a TLDR of a very

**15:37** · long-running session, that that TLDR

**15:39** · actually injects the parts that matter.

**15:41** · Now, without being fuzzy about this, how

**15:43** · can we accomplish this? So, one way is

**15:46** · in your Claude MD, you can actually say

**15:48** · when you start a session, read this

**15:50** · vault file. So, vault would be for an

**15:52** · Obsidian database. Then you have this

**15:54** · markdown file, and you're telling it to

**15:56** · read it at session start. Now, the thing

**15:58** · with Claude MD is it's always auto

**16:00** · injected at the very beginning of a

**16:02** · session, but it's not deterministic,

**16:04** · meaning maybe nine times out of 10,

**16:07** · Claude Code will read it and it will

**16:08** · read anything associated to it in that

**16:10** · file, but there is always a chance that

**16:12** · it doesn't. Which is where we come to

**16:14** · row two. If you use a hook, you can

**16:17** · actually [clears throat]

**16:17** · deterministically fire a hook at session

**16:20** · start to make it read this identity

**16:22** · file. And you can do the same thing with

**16:24** · compaction, where before the pre-compact

**16:27** · event using hooks, you can also inject

**16:29** · another thing. So, you can call this

**16:30** · underscore context MD. One little Easter

**16:33** · egg here is theoretically, you could

**16:35** · maintain a markdown file of what you

**16:38** · deem to be the most important parts of

**16:39** · your session, so when you compact, you

**16:42** · can auto inject that context that

**16:44** · matters. And this comes in really handy

**16:46** · if you have something like an open claw,

**16:48** · a Hermes agent, or something like me,

**16:50** · like a Claude Code system that uses

**16:52** · Claude Code as the base. If you don't

**16:54** · know what I'm talking about, I have a

**16:55** · whole video on this and I'll link it

**16:57** · above. So, with your agent team, each

**16:59** · one can have its separate vault folder

**17:02** · that it always auto injects. So, for me,

**17:04** · day-to-day, when it comes to

**17:06** · communication, so these are things like

**17:07** · emails, WhatsApp, Slack, anything that I

**17:10** · want to answer on the go, my comms agent

**17:13** · will always auto inject all of my notes

**17:15** · about communications, maybe not just

**17:17** · style, but certain events that are

**17:19** · happening. So, when we start a session,

**17:21** · we have the Claude MD, but we also have

**17:23** · an auto injection of these core

**17:24** · memories. So, approach one is purely

**17:27** · text. All you have to do is just say

**17:29** · read the following, and when you

**17:31** · intentionally say things like read,

**17:33** · these are magic words because Claude

**17:35** · Code uses tools like read, write, edit,

**17:37** · glob, grep, and a series of others. So,

**17:40** · when you say the specific command word,

**17:42** · it is much more likely to actually do

**17:44** · it. For approach two, if you're a

**17:45** · beginner, you might be fearful of

**17:47** · setting up hooks. Luckily, you can tag

**17:49** · something called the Claude Code Guide

**17:52** · and ask it to create a hook at the

**17:54** · session start or before a tool call that

**17:56** · auto injects a specific memory file. And

**17:59** · for number three, assuming you're using

**18:00** · something like Obsidian, as long as you

**18:03** · have the command line interface set up,

**18:05** · you can always go back and forth with

**18:06** · Claude Code to negotiate for a certain

**18:08** · project, for a certain agent, when a

**18:11** · vault or a series of vault memories

**18:13** · should be injected. And if we go back to

**18:15** · our memory system, it is almost ready to

**18:17** · go. So, all the files are created. This

**18:19** · is what it looks like. It's in this

**18:21** · folder called memory within this

**18:22** · project. We have the Claude MD file with

**18:25** · some memory instructions. We have the

**18:27** · prime auto injected memory that we're

**18:29** · going to put, the identity file of who I

**18:31** · am, the context, some scripts. If you

**18:34** · scroll through, it walks you through

**18:35** · exactly how it works, and it says, I

**18:38** · need you to configure Claude Code hooks

**18:41** · for a custom memory system.

**18:43** · What we can do is, if we don't know

**18:44** · exactly how to do this ourselves, we can

**18:47** · tag our buddy and do @ClaudeCodeGuide,

**18:52** · and we'll say, can you take care of

**18:54** · setting up all the hooks for us based on

**18:56** · the top specifications and the latest

**18:58** · documentation that you find on

**19:00** · effectively and efficiently implementing

**19:02** · them?

**19:03** · And then when we send this off, this

**19:05** · basically spins up a sub-agent to go and

**19:07** · look at documentation and come back to

**19:09** · us with the result. And after some

**19:11** · research, it is creating all the hooks

**19:13** · right in front of you right here. You

**19:15** · can already take a peek at hooks at

**19:17** · session start, what it should look like,

**19:19** · the fact that it will auto inject this

**19:21** · specific priming memory file. And all

**19:24** · you have to do is just do allow, it will

**19:26** · continue, and the goal is, not in this

**19:28** · current session, in the next one, we

**19:31** · will see an auto injection of all of

**19:33** · these memories. So, it tells us to close

**19:35** · the session and open a fresh new one,

**19:37** · like I said. So, if I ask something

**19:39** · like, who am I and what am I working on,

**19:41** · it will auto inject everything in that

**19:43** · priming file that tells me that I am a

**19:45** · content creator, I am CLI comfortable,

**19:47** · I'm working in Claude Code, and my

**19:49** · current project is the memory recording

**19:51** · from YouTube. So, this is just a glimpse

**19:53** · of how deep you can make a memory system

**19:55** · in a very short amount of time. So, I'm

**19:57** · hoping this entire walk-through breaks

**19:59** · not only limiting beliefs, but also

**20:01** · breaks any anxieties and overwhelm of

**20:03** · having to keep up with the latest and

**20:05** · greatest framework [music] deemed to be

**20:07** · the ultimate version of memory. By

**20:09** · taking all the concepts in this video,

**20:11** · as well as the skill in the second link

**20:14** · in the description below, you'll be able

**20:15** · to start and finish your version of a

**20:17** · memory system that works for you. And

**20:19** · once again, if you want to go much

**20:21** · deeper on memory, if you want to see how

**20:23** · I design memory [music] systems for my

**20:25** · Claude Claw Personal Assistant System,

**20:27** · then you're going to want to hop into

**20:29** · the Early Adopters Community to catch my

**20:31** · Claude Code Magic Course and everything

**20:33** · else I have cooking up. And for the rest

**20:34** · of you, if you found this helpful and

**20:36** · you appreciated the depth, then all I

**20:38** · could ask of you is a like on the video,

**20:40** · a comment if you're feeling friendly,

**20:41** · and a sub if you want to see more.
