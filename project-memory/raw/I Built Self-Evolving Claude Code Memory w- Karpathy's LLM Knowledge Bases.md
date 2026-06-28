---
title: "I Built Self-Evolving Claude Code Memory w/ Karpathy's LLM Knowledge Bases"
source: "https://www.youtube.com/watch?v=7huCP6RkcY4"
author:
  - "[[Cole Medin]]"
published: 2026-04-06
created: 2026-06-28
description: "Andrej Karpathy posted about using LLMs to build personal knowledge bases - raw articles go in, an LLM compiles them into an interconnected wiki, and health checks keep everything ..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=7huCP6RkcY4)

Andrej Karpathy posted about using LLMs to build personal knowledge bases - raw articles go in, an LLM compiles them into an interconnected wiki, and health checks keep everything consistent. It went massively viral. 

But here's the thing: the most valuable raw data isn't external articles. It's your own conversations with your agents.

Every time you work with Claude Code, you make decisions, discover gotchas, learn patterns, and build up context that vanishes when the session ends or the context window compacts. What if instead of losing all of that, every conversation automatically compiled into a structured knowledge base that gets smarter over time? 

That's what I built and in this video I'll show you how to use it!

~~~~~~~~~~~~~~~~~~~~~~~~~~

- Try InsForge - the open source platform that gives your coding agent a database, auth, storage, AI model routing, and hosting all in one. Free to get started, use code InsForgePromo for a free month of Pro:
https://insforge.dev/

~~~~~~~~~~~~~~~~~~~~~~~~~~

- If you're interested in building your own AI second brain to save yourself hours every week, check out the Dynamous community and the new 4 hour second brain bootcamp: 
https://dynamous.ai/second-brain-bootcamp

- Karpathy inspired Claude Code memory system repo:
https://github.com/coleam00/claude-memory-compiler

- Karpathy's original Tweet:
https://x.com/karpathy/thread/2039805659525644595

- Gist to build your own Karpathy LLM knowledge base:
https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

~~~~~~~~~~~~~~~~~~~~~~~~~~

0:00 Karpathy LLM Knowledge Bases
2:32 How it Works
6:01 Data Flow and Architecture
8:40 My Claude Code Memory System
9:19 InsForge
10:43 Setting Up the System
11:04 Obsidian Setup and Vault Configuration
12:16 Claude Code Hooks
16:51 The Compounding Knowledge Loop
18:35 Outro

~~~~~~~~~~~~~~~~~~~~~~~~~~

Join me as I push the limits of what is possible with AI. I'll be uploading videos weekly - at least every Wednesday at 7:00 PM CDT!

## Transcript

**0:00** · Let's face it, every week you and I are

**0:01** · playing the game what's the latest and

**0:03** · greatest in the AI space, right? It

**0:05** · changes every single week and right now

**0:08** · everyone is focused on LLM knowledge

**0:10** · bases, which originated from this tweet

**0:12** · from Andrej Karpathy and there are a lot

**0:15** · of really cool ideas here that I want to

**0:17** · get into with you and I built my own

**0:20** · memory system on top of this I think

**0:21** · you're really going to like. It's simple

**0:23** · but super effective. So, more on that in

**0:26** · a bit but let's get into a bit of

**0:27** · context here. So, Karpathy starts by

**0:29** · saying something I'm finding very useful

**0:31** · recently is using LLMs to build personal

**0:33** · knowledge bases for various topics of

**0:36** · research interest. So, taking external

**0:38** · information, bringing it into our own

**0:40** · system and organizing it in the best way

**0:42** · for agents to query. And this is a big

**0:46** · use case for AI second brains right now,

**0:48** · which is something I've been focusing on

**0:49** · a lot recently and I love seeing that

**0:52** · he's using Obsidian as a core part of

**0:54** · his stack. I always call it my canvas

**0:56** · for working with things with my second

**0:58** · brain. So, cool to see that. And he

**1:00** · really gives us his entire playbook

**1:02** · here. It's nice and simple. So, he talks

**1:03** · about how he brings in information, data

