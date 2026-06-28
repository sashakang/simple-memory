---
title: "The One AI Writing Hack Nobody Talks About."
source: "https://www.youtube.com/watch?v=ltbzgzZZmgI"
author:
  - "[[AI News & Strategy Daily | Nate B Jones]]"
published: 2026-05-22
created: 2026-06-28
description: "Full Post w/ Prompt Pack: https://natesnewsletter.substack.com/p/ai-organize-files-before-writing?r=1z4sm5&utm_campaign=post&utm_medium=web&showWelcomeOnShare=true ________________..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=ltbzgzZZmgI)

Full Post w/ Prompt Pack: https://natesnewsletter.substack.com/p/ai-organize-files-before-writing?r=1z4sm5&utm_campaign=post&utm_medium=web&showWelcomeOnShare=true
__________________________________
What's really happening when prestigious law firms file motions full of AI hallucinations? The common story is that better prompts prevent hallucinations — but the reality is more complicated.

In this video, I share the inside scoop on the project room workflow that makes hallucinations structurally unlikely:

 • Why your first AI prompt should never be "do the thing"
 • How agents now walk folder trees and compare files cleanly
 • What artifacts make an agent's judgment visible and inspectable
 • Where most serious knowledge work breaks down before the draft

Operators doing high-stakes knowledge work with AI agents need to shape the canvas before the writing starts, or they ship the same soft spots that landed Sullivan and Cromwell in front of a federal judge.

Chapters
00:00 The Sullivan and Cromwell hallucination story
01:30 Why a better prompt cannot fix this
03:00 What changed with Opus 4.7 and GPT-5.5
04:30 Three takeaways for serious knowledge work
06:00 Why your first prompt is never "do the thing"
07:30 The messy source material problem
09:00 Introducing the project room workflow
10:30 Where to build your room across tools
12:00 The source inventory table
14:00 The conflict log artifact
15:30 The missing context list
17:00 Why duplicates are a reasoning problem
18:30 Files as the canvas for agentic work
20:00 The short writing prompt that finally works

Subscribe for daily AI strategy and news.
For deeper playbooks and analysis: https://natesnewsletter.substack.com/

Listen to this video as a podcast.
- Spotify: https://open.spotify.com/show/0gkFdjd1wptEKJKLu9LbZ4
- Apple Podcasts: https://podcasts.apple.com/us/podcast/ai-news-strategy-daily-with-nate-b-jones/id1877109372

## Transcript

_Caption track: English auto-generated or provided._

**0:00** · A few weeks ago, Sullivan and Cromwell,

**0:02** · one of the most prestigious law firms on

**0:04** · the planet, had to write an apology

**0:06** · letter about AI to a federal bankruptcy

**0:08** · judge. Their emergency motion in a

**0:10** · chapter 15 case had been filed with

**0:12** · dozens of fabricated or misqued

**0:14** · citations. AI hallucinations. The other

**0:16** · side's lawyers caught them. Sullivan and

**0:18** · Cromwell's own review did not. The

**0:21** · partner who signed the apology letter is

**0:23** · the co-head of the firm's restructuring

**0:25** · practice. This is the failure mode I

**0:27** · want you to think about with me for the

**0:29** · next few minutes. I'm not talking about

**0:31** · 2024 hallucinations where a solo

**0:33** · practitioner uses chat GPT and tries to

**0:36** · tell it not to hallucinate. I'm talking

**0:38** · about organizational and structural

**0:41** · hallucinations at the top of aic

**0:43** · workflows. In this case, the motion

**0:45** · looked legitimate. The structure of the

**0:47** · motion was correct. The citations were

**0:49** · professionally formatted. Dozens of them

**0:51** · were pointing at the wrong things and

**0:53** · nobody on the team caught it before the

**0:55** · filing. The model is not the problem

**0:57** · here. The working environment around the

**0:59** · model is the problem and it's the source

**1:01** · for most of our 2026 hallucinations. I