**1:06** · ingestion, how he views it, how he

**1:08** · queries it, how he formats it, health

**1:10** · checks that he's built in as well. And

**1:12** · so, I want to cover this entire

**1:13** · architecture here and that'll guide us

**1:15** · into the custom solution that I've built

**1:18** · on top. I'm excited to show you this cuz

**1:20** · here's the thing, this entire thing that

**1:22** · he's presenting is working with external

**1:24** · data, which there are a lot of use cases

**1:27** · for that. But what I've built here is

**1:29** · working with internal data. So, giving

**1:31** · Claude code a memory that evolves with

**1:34** · your code base. So, basing the whole LLM

**1:37** · knowledge base on our conversations with

**1:39** · our coding agent or second brain instead

**1:42** · of bringing in external data. But I've

**1:43** · structured everything in exactly the

**1:45** · same way. All of the optimizations for

**1:47** · how we index and create systems for our

**1:50** · agent to explore the information. It's

**1:53** · really cool. So, let's get into the

**1:54** · infrastructure and then I'll show you

**1:55** · how you can use

**1:57** · to evolve any code base. And yes, Claude

**1:59** · Code does already have a memory system

**2:01** · built in and there are open source

**2:03** · solutions out there already for Claude

**2:05** · Code long-term memory, but I wanted to

**2:06** · build this specifically because I am

**2:09** · following everything Karpathy laid out

**2:11** · here to a T just for internal instead of

**2:13** · external information. It's a lot simpler

**2:16** · than other approaches already out there

**2:18** · and I would argue even more effective.

**2:20** · You'll see what I mean when we get into

**2:21** · it. So, something really interesting

**2:23** · that he says at the top here is he's

**2:24** · spending more of his tokens with his

**2:26** · agents manipulating knowledge like

**2:28** · markdown and Obsidian instead of

**2:30** · manipulating code. But, he works with

**2:33** · knowledge in a very similar way that we

**2:35** · work with code. That brings us to the

**2:37** · compiler analogy. This is the simplest

**2:39** · way to explain everything that he's

**2:41** · built in the system here because the way

**2:43** · that we're handling knowledge is very

**2:45** · similar to how we take source code all

**2:47** · the way into a final application for the

**2:50** · end user to run with a compiler. And so,

**2:53** · let let's take it from the top here. So,

**2:54** · we start with our source code, which for

**2:56** · the case of our LLM personal knowledge

**2:59** · bases, it's our articles, papers,

**3:01** · anything that we are finding online that

**3:04** · we want to bring into our system. So,

**3:06** · I'll go to the Obsidian vault because

**3:07** · this is what Karpathy uses. This is what

**3:09** · I use for my AI second brain. We have

**3:11** · the raw folder here. This is the entry

**3:13** · point into our system where we'll dump

**3:15** · anything, articles, papers, transcripts,

**3:18** · everything just as raw markdown. And

**3:20** · then we'll take that and move it into

**3:22** · the compiler stage. This is where we

**3:24** · have a large language model process all

**3:26** · this raw information. So, creating

**3:28** · summaries, linking documents together,

**3:30** · just generally figuring out how to

**3:32** · structure our knowledge. And for the

**3:34** · system that Karpathy has designed here

**3:36** · for the compiler, we do actually have

**3:38** · scripts. We have code that takes our raw

**3:41** · information and gives it to an LLM to

**3:43** · produce the wiki here. So, that brings

**3:45** · us to the next step. The compiler goes

**3:47** · to the executable. This is what we run

**3:50** · or in the case of our personal knowledge

**3:52** · base, this is what we query. So, he

**3:54** · calls it a wiki. This is where we have

**3:55** · our compiled articles, everything

**3:57** · produced from the large language model,

**3:59** · and we have the backlinks. We are

**4:01** · connecting pieces of knowledge together.

**4:03** · So, going back to Obsidian again, we

**4:06** · have our graph view. This is one of the

**4:07** · coolest parts of Obsidian, where we can

**4:10** · see how our different pieces of