**1:04** · know what some of you are thinking,

**1:06** · Nate, the answer is a better prompt. We

**1:08** · talked about this. Just tell the model

**1:09** · not to hallucinate. And by the way, the

**1:11** · Mark Andrees screenshot has been all

**1:13** · over the timeline for a few days now. It

**1:16** · doesn't work. You cannot tell a language

**1:19** · model not to hallucinate any more than

**1:22** · you can tell autocomplete not to

**1:23** · autocomplete. There is no separate truth

**1:26** · check pass inside the model that the

**1:29** · instruction can hook into and have some

**1:31** · purchase and meaning. Sullivan and

**1:33** · Cromwell had access to the best AI

**1:35** · tooling that money can buy. The wrong

**1:37** · detail still made it into court. The fix

**1:40** · is not a sharper prompt. It just isn't.

**1:43** · In the last month with 4.7 Opus and 5.5

**1:47** · from OpenAI, agents have picked up a

**1:49** · capability that changes the way we think

**1:51** · about this. And I don't think law firms

**1:53** · or most other people have realized it

**1:54** · yet. There is a fix. It is not a prompt

**1:57** · fix. And that's what I want to talk

**1:59** · about today. So what is it about 4.7 and

**2:02** · 5.5 that's special? They do longunning

**2:05** · agentic tasks, as I've said a lot, but

**2:07** · they do it on your file system. And

**2:10** · that's such an unsexy thing to talk

**2:12** · about. Oh, files. That's all the way

**2:14** · back to 1982, right? Like that's a long

**2:16** · time ago we handled files. Longer ago

**2:18** · than that. Why do we care about files

**2:20** · now? Why do we care that agents that are

**2:22** · long running are now very good at taking

**2:24** · and manipulating files? And how does all

**2:26** · of that connect to the hallucination

**2:28** · story? I will tell you these new agents

**2:31** · do not just read what you paste. They

**2:33** · can walk a folder tree. They can open

**2:35** · files. They can compare dates across

**2:37** · documents. They can inspect metadata.

**2:39** · The workflow around hallucinations has

**2:42** · flipped, but most people haven't caught

**2:45** · that yet because the first useful prompt

**2:47** · in a serious project is now like it's

**2:50** · not write the document, right? It's much

**2:52** · more boring than that. It is build me

**2:54** · the folder in the file room. Build me

**2:56** · the room to do the work in. And I want

**2:59** · to talk to you about three key takeaways

**3:02** · in this video. And if you follow them,

**3:04** · you are not going to end up in the same

**3:06** · hallucination place because you will

**3:08** · have set up a process that is

**3:10** · structurally antagonistic to

**3:12** · hallucinations. I'm not saying they

**3:14** · never happen. I am saying that you are

**3:16** · building a structure that makes them

**3:18** · much less likely to occur at scale and

**3:21** · it keeps you and the work you do much

**3:24** · more accurate and much less likely to

**3:26** · lead to the kind of corporate liability

**3:28** · that this prestigious law firm generated

**3:31** · for itself because it did not think

**3:33** · through its agentic pipeline correctly.

**3:35** · It all comes back to file. So here we

**3:37** · go. Three things. One, why your first AI

**3:41** · prompt is never do the thing. And I

**3:43** · talked about that just above. We're

**3:44** · going to get into why that is. Two, what

**3:46** · to ask the agent for when you want to go

**3:49** · deeper and how you do that

**3:50** · intelligently. And three, why this

**3:53** · approach actually works with 5.5 in

**3:56** · particular. 5.5 is really good at this

**3:57** · and also with 4.7 as well. Look, the

**4:00** · thing that sold me on this workflow was

**4:02** · a real moment that I had multiple real

**4:05** · moments over the last couple of weeks

**4:06** · with codeex. I have been in situations

**4:10** · where the AI agent has now been able to

**4:13** · do incredibly powerful simultaneous

**4:17** · drafting of up to eight different

**4:19** · documents. I haven't gone past eight

**4:21** · yet. I think I could. And the only way I

**4:24** · could get eight documents drafting at

**4:26** · once in codeex is because I prepared the

**4:29** · data room first and I knew my outputs

**4:32** · and I could then execute really cleanly

**4:35** · and consistently. And it saved me so

**4:37** · much time. It was an incredible speed

**4:40** · up. It felt like the hair was blowing

**4:42** · back on my face and I was living in the

**4:43** · future. And I think that that's one of

**4:45** · the things that we need to pay attention

**4:47** · to is that we get these aha moments when

**4:50** · we think about the boring primitives

**4:52** · when we think about the files. And

**4:53** · that's why we're going to talk about

**4:54** · look because of chat GPT. Back in 2022,

**4:57** · most people think the AI workflow starts

**4:59** · with doing a job. Does the model write

**5:02** · for me? Does the model code for me? Does

**5:03** · the model make the Excel file? that's

**5:05** · where the value is, right? It starts

**5:07** · when the agent walks in and does

**5:10** · something. But I don't think that's

**5:11** · true. I think a serious project almost

**5:14** · never has its source material organized.

**5:16** · And we have had to be the human

**5:18** · organizers for most of the prompting era

**5:21** · in the last couple of years. We've had

**5:22** · to find the strategy docs and the

**5:24** · meeting transcripts and the spreadsheets

**5:25** · and the half-finish notes and the

**5:26** · follow-up emails and the old deck and

**5:28** · the PDF you forgot about and the Slack

**5:30** · thread where the actual decision was

**5:31** · made. Can you tell I've actually had to

**5:33** · do this? Some of it is current. Some of

**5:34** · it is stale. Some of it contradicts

**5:36** · itself. A few files may be helpful.

**5:38** · You're not sure which one is the source

**5:39** · of truth. You're often wrong. When you

**5:41** · ask an AI to write from that general

**5:44** · mess, you're asking it to do two jobs at

**5:46** · once. Job one, figure out what this is.

**5:49** · And job two, produce this beautiful

**5:51** · artifact for me. That is a recipe for a

**5:53** · really mediocre result. And it's one of

**5:55** · the situations in which it's likely that

**5:58** · you will have a hallucination problem in

**6:01** · the way that this law firm did. The

**6:03** · model didn't have a clean working

**6:05** · environment. So, the dirt got into the

**6:07** · dock. It didn't know which sources

**6:09** · mattered. It didn't know what was stale.

**6:11** · It didn't know what was missing. It

**6:12** · didn't know which file was

**6:13** · authoritative. You cannot patch that

**6:16** · with a better opening sentence. And you

**6:18** · really can't patch it by reading the doc

**6:20** · and hand editing anymore because we're

**6:21** · working at a different kind of scale.

**6:23** · You have to patch it and prevent it from

**6:25** · the beginning by cleaning up your data

**6:27** · room first. So your first instruction

**6:29** · should not be do the thing like write

**6:31** · the memo, make the Excel etc. Instead,

**6:34** · your first instruction needs to be find

**6:36** · the relevant materials on the internet

**6:40** · on my local computer in my files in the

**6:42** · tools that I have connected to you. And

**6:44** · by the way, Claude and Codeex both have

**6:46** · a ton of connectors now. And so you can

**6:48** · actually tell them to look in their

**6:49** · connectors and they will. And so the

**6:50** · first instruction is find the relevant

**6:52** · materials, preserve the originals, build

**6:54** · me a data inventory, put it in a folder,

**6:57** · tell me which files seem authoritative,

**6:59** · which are duplicates, which are old,

**7:00** · which are missing. Summarize every

**7:02** · source before you synthesize anything.

**7:04** · And do not write the deliverable yet.

**7:06** · We're just learning. That is so

**7:08** · powerful. And it's possible because

**7:11** · these tools can do complex longunning