**4:12** · knowledge, our different markdown

**4:13** · documents, are connected together

**4:15** · through backlinks. And this is powerful

**4:17** · because it gives our agent the ability

**4:18** · to traverse through the graph, to search

**4:21** · better, and even connect different

**4:23** · pieces of knowledge together to give us

**4:25** · a more comprehensive answer. So, this is

**4:28** · what we run. This is what we search. But

**4:30** · before we actually get to the final step

**4:32** · with the runtime, we also have a test

**4:34** · suite. To continue with the analogy of

**4:36** · code here, we are performing linting. He

**4:39** · calls it linting over our documents. So,

**4:42** · we're finding gaps where maybe we need

**4:44** · to do more research, any kind of stale

**4:46** · data, things that maybe we have in our

**4:48** · raw folder that aren't actually in our

**4:50** · wiki yet, and we need to take care of

**4:52** · that discrepancy, any kind of broken

**4:54** · links, like if we have one document

**4:56** · linking to another that doesn't exist,

**4:58** · we're going to take care of all of that.

**4:59** · And so, we're even going so far in this

**5:02** · system as to making sure that our data

**5:05** · has integrity. And that's pretty

**5:07** · important. We want to have an accurate

**5:09** · personal knowledge base. And then

**5:10** · finally, we get into the last step here,

**5:12** · where we are running queries, right?

**5:13** · This is the runtime, where we are taking

**5:16** · advantage of our wiki, having our agent

**5:18** · search through it to find information

**5:20** · for what we are currently working on.

**5:22** · And the really interesting thing here is

**5:23** · Karpathy said, "I thought I had to reach

**5:25** · for fancy rag, but the large language

**5:27** · model has been pretty good about auto

**5:29** · maintaining index files." And so, one of

**5:31** · the most important files in this entire

**5:34** · setup, within the wiki, we have the

**5:36** · index. So, this file describes to the

**5:38** · agent, "Here are all of the different

**5:40** · folders and resources that you have

**5:42** · access to." So, it uses this as a

**5:44** · starting point, so we don't even have to

**5:46** · do fancy rag. The agent can just

**5:48** · navigate through all the files that we

**5:50** · have as marked down in our Obsidian

**5:52** · vault. It doesn't have to do any

**5:53** · semantic search. There's no vector

**5:55** · database here. It's nice and simple.

**5:57** · It's one of the beauties of this

**5:59** · strategy that really drew me to build on

**6:01** · top of it. Okay, so let's now go from

**6:03** · the compiler analogy to the exact data

**6:06** · flow. Think this will really take it

**6:07** · home for you. Then we'll get into my

**6:09** · implementation that I built on top. I'll

**6:11** · talk about how it relates to all these

**6:13** · ideas here. So, okay. We start with our

**6:15** · external information. And Karpathy

**6:18** · specifically calls out the Obsidian web

**6:20** · clipper. It's a really neat extension to

**6:23** · Obsidian that allows us to very easily

**6:25** · take anything from the internet and

**6:27** · bring it directly into our vault or in

**6:29** · this case right into our raw folder. The

**6:31** · source of truth, like we talked about

**6:33** · earlier, the unprocessed markdown. Then

**6:35** · we feed that into the large language

**6:37** · model to create our wiki for us. And so,

**6:39** · I've built up a simple example here for

**6:41** · demonstration. My raw folder just has

**6:44** · some different articles on AI topics.

**6:47** · And then within the wiki, this is what

**6:48** · is processed. This is what our agent

**6:50** · actually queries. We have this concepts

**6:53** · folder, and this is where we tie

**6:55** · everything together. We're taking ideas,

**6:57** · concepts out of our raw documents. And

**7:00** · we also have connections, how different

**7:02** · things are relating together. And then

**7:03** · of course we have the index. This is the

**7:05** · main file that we want our agent to

**7:07** · always have access to so that it has a

**7:09** · high-level idea of where it's going to

**7:11** · start looking based on our question. And

**7:13** · then the last thing that we have here is

**7:15** · the agents.md. So, this is like global

**7:17** · rules for your coding agent, right? And

**7:19** · so, really what we do in our global

**7:21** · rules here is we're describing the

**7:24** · entire system for LLM knowledge bases,

**7:27** · so that the agent understands, here's

**7:29** · where my information comes from, here's

**7:31** · the compiled version that I'm going to

**7:33** · search, here is the index and the log

**7:35** · file, right? Like the entire system we

**7:37** · explain to the agent, so it has that

**7:39** · meta reasoning. It understands what it's

**7:42** · been dropped in. When you start a new

**7:44** · session with your second brain or coding

**7:46** · agent, whatever it is. And the best part

**7:48** · is, if you want to build this entire LLM

**7:50** · knowledge base system for yourself, all

**7:53** · you need to do is send this prompt into

**7:55** · your coding agent. It could not be

**7:57** · simpler. So, this came directly from

**7:59** · Karpathy. He had a follow tweet where he

**8:01** · linked to this. This is essentially a

**8:03** · PRD, right? a product requirement

**8:05** · document that outlines everything we

**8:07** · have to build for you to include this

**8:09** · system in your own coding agent or

**8:11** · second brain. And so, you just prompt

**8:13** · this in, no other context, and it's just

**8:16** · going to one-shot the whole thing for

**8:17** · you. And that's what I built into my

**8:20** · version as well. If you look at the

**8:22** · readme here for the quick start, you

**8:23** · don't even have to clone the repo

**8:25** · yourself. You just send this prompt into

**8:27** · your Claude code. Clone it and then set

**8:30** · up everything with the Claude code

**8:31** · hooks, everything that I have to make

**8:34** · this LLM personal knowledge base, but

**8:36** · for internal information in instead of

**8:39** · external. So, inspired by the entire

**8:41** · architecture we just covered here, but

**8:43** · that's the key difference is now this is

**8:45** · giving Claude code a memory that evolves

**8:47** · with your code base. So, instead of

**8:49** · taking things from the internet, we are

**8:50** · going to automatically capture session

**8:53** · logs with hooks. And so, session logs

**8:56** · are kind of like the raw folder where

**8:58** · we're just putting in our conversations,

**9:00** · and then we're going to use the Claude

**9:01** · agent SDK behind the scenes to

**9:03** · automatically extract everything into

**9:06** · structured cross-reference knowledge

**9:08** · articles. So, your coding agent, like

**9:11** · you can do this per code base. It's

**9:12** · going to get smarter and smarter over

**9:14** · time because it remembers the decisions

**9:16** · you've made and how you evolved your

**9:18** · project. The sponsor of today's video is

**9:20** · Inspo Forge. Inspo Forge is an

**9:22** · open-source platform that gives your

**9:24** · coding agent everything it needs to ship

**9:25** · full stack apps. Think if you had

**9:28** · Vercel, Superbase, and Open Router all

**9:30** · in one platform. So, we have a database,

**9:33** · we've got authentication, storage. We

**9:36** · can route to 50 different large language

**9:38** · models. We have hosting as well. It is

**9:41** · everything you need and we give our

**9:42** · agent the ability to manage all of this

**9:44** · through a CLI and an agent skill. And

**9:46** · take a look at this. It literally takes

**9:48** · less than 5 minutes to install the In

**9:50** · Forge CLI and skill on any code base and

**9:52** · then I can go into Claude Code and

**9:53** · prompt it to create an application. So

**9:55** · here I'll have it make both a back end

**9:57** · and a front end and I'm specifically

**9:59** · asking it to use In Forge to create my

**10:02** · database table, set up authentication,

**10:04** · to host it as well. Once it goes through

**10:06** · this entire process here, then we end

**10:10** · with a hosted application. What I'm

**10:11** · showing you right here is a live URL and

**10:14** · I have authentication set up so I can

**10:15** · even demo this here. I created an

**10:17** · account off camera. I'll sign in. We

**10:19** · have access to our database behind the

**10:21** · scenes. So this is not just local

**10:22** · storage, a hosted application, live