**7:13** · file manipulation tasks successfully and

**7:16** · with very high accuracy. So let's use

**7:18** · them to do that. Let me give the

**7:20** · workflow a name so we can talk about it

**7:22** · very very clearly. I'm calling it a

**7:25** · project room or a data room. A project

**7:27** · room is a bounded workspace for one

**7:29** · serious job. It's a project, a

**7:31** · deliverable, a source set. Now, this is

**7:34** · much smaller than a whole second brain.

**7:36** · It's much more specific than a knowledge

**7:38** · management system. It is a workspace set

**7:40** · up so an agent can do useful work inside

**7:42** · it. And in most cases, it is a local

**7:44** · workspace. This is different than a lot

**7:48** · of the published cloud solutions that

**7:50** · claude and chatgpt and codeex have had

**7:53** · where they say here start up a project

**7:54** · and sort of a shared context window that

**7:57** · people can all chat into and all work

**7:59** · with. I have found those have been much

**8:01** · less useful than the flexibility of a

**8:04** · local file system. And there is a whole

**8:06** · 2026 conversation to be had around the

**8:08** · idea that we are going back to files and

**8:10** · going back to simple primitives. And

**8:12** · those tend to work really really well

**8:14** · because LLMs are being taught to use

**8:17** · computers at their most primitive and

**8:19** · root level in order to successfully do

**8:21** · anything on computers. And when we go

**8:23** · back to files, we are going back to what

**8:25** · they know really, really well. Why not,

**8:27** · right? Why not lean into it? So, let me

**8:28** · give you an example. For a consulting

**8:30** · project, this could look like client

**8:32** · decks, interview transcripts, data

**8:34** · exports, prior proposals, meeting notes.

**8:36** · For a house purchase, it's inspection

**8:38** · reports, disclosures, contractor

**8:40** · estimates, mortgage documents, email

**8:42** · threads. For a Substack, article you're

**8:43** · writing, it could be uh sources you're

**8:45** · researching, transcripts, draft notes,

**8:48** · screenshots, prior related posts. For a

**8:50** · board doc, it's a financial model, an

**8:52** · operating plan, an old board deck, the

**8:53** · current KPI exports, and the notes from

**8:55** · the last three review meetings. The

**8:57** · point here is that you don't have to

**8:59** · build a perfect archive to gain a

**9:01** · tremendous amount of advantage in the

**9:03** · task you're setting the model. The point

**9:05** · is just to give the agent a usable work

**9:07** · surface, just enough room for it to

**9:09** · operate. Where you build your room, of

**9:12** · course, will depend on your preference

**9:14** · on your source set. Look, you can do

**9:16** · this in cloud projects. It's solid when

**9:18** · you need a bounded workspace with

**9:19** · uploaded docs. Chat GPT projects handle

**9:22** · smaller sort sets and spreadsheets.

**9:24** · Cursor or clawed code is the right tool

**9:26** · in the room. Includes a code or folder

**9:27** · tree. Codeex works for that too.

**9:30** · Notebook LM works when it's very sort of

**9:32** · research heavy and sourcebounded. And

**9:34** · like I said, my personal preference,

**9:36** · just go to local files, have it create a

**9:39** · folder, and you can stick literally

**9:40** · anything in there. And that's what I

**9:42** · love about it because there's no like

**9:43** · file type limitations that you get with

**9:45** · some of the tools I mentioned. If it's a

**9:47** · file, it goes in there. And if Codex can

**9:49** · read it or Claude can read it, you're in

**9:50** · good shape. So, if you want to dive

**9:52** · deeper on different options to organize

**9:54** · your files from the all those different

**9:57** · tools and how you want to think about

**9:58** · making that choice, I put that on

**10:00** · Substack. You can dig into strategies

**10:01** · for local file organization because

**10:03** · imagine doing 20 projects. You're going

**10:05** · to need to have some thinking around

**10:06** · that. Uh you're going to want to dig