**10:24** · database. I can even use an AI model to

**10:26** · recommend a task for me here. So showing

**10:28** · off the AI part of In Forge as well. We

**10:31** · have got everything running and we

**10:32** · didn't have to configure anything

**10:34** · ourselves. In Forge is open source and

**10:36** · free to get started. Plus you can use

**10:38** · promo code In Forge promo for a free

**10:41** · month of pro. I'll have a link in the

**10:42** · description. So seriously, you should

**10:44** · just try this right now. Open up Claude

**10:46** · Code in whatever code base you're

**10:47** · currently working on, your second brain,

**10:49** · open Claude, whatever and just send in

**10:51** · this prompt. It'll immediately level up

**10:53** · the long-term memory for your coding

**10:54** · agent when it's working on that project

**10:56** · specifically. We're building up lessons

**10:59** · and takeaways for this code base. And so

**11:02** · I have the repository cloned locally.

**11:04** · I'm just going to work within it

**11:05** · directly to give you an example here,

**11:07** · but you're going to use this prompt to

**11:09** · bring it into wherever you are already

**11:11** · working. And so you don't have to do

**11:13** · this, but I would recommend starting

**11:15** · with an Obsidian vault. It's our canvas

**11:16** · to view all of the memories in the whole

**11:19** · wiki that we create with Claude Code.

**11:21** · And so you'll open a folder as a vault.

**11:23** · Once you have Obsidian installed, it's

**11:25** · free and super easy to install.

**11:27** · So I'll open here and you just have to

**11:29** · give it a path to where wherever you

**11:31** · have the code base that you've brought

**11:32** · in this system. So, I'll just select

**11:34** · this folder right here. That'll create a

**11:36** · brand new Obsidian vault. I usually like

**11:38** · to make it look nice as well when I

**11:39** · first create a vault. So, I'll go into

**11:41** · the settings in the bottom left. I'll go

**11:43** · to appearance and then manage to select

**11:45** · a theme. They've got a lot of really

**11:47** · awesome ones. Obsidian night is my

**11:48** · favorite. So, I will click install and

**11:50** · use. And then I usually like to switch

**11:52** · to the dark theme as well. There we go.

**11:54** · Now it looks like the other vault I

**11:56** · showed you earlier for a demo. And so,

**11:58** · this is where we're going to manage the

**12:01** · daily logs. I'll talk about this in a

**12:02** · second. And then also this is our wiki

**12:05** · equivalent where we have our index. I

**12:07** · mean, everything this is exactly what

**12:09** · Karpathy has set up with the concepts

**12:11** · and connections. Everything that we use

**12:13** · a large language model to process from

**12:15** · our raw input. So, this entire system is

**12:18** · only driven by Claude code hooks. So,

**12:20** · that's the beautifully simple part about

**12:22** · it. That's why all you have to do is

**12:24** · send in this prompt to get everything

**12:26** · set up for your code base where you run

**12:28** · Claude code. We don't have to install

**12:30** · anything else. We don't have to set up

**12:32** · any integrations. And so, going to our

**12:34** · settings.json, this is where you always

**12:36** · define your hooks for Claude code. I

**12:38** · want to at least at a high level show

**12:40** · you how everything works here. I think

**12:41** · it'll really click for you. So, we start

**12:43** · with a session start hook. And so, this

**12:46** · is going to run whenever we start a new

**12:48** · Claude code session. And all we're doing

**12:50** · with this simple Python script is

**12:52** · loading in the agents.md. We covered

**12:55** · this earlier. That's so our Claude code

**12:57** · understands the system that we put in

**12:59** · it. And then it's also loading in if we

**13:01** · go into the knowledge, this is our wiki

**13:03** · equivalent. We're loading in our

**13:04** · index.md. You've already seen this as

**13:06** · well. This is our actively maintained

**13:08** · list of files so our agent can query

**13:11** · more efficiently.

**13:12** · And so, whenever we begin a new Claude

**13:14** · code session, it has both of those

**13:16** · things already. And so, now I can ask a

**13:18** · question. Just for a demo purposes, I

**13:20** · have a knowledge base already built up

**13:21** · for a project. And so, I'm asking

**13:24** · something that it wouldn't really know

**13:26** · by itself without having to do a deep

**13:28** · analysis in the code base. But, right

**13:30** · here, it's just going to rely directly

**13:32** · on what we have in our knowledge base.

**13:33** · Take a look at that. Based on your

**13:35** · knowledge base, here are the key things

**13:37** · to watch out for. Then, some technical

**13:38** · details you don't have to cover here,

**13:40** · but then it calls out the specific KB

**13:42** · articles that it referenced in order to

**13:44** · get us this answer. And so, the index

**13:47** · told it where to point. It ran some

**13:49** · queries we'll talk about in a little

**13:51** · bit, and it pulled things from our

**13:53** · knowledge. And so, again, we have the

**13:55** · equivalent of our raw folder with our

**13:57** · daily logs. This is where we're going to

**13:58** · capture summaries of every single

**14:00** · conversation with Claude code. I'll show

**14:02** · you how we do that with the other hooks

**14:04** · in a second. So, daily logs, that's our

**14:06** · raw equivalent. And then, we have our

**14:08** · wiki. This is where we have the things

**14:10** · that are better formatted, linked

**14:12** · together. We have the whole graph view

**14:14** · here in Obsidian. This is what our agent

**14:16** · is searching through. And I know this is

**14:18** · a really basic example here, but just

**14:20** · like think for a second how powerful

**14:22** · this actually is. If I ask this question

**14:24** · without this whole system built in, it

**14:27** · would have had to look through the git

**14:28** · log, and even that might not have had

**14:30** · the lessons for what to watch out for.

**14:32** · It would have had to spin up sub-agents

**14:33** · to look through the code base, which

**14:34** · would be painfully slow, especially if

**14:36** · the code base was bigger. But, since

**14:38** · we're maintaining takeaways from all of

**14:40** · our conversations with Claude code, I

**14:42** · was able to get this answer in like 10

**14:45** · seconds. You saw it happen live. And so,

**14:47** · the other really powerful part of this

**14:49** · entire system is the other two hooks. We

**14:51** · have a pre-compact and a session end.

**14:53** · And they're both actually doing a very

**14:55** · similar thing. Whenever we're about to

**14:57** · lose context, either through closing off

**14:59** · a session or doing memory compaction,

**15:02** · we want to send the latest messages from

**15:05** · Claude code into another large language

**15:08** · model to process and create the summary.

**15:11** · And that summary is what we're going to

**15:12** · put in the daily log file. So, like this

**15:15** · is the summary from one conversation,

**15:17** · you know, decisions that were made,

**15:18** · lessons that were learned, action items,

**15:20** · and then we go on to the next session.

**15:21** · We have a very standard format here

**15:23** · handling every single Claude code

**15:25** · session.

**15:26** · And the way that this works is this

**15:28** · hook, actually both of these hooks, they

**15:31** · are going to call the Claude agent SDK

**15:34** · under the hood. So, we have a separate

**15:36** · Claude process running where it's just

**15:38** · given the transcript from the

**15:39** · conversation and it summarizes things

**15:41** · here. So, we're doing that initial layer

**15:44** · of data processing. And not to get too

**15:47** · technical here, but one other really

**15:49** · powerful part of this is we have the

**15:50** · flush process.

**15:52** · And so, once a day, we're going to take

**15:55** · the logs. We're going to extract the

**15:58** · concepts and connections from them and

**16:00** · then that's what we populate in the

**16:01** · wiki. And then our search is going to

**16:03** · focus here in knowledge, but then it can

**16:05** · also look through the daily logs if we

**16:07** · want as well. So, we have full

**16:08** · information about everything here,

**16:11** · lessons learned, decisions made. If you

**16:12** · want to customize this, you can even go

**16:14** · into the scripts here. You can go into

**16:17** · the flush or you could go into the

**16:19** · compile and you can actually change the

**16:21** · prompt that we send into the Claude