**10:08** · into strategies if you want to use other

**10:09** · tools too like uh projects on claude or

**10:12** · on notebook LM looking at the sort of

**10:14** · the folder structure, how you think

**10:15** · about project breakdown. I've got all of

**10:17** · that in detail there. We're going to

**10:19** · stick in this video with how we think

**10:21** · about this as an archetype, how we think

**10:23** · about this as a larger pattern that

**10:25** · works across many tools. So let's keep

**10:27** · moving. So, you have your folder. You

**10:30** · have stuff in it. The most important

**10:32** · artifact in this whole folder I haven't

**10:35** · talked about yet. It's a table. It's

**10:37** · just a table. Hear me out. It's called

**10:38** · the source inventory. And once the room

**10:40** · exists, it's the first thing you ask the

**10:43** · agent to produce. For every file in the

**10:45** · room, the agent records the path, the

**10:48** · type, the date, the apparent authority,

**10:50** · whether the file is current or

**10:51** · superseded, what claims it supports,

**10:54** · what its limitations are, and how it

**10:55** · should be used in the final work. Yeah,

**10:57** · that does sound boring. It's also the

**10:59** · artifact that determines whether

**11:00** · everything downstream is any good. And

**11:02** · by the way, it's an artifact that makes

**11:04** · it really, really helpful when another

**11:06** · LLM checks your current LLM's work. It

**11:09** · makes it easy to pass. The inventory

**11:11** · tells you what the agent thinks the

**11:12** · project consists of, which is critical,

**11:14** · and that gives you a chance to correct

**11:16** · the working set of docs and and current

**11:18** · set of data before the final draft is

**11:21** · going to like inherit a bunch of

**11:23** · mistakes and lead to hallucinations,

**11:25** · frankly. And so yes, I do recommend

**11:27** · checking what is in your inventory and

**11:30** · making sure you're aligned with it and

**11:31** · nothing is missing. And when in doubt,

**11:32** · just say, "Hey, you know, codeex, I

**11:35** · think this transcript may not be in

**11:36** · here. Can you check and if need be,

**11:37** · create a file for it?" And we'll do

**11:39** · that. And the beautiful thing is these

**11:40** · agents are strong enough to sort this

**11:42** · out. Right? They can tell that an

**11:44** · approved deck represents the story even

**11:46** · when the underlying data lives

**11:47** · elsewhere. That the old PDF might be

**11:49** · useful background but not a source for

**11:51** · current claims. and the the agents

**11:53** · really can sort that out at the at the

**11:55** · opus 4.7 at the Chad GPT 5.5 level and

**11:58** · and the inventory artifact that you you

**12:01** · create that table I'm talking about what

**12:03** · you're really doing is you're making the

**12:06** · agents judgment visible and legible so

**12:08** · you can see it really really clearly

**12:11** · because if you review the inventory and

**12:12** · you can't tell why one file outranks

**12:14** · another you can just like focus on

**12:16** · getting the inventory right focus on

**12:18** · making sure all the data is there before

**12:19** · you have to go farther it's a really

**12:21** · clean gate Now, I have been testing

**12:23** · different knowledge systems for AI and

**12:26** · the the organization framework that I

**12:28** · landed on for large projects is

**12:30** · something I'm writing up in a lot of

**12:31** · detail on Substack. So, if you're

**12:33** · serious about AI work, if you're trying

**12:34** · to figure out how you organize these

**12:36** · files at a 10, 20, 30 project scale so

**12:39** · you're clean and you understand what

**12:41** · you're working with, that's what you

**12:42** · want to get to. Like, I have it all

**12:43** · written up over there. Let's get into a

**12:46** · couple of more artifacts to illustrate

**12:47** · the principles because remember that's

**12:49** · what we're doing. So, we talked about

**12:50** · the table. Let's talk about two more

**12:52** · artifacts. The first is the conflict

**12:54** · log. When the agent reads a serious