**16:23** · agent SDK under the hood. So, another

**16:25** · beautiful part about this whole setup,

**16:27** · unlike Claude code's memory system, is

**16:29** · you can customize this to your heart's

**16:31** · content. And Claude code can even walk

**16:33** · you through making the customizations

**16:35** · because it has access to the agents.md.

**16:37** · It knows how everything works. It knows

**16:39** · where the prompts are. It knows how the

**16:41** · memory promotion process works. It knows

**16:43** · where the daily logs are. So, it's very

**16:46** · it's a very self-contained system that

**16:48** · can improve itself. And speaking of

**16:50** · improving itself, that's actually the

**16:51** · last big thing that I want to cover with

**16:53** · you. I want to talk about the

**16:54** · compounding loop. Cuz think about this

**16:56** · with me for a second. We always will

**16:57** · start by asking some kind of question.

**17:00** · We want to leverage our knowledge base.

**17:02** · We're going to get some kind of answer

**17:04** · with our agent searching across many

**17:05** · different wiki articles. So, it's

**17:07** · extending its arm across our knowledge

**17:09** · base, synthesizing information together,

**17:12** · but then it's going to file that single

**17:14** · answer. So, we're constantly connecting

**17:16** · information between our conversations

**17:19** · and saving that. And so our Wiki grows

**17:21** · over time because of that. And then also

**17:22** · all the new information coming in from

**17:25** · all of our future Claude code sessions.

**17:27** · And so we're building up our knowledge

**17:29** · base over time. The agent is going to be

**17:31** · able to search through our knowledge

**17:32** · better over time as we ask more

**17:34** · questions. It just gets better and

**17:37** · better and better. And we really don't

**17:39** · have to do anything to maintain this.

**17:41** · For example, if I extend the

**17:43** · conversation where I ask our first

**17:45** · question here to have it do more web

**17:47** · research, I have more takeaways. All I

**17:49** · have to do is end the session or do a

**17:51** · memory compaction. And then

**17:53** · automatically, we can see that the logs

**17:55** · are I saw this just come up here. We

**17:57** · already have the Claude agent SDK

**17:59** · running in the background. It can use

**18:00** · your Anthropic subscription just like

**18:02** · Claude code. So you don't have to set up

**18:03** · any API key or anything. And it's

**18:06** · automatically going to extract takeaways

**18:07** · and put it in our daily logs. Let's

**18:09** · actually look at this right now cuz I

**18:10** · believe it already finished. There we

**18:12** · go. Take a look at this. So this is our

**18:13** · session that just ran. We were exploring

**18:15** · best practices for handling external

**18:17** · service data. And then we have these key

**18:20** · exchanges, lessons learned from our

**18:22** · additional web research. We're building

**18:24** · this up over time. It'll eventually get

**18:26** · promoted into our Wiki here. We don't

**18:28** · have to do anything. And the questions

**18:31** · that we ask our agent are just going to

**18:32** · get better and better answers over time.

**18:35** · Very, very powerful. So there you go.

**18:37** · That is LLM knowledge bases for internal

**18:39** · data, long-term memory for our second

**18:41** · brains instead of external data like

**18:43** · Karpathy's implementation. But of

**18:45** · course, thanks to him for all of the

**18:47** · inspiration here. And Claude code hooks

**18:49** · is something I've been building into my

**18:51** · second brain for a long time now. And so

**18:53** · I recently did a 4-hour workshop in the

**18:56** · Dynamis community where I showed

**18:58** · everything. I actually built my second

**19:00** · brain again from scratch. And so

**19:02** · definitely check out the Dynamis

**19:04** · community linked in the description and

**19:05** · pin comment if you're interested in

**19:07** · building your own second brain on top of

**19:10** · Claude code and the Claude agent SDK.

**19:12** · Otherwise, if you appreciate this video

**19:14** · and you're looking forward to more

**19:15** · things on building agents and second

**19:17** · brains, I would really appreciate a like

**19:19** · and a subscribe. And with that, I will

**19:21** · see you in the next video.