**12:57** · source set, it will find disagreements.

**12:59** · The old PDF says one thing, the current

**13:00** · plan says another. The transcript uses a

**13:02** · different name for a person who's a key

**13:04** · stakeholder versus a doc. The

**13:06** · spreadsheet has a number with no visible

**13:08** · assumptions behind it. Two documents

**13:09** · that look adjacent are actually three

**13:11** · months apart. A weak workflow lets the

**13:14** · agent synthesize and smooth those

**13:16** · conflicts over. The output will read

**13:18** · confidently, but you don't know what you

**13:19** · can trust. you get into the same

**13:21** · hallucination problem that the law firm

**13:23** · did at the beginning of this video. A

**13:25** · strong workflow surfaces that

**13:27** · disagreement without necessarily

**13:29** · resolving it or at least without

**13:30** · resolving it, without you being able to

**13:32** · tell. The conflict log allows your agent

**13:35** · to surface conflicts that I've just

**13:37** · described and recommended responses and

**13:40** · allows you to have opinions and edit,

**13:42** · adjust, tell the agent it's wrong, etc.

**13:45** · before you get into building the doc.

**13:48** · The second artifact I want to talk about

**13:50** · on top of the conflict log is the

**13:51** · missing context list. One of the best

**13:54** · signs that an agent is helping properly

**13:56** · is that it tells you what it doesn't

**13:58** · have to do the job well. The missing

**14:00** · decision, the number with no source, the

**14:02** · current version of a file that that's

**14:03** · nowhere to be found. The completely

**14:06** · absent data file that is referred to in

**14:09** · only one document. All that matters

**14:11** · because the missing material is often

**14:13** · more important than the material you

**14:15** · have. Your file can say as discussed and

**14:18** · the actual discussion can be somewhere

**14:20** · else. The deck can include a chart in

**14:21** · the data source ends up being way far

**14:24** · away and maybe not in your data room at

**14:25** · all. Ask for the final memo or the final

**14:29** · output or whatever you're writing too

**14:30** · quickly and all of those gaps become

**14:32** · effectively hallucination traps. The

**14:34** · model invents its way around them to get

**14:36** · your job done and the pros looks fine

**14:38** · and you may ship something with a very

**14:40** · soft spot underneath and someone will

**14:42** · find it. So ask for the missing context

**14:44** · list first and those gaps become

**14:46** · transparent and legible and you can

**14:48** · review them. You can see them. You can

**14:50** · decide whether they matter, whether you

**14:51** · can find the source, whether you have to

**14:53** · phrase the claim more carefully. So the

**14:56** · full sevenfolder structure that I use

**14:58** · inside projects, every folder name, the

**15:00** · purposes, and all of that, I link that

**15:01** · in the substack. It's all laid out. You

**15:03** · can see it really cleanly there. Uh

**15:05** · we're going to go on from here to talk

**15:07** · about duplicates. And and I want to be

**15:10** · really honest about this because a lot

**15:12** · of people miss this. People think

**15:14** · duplicate detection in files is

**15:16** · housekeeping. But in AI work, duplicates

**15:19** · can be a reasoning problem. If the agent

**15:21** · sees three versions of a plan and

**15:23** · doesn't know which one is current, it

**15:25** · might blend them. The same transcript

**15:27** · exported twice can get overweighted in

**15:29** · the synthesis if you're not careful. An

**15:31** · old deck and a new deck with similar

**15:32** · titles can become a source for wrong

**15:34** · claims. a revised budget sitting next to

**15:36** · an earlier copy. It produces averaged

**15:38** · assumptions, right? You do not want your

**15:40** · agent deleting duplicates, but you do

**15:43** · want it to produce a duplicates report

**15:46** · and probably a separate folder with

**15:48** · suspected duplicates and hand that back

**15:50** · to you. Let the agent find the mess. Let

**15:52** · the agent name the duplicates, name the

**15:54** · likely duplicates, name the level of

**15:56** · confidence, name the version families.

**15:58** · Do not let it silently resolve the mess,

**16:01** · especially when you care about the work.

**16:03** · the agent finds you decide that is a

**16:06** · really healthy way to have good clean

**16:09** · agentic pipeline work for very

**16:11** · complicated highv value critical

**16:13** · knowledge work. So why does all of this

**16:14** · matter? One more thing before I get to

**16:17** · like how we write the prompt to get

**16:19** · actually going into stuff. There's a

**16:21** · reason this matters now. The agents have

**16:24** · just gotten so much better at the

**16:26** · details of the file manipulation I'm

**16:28** · talking about. They really do walk

**16:30** · folder trees cleanly. They open files

**16:32** · well. They inspect metadata. They're

**16:34** · good at actually doing the nitty-gritty

**16:37** · work of file comparison at high fidelity

**16:40** · across hundreds of documents for a long

**16:42** · period of time. And so file organization

**16:45** · used to be something we had to do to

**16:47** · housekeep for ourselves. Increasingly, I

**16:50** · think of it as a canvas that we have to

**16:53** · work with the agent to create so that

**16:55** · the final work reflects the underlying

**16:58** · data. In that sense, the data underneath

**17:00** · is the substrate for the canvas. It's

**17:01** · that white gesso that's on the surface

**17:03** · of the canvas and then you paint across

**17:05** · it the work you want to create with your

**17:06** · agent. But if you don't get the canvas

**17:09** · right, you're never going to get the

**17:11** · final work to look right. And that's

**17:13** · what we're doing with a data room.

**17:14** · You're framing the work. Literally,

**17:16** · you're framing the work. And because we

**17:17** · are now doing harder work because the

**17:19** · agents are more capable, our traditional

**17:22** · ways of compensating don't work. You

**17:24** · used to be able to compensate for a

**17:25** · messy folder with a sharp prompt. It's

**17:27** · too big now. You can't now. The mess is

**17:30** · becoming structural and entangled and

**17:32** · it's becoming something that you can't

**17:33** · clean up with a single prompt. The mess

**17:36** · is sitting inside the agent's context

**17:38** · window and it's something that the agent

**17:40** · will disentangle in the best way it

**17:42** · knows how. And the risk is actually

**17:44** · higher because the agent will find you

**17:46** · know no matter what come hell or high

**17:48** · water and a way to disentangle it

**17:50** · because that's its job and it's trained

**17:52** · to go after that task aggressively. You

**17:54** · may just not have ever seen that way of

**17:56** · disentangling it. you may not be

**17:57** · aligned. And that's exactly where you

**17:59** · get the kinds of hallucinations that we

**18:02** · saw in the law firm at the top of this

**18:03** · video. That's that's the structural

**18:06** · reason those sorts of things start to

**18:08** · surface in final materials. Now, the

**18:10** · good news is we're finally at the prompt

**18:12** · part. I know you guys are waiting for

**18:13** · it. Once the room is in shape, once you

**18:16** · have inventory, conflict log, missing

**18:18** · context list, duplicates report, the

**18:20** · writing prompt actually gets really

**18:22** · short. It's not long and the output gets

**18:24** · much better. Before the room, the prompt

**18:27** · was like, "Write me a strategy memo.

**18:29** · Here are a bunch of files." And then if

**18:30** · you're doing prompt engineering, it's a

**18:32** · very detailed like, "Here's what I want

**18:33** · you to write." After the room, after you

**18:35** · have your data together, the prompt is

**18:38** · very simple. Use the reviewed source

**18:40** · inventory in the project room in the

**18:41** · working brief. Treat the current

**18:43** · operating plan as authoritative for

**18:45** · numbers, the transcript as source

**18:47** · material for decision context, and the

**18:48** · older deck as background only. Draft the

**18:50** · memo, site claims, flag anything not

**18:52** · supported. The key here is that all I'm

**18:55** · doing in that prompt is I am saying this

**18:59** · is what matters to me. This is what I

**19:01** · care about from a conflict perspective.

**19:04** · This is what I think the authoritative

**19:06** · true line is for this piece of work that

**19:08** · we're working on together. And then you

**19:11** · go do the rest. And this makes the AI's

**19:14** · work inspectable. It's not that I'm

**19:16** · saying if you do this the AI's work will

**19:17** · be perfect. But it is the difference

**19:19** · between using AI as a colleague and

**19:22** · using AI as a gopher. And we are really

**19:26** · underusing these agents if we treat them

**19:28** · like gophers and say just go deal with

**19:29** · stuff and we don't give them any any

**19:32** · ability to think about their structure

**19:34** · and their context with us. They are more

**19:36** · senior than that. Now our AI agents

**19:38** · deserve to be able to shape their

**19:40** · context windows and their data rooms

**19:42** · together with us if we want to get the

**19:44** · most out of them. and they are capable

**19:46** · of doing so. Now, a word on calibration

**19:48** · before I close. I am talking

**19:50** · specifically about agents for serious

**19:53** · knowledge work. Right? If you are

**19:55** · working with codecs for a 30, 40, 50

**19:57** · hour, two-hour run, this makes sense. It

**20:00** · makes sense for coding. It makes sense

**20:02** · for heavy knowledge work like I've been

**20:03** · discussing with projects and reports. Do

**20:06** · not run this workflow on every casual

**20:08** · interaction with AI. It's way overkill.

**20:10** · Also obviously I am not talking about

**20:12** · using this approach to produce agentic

**20:15** · pipelines that take care of back office

**20:17** · operations. You still need a data

**20:19** · strategy. You need to think about how

**20:20** · you input data. That's important and I

**20:22** · cover it in other videos, but it's not

**20:24** · this problem. And yes, I have more

**20:26** · prompts on the Substack. I know that not

**20:28** · everyone has the exact prompt situation

**20:30** · that I gave you. If you want more sample

**20:32** · prompts that kind of cover a wider

**20:34** · variety of use cases for this kind of

**20:35** · knowledge work, it's on the Substack.

**20:37** · you can grab them and apply it to your

**20:39** · messiest folder this week. It'll help.

**20:40** · So, in closing, here's the mental model

**20:43** · shift that I want you to walk away with.

**20:45** · I'm really passionate about this. I

**20:47** · think this is one of the most slept on

**20:48** · implications of AI in the last 40 days

**20:50** · and and we're not talking about it

**20:52** · enough because it's files and it's

**20:53** · boring. The old AI question was whether

**20:55** · the model could do the thing, right?

**20:56** · Could it write the memo? Could it make

**20:58** · the spreadsheet? Could it write the

**20:59** · code? Those questions still matter.

**21:01** · They're just not the most powerful

**21:03** · questions anymore because the models

**21:05** · have gotten so good. The new question is

**21:06** · whether the agent can help prepare the

**21:08** · conditions under which good work

**21:10** · happens. Can it shape the canvas? Can it

**21:12** · find the right sources? Can it tell

**21:14** · which ones are current? Can it identify

**21:16** · what's missing before it invents around

**21:18** · the missing thing? That's where agents

**21:20** · start to feel really useful as

**21:22** · colleagues for real work. Because an

**21:23** · agent can walk into a messy room, it can

**21:25** · turn on the lights. It can label what's

**21:27** · in all of the folders. And it can get

**21:29** · the entire desk area organized for

**21:31** · serious work. That is an AI worth using.

**21:35** · Please use your AI that way. And I'm

**21:37** · talking specifically about Chad GPT 5.5

**21:41** · and Opus 4.7. I would not do this with

**21:43** · earlier models. I hope this has been

**21:45** · helpful. There will be more practical

**21:46** · tips coming on this channel shortly, so

**21:48** · subscribe for more. Cheers.
