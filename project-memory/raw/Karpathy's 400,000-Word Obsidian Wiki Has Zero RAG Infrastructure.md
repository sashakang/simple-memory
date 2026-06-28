---
title: "Karpathy's 400,000-Word Obsidian Wiki Has Zero RAG Infrastructure"
source: "https://www.youtube.com/watch?v=VUnABqzrZQg"
author:
  - "[[Josh Pocock]]"
published: 2026-04-06
created: 2026-06-28
description: "Andrej Karpathy just posted a system that replaces personal vector RAG with a folder of markdown files.  No vector database. No embeddings. No retrieval chain. Just Obsidian, Claud..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=VUnABqzrZQg)

Andrej Karpathy just posted a system that replaces personal vector RAG with a folder of markdown files.

No vector database. No embeddings. No retrieval chain. Just Obsidian, Claude Code, and one schema file. He is running a 400,000-word research wiki on it.

In this video I walk through the complete pattern: the three-layer architecture, the CLAUDE.md schema file line by line (the part nobody else shows on camera), a live ingest, three query patterns, a live lint health check, and the honest comparison against vector RAG.

Plus you get the finished Obsidian vault template. Folder structure, schema file, example pages, pre-installed plugins, and a sample article ready to compile. Download, open in Obsidian, run Claude Code. Working wiki in 90 seconds.

📄 DOWNLOAD THE FREE VAULT TEMPLATE & FREE REFERENCE DOC (12 pages): https://www.skool.com/stride-ai-academy-7057

🎓 Free Stride AI Academy community:
https://www.skool.com/stride-ai-academy-7057

🚀 Premium community:
https://www.skool.com/stride-ai-automation-academy-9690

💼 Work with us:
https://www.executivestride.com/apply

⌛ Chapters
00:00 What Claude Code built while I was away
00:26 What you'll get (free template + resource doc)
00:57 Why every second brain fails
01:41 Who is Karpathy and why this matters
02:28 The three layers (raw, wiki, schema)
04:30 The four operations explained
05:09 Setting up Obsidian Web Clipper
05:54 Live ingest: clipping an article
07:24 Live compile: one command, 11 files touched
09:01 The CLAUDE.md file walkthrough
11:13 Lint and health checks explained
12:24 The citation rule (hallucination fix)
12:49 AI Research folder (Stride exclusive)
14:21 Query 1: Direct lookup
15:17 Query 2: Cross-topic synthesis
16:07 Query 3: File-back synthesis (the money shot)
17:30 AI Research query: QMD deep dive
19:11 Live lint pass
20:04 Vector RAG vs the wiki pattern
22:02 Objections: scale and hallucinations
23:37 Free vault template + resource doc
23:58 Wrap up

TOOLS IN THIS VIDEO:
Obsidian (free): https://obsidian.md
Claude Code: https://claude.com/product/claude-code
Obsidian Web Clipper (browser extension)
Local Images Plus (Obsidian community plugin)
Dataview (Obsidian community plugin)

SOURCES:
Karpathy tweet on LLM knowledge bases: https://x.com/karpathy/status/2039805659525644595
Karpathy gist (full pattern description): https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

STRIDE COMMUNITIES:
Free community: https://www.skool.com/stride-ai-academy-7057
Premium academy: https://www.skool.com/stride-ai-automation-academy-9690
Work with us: https://www.executivestride.com/apply

#karpathy #obsidian #claudecode #rag #knowledgebase #ai #secondbrain

## Transcript

**0:00** · Everything you're looking at right now

**0:01** · was built 100% with Claude Code and

**0:03** · Obsidian. Every wiki page, every

**0:06** · backlink, every summary, I simply

**0:08** · dropped in raw articles, raw transcripts

**0:11** · into a folder and walked away. When I

**0:13** · came back, I had this. Now, this entire

**0:16** · pattern didn't come from me. This came

**0:19** · from a Andre Karpathy tweet, which went

**0:22** · mega viral, and this whole entire setup

**0:25** · takes about 15 minutes, and you're going

**0:27** · to be getting access to this finished

**0:28** · vault template at the this video 100%

**0:31** · for free, no paywall or anything like

**0:33** · that. Now, you've probably saved

**0:35** · articles, podcasts, notes, whatever the

**0:38** · case is, you know, in Notion, PDFs,

**0:41** · podcast transcripts, and you meant to

**0:43** · review these, but you never got around

**0:45** · to them, and part of the reason of that

**0:47** · is is because none of it is actually

**0:49** · searchable. None of it's connected, it's

**0:52** · just scattered all over the place, and

**0:53** · none of it actually feeds into your

**0:56** · work. And every second brain system you

**0:59** · may have tried out there, whether it's

**1:01** · Notion, different systems and setups,

**1:03** · they typically fail for the same reason.

**1:05** · You stop maintaining it, and the reading

**1:07** · and thinking was never really the

**1:09** · problem, the bookkeeping was. Now, Andre

**1:11** · Karpathy just posted the fix on Twitter,

**1:14** · it went viral, he posted a gist as well,

**1:16** · which really dives deep, and all this

**1:18** · will be linked, of course, in the

**1:20** · description down below. I'm also going

**1:21** · to be giving you a free resource, it's a

**1:24** · 12-page document that literally goes

**1:26** · over everything, goes over in-depth this

**1:28** · entire system from start to end, which

**1:30** · we're, of course, going to dive deep

**1:31** · into in today's video. I also will be

**1:33** · giving you this exact template, so you

**1:35** · can literally just copy and paste and

**1:37** · start using this by the end of this

**1:38** · video for your own knowledge system.

**1:40** · Now, before we dive in, just to give you

**1:42** · some quick context in case you don't

**1:44** · already know, who is Andre Karpathy?

**1:46** · Well, he was a part of the founding team

**1:48** · at OpenAI, he was the head of AI at

**1:50** · Tesla, built the entire autopilot vision

**1:53** · stack, he created one of the most

**1:54** · popular deep learning courses on the

**1:56** · internet. You may have seen his recent

**1:58** · GitHub project go viral, auto research.

**2:01** · And when this guy posts a workflow for

**2:03** · managing knowledge, or really anything

**2:05** · about AI that he posts, it's worth

**2:08** · paying attention to, and really everyone

**2:10** · just listens. So, currently he is

**2:12** · running a 400,000 word personal research

**2:15** · wiki with no vector database, no

**2:18** · embeddings, no retrieval chain, just

**2:21** · markdown files and Obsidian, and one

**2:24** · schema file that Claude Code reads every

**2:27** · single session. Now, in the next 10

**2:29** · minutes or so, I'm going to show you the

**2:30** · entire pattern so you have a deep

**2:32** · understanding of it, every line of the

**2:34** · schema file that nobody else wants to

**2:36** · explain. I'm going to show you a live

**2:37** · compile, a live query, a live lint, and

**2:41** · by the end of this video, you will have

**2:42** · a working system and a template that you

**2:45** · can run on your own stuff. Now, every

**2:47** · version of this pattern has the same

**2:49** · three layers. Get these right and

**2:51** · nothing else really matters. So, layer

**2:52** · one is raw. This essentially is your

**2:55** · personal inbox as a human. So, what goes

**2:57** · in here are articles, papers,

**3:00** · transcripts, screenshots, anything that

**3:02** · you dump in here that you want the LLM

**3:04** · to read, and that's where it's going to

**3:06** · read is from this raw folder. Now, keep

**3:08** · in mind the LLM is never going to write

**3:11** · into this folder. This is literally just

**3:13** · an inbox for you to dump things in, and

**3:15** · this is immutable. It is your source of

**3:17** · truth. Now, layer two right here is the

**3:20** · actual wiki, so this is where the LLM

**3:22** · files live. It writes summaries, it

**3:24** · writes entity pages, it writes concept

**3:26** · pages, it builds an index, it maintains

**3:29** · cross-links between every article. You

**3:31** · read this layer in Obsidian. Now, you as

**3:34** · the human do not write in this layer.

**3:35** · Not because you can't, but because every

**3:37** · edit that you make in here is one that

**3:39** · the model cannot predict in the next

**3:40** · session, and the whole system starts to

**3:42** · drift. And then at the top here for

**3:44** · layer three is the schema. This is one

**3:46** · claude.md at the vault root. And this is

**3:50** · what turns a generic Claude Code session

**3:52** · into a disciplined librarian. Every

**3:54** · session it reads this file first, every

**3:56** · operation follows rules from this file,

**3:58** · and this is the core piece of the

**4:00** · system. Now, if you want a deep dive

**4:02** · into claude.md files, make sure to check

**4:04** · out this video right here I did a few

**4:06** · days ago on claude.md files and how to

**4:08** · properly structure them, but of course,

**4:10** · like I mentioned, I'm going to be giving

**4:12** · you this free template, which includes a

**4:14** · structured Claude MD that you can use

**4:16** · out of box. So, raw, wiki, schema. That

**4:19** · is the whole architecture. Now, let's

**4:22** · dive into the actual layers and how this

**4:24** · all works. So, there's really four

**4:26** · operations, and we're going to start off

**4:28** · with the first one, which is ingest. So,

**4:30** · this is where you drop one source in the

**4:32** · raw folder, and you tell Claude Code to

**4:35** · then compile it. And in one pass, it can

**4:37** · touch 10 to 15 wiki pages. Here's what

**4:39** · it actually does though under the hood.

**4:41** · So, it reads the raw file in full, then

**4:43** · it runs checks in the master index to

**4:46** · see if the topic already exists. If yes,

**4:49** · it updates the existing article and adds

**4:51** · backlinks from any related pages. If no,

**4:55** · it creates a new topic folder with its

**4:58** · own index file. Either way, it updates

**5:01** · the master index and appends a line to

**5:03** · the log, and the wiki has just

**5:05** · compounded by one source. All right, so

**5:07** · let me show you how this actually works

**5:08** · in action. So, first things first,

**5:10** · you're going to want to download the

**5:11** · Obsidian web clipper. So, link to this

**5:13** · will be in the resource below, and this

**5:14** · whole document, as well as all the

**5:16** · different resources, templates, etc.

**5:17** · from this video and others is available

**5:19** · in our free Stride AI Academy. Now, once

**5:22** · you go ahead and actually download this,

**5:23** · you'll see the Obsidian icon right here

**5:25** · for the extension. We can go ahead and

**5:27** · click on it. You're going to want to

**5:28** · click on settings to open up the

**5:30** · Obsidian settings. You'll see right

**5:31** · here, I actually selected the name of my

**5:34** · specific vault. By default, it will save

**5:36** · it to the open vault. You can also

**5:38** · create new templates for how it's going

**5:39** · to save it, or use this default one

**5:41** · right here, and all you're going to want

**5:43** · to do is just change this note location.

**5:45** · It's going to be clippings by default,

**5:47** · but you can change this to raw, or

**5:50** · whatever you want to have your actual

**5:52** · intake folder to be. Once we have that

**5:54** · set up, we're going to find a blog or

**5:56** · whatever piece of information that you

**5:58** · want to actually ingest into the system.

**5:59** · For this, we're going to be using one of

**6:01** · Claude's blog posts right here. I'm just

**6:02** · going to go ahead and click on this, and

**6:04** · then I'm going to click add to Obsidian.

**6:07** · Next, it's going to ask me to open

**6:08** · Obsidian. And boom, here you can see we

**6:11** · have this entire article with different

**6:13** · properties, such as the title, the

**6:15** · source, the author, when it was

**6:16** · published, created, a description, any

**6:19** · specific tags. And you can see here, it

**6:21** · literally pulled in everything,

**6:23** · including the images. Now, by default,

**6:25** · it won't actually pull in the images,

**6:27** · but we're using a plugin right here

**6:29** · called local images plus, which by

**6:32** · default is actually installed in the

**6:34** · template that I'm providing you for

**6:35** · free. Actually, every single plugin that

**6:37** · I cover is actually installed in this

**6:39** · template by default. But if you already

**6:41** · have an Obsidian setup and you're

**6:43** · setting this up in there, or whatever

**6:45** · the case is, maybe you just need to

**6:47** · install this plugin yourself. You can

**6:48** · just go over to community plugins, make

**6:50** · sure you turn them on, and then you're

**6:51** · going to want to search over here,

**6:53** · browse, and you're going to want to

**6:54** · search for the specific plugins that we

**6:56** · cover. So, I have DataView installed

**6:59** · here. I also have local images plus, as

**7:01** · well as terminal. So, the terminal one

**7:03** · right here, you can actually use Claude

**7:05** · Code if you want in Obsidian if you

**7:07** · don't want to leave uh Obsidian

**7:09** · whatsoever. I personally usually prefer

**7:11** · using it in something like Cursor's

**7:14** · terminal or VS Code, and I have Obsidian

**7:17** · and my actual IDE open at the same time.

**7:20** · So, here you can see we have that same

**7:21** · Claude blog post that we just saved into

**7:24** · our Obsidian, and I'm going to say to

**7:25** · Claude, compile, and then I'm linking to

**7:28** · that specific uh blog post right here,

**7:30** · that markdown file, compile this one

**7:32** · into the wiki. That's all I'm going to

**7:34** · say, and Claude's just going to do its

**7:35** · magic. It's going to take maybe uh 30

**7:38** · seconds to a minute, depending on how

**7:39** · much you're compiling, and it's going to

**7:41** · actually go about the process. So, watch

**7:43** · what happens. It's going to read the

**7:44** · article, it's going to identify the core

**7:46** · topics, going to decide what needs its

**7:48** · own concept page. If the topic doesn't

**7:50** · exist yet, it's going to then write the

**7:52** · summary, it's going to write a key

**7:54** · takeaway section, it's going to add

**7:56** · inbound and outbound wiki links, and

**7:58** · then it's going to update the topic

**7:59** · index, and it's also going to update the

**8:01** · master index, and then it's going to log

**8:04** · the entry. All from one simple command,

**8:06** · which, of course, is powered by our

**8:08** · claude.md file. So, before Claude Code,

**8:10** · Obsidian was kind of like a big scary

**8:12** · tool for a lot of people because you

**8:13** · have to do all these different things,

**8:15** · backlinks. It was great for bookkeeping

**8:17** · your notes and knowledge, but it's

**8:19** · something that humans aren't really

**8:20** · going to do, and they're just going to

**8:21** · abandon, you know, 15 edits across eight

**8:23** · files from one source, you would never

**8:25** · personally do this manually, but Claude

**8:27** · Code does this for us in 30 seconds, and

**8:29** · it's easy as that. So, if you start

**8:31** · building this up, you do it 10 times,

**8:32** · you start to have a real knowledge base,

**8:34** · and if you do it maybe like 100 times or

**8:35** · a couple hundred times, you know, the

**8:37** · graph view is going to start looking

**8:38** · like actual research. And boom, it's

**8:40** · done. You can see we have a new topic,

**8:42** · which is agent design patterns with five

**8:44** · articles. So, we have three key

**8:46** · patterns, composable general tools,

**8:49** · progressive context management, prompt

**8:51** · caching strategies, and declarative tool

**8:53** · designs. You can see it also updated the

**8:55** · master index, the log.md, plus added

**8:58** · backlinks with a total of 11 files

**9:00** · touched. And like I said, the template

**9:02** · that I'm providing you for free with

**9:04** · this entire knowledge system comes with

**9:05** · a complete claude.md file, and this is

**9:08** · really what makes this system work. But

**9:10** · you can, of course, customize this if

**9:11** · you want to change the system for your

**9:13** · specific flow. You can see here, it

**9:15** · starts off saying, "You are the

**9:16** · librarian of this vault. The wiki

**9:18** · {slash} folder is your domain. You

**9:21** · write, you maintain every file in this

**9:23** · wiki. The human rarely edits wiki files

**9:25** · directly." Now, this basically is

**9:27** · defining the ownership. Without it,

**9:29** · Claude Code treats wiki files like any

**9:30** · other file and starts deferring to

**9:32** · whatever it sees there. But with it,

**9:34** · it's going to start taking

**9:35** · responsibility and write these pages

**9:36** · confidently with new source conflicts.

**9:39** · So, you can see here for ingest, read

**9:40** · the raw file in full, identify the core

**9:42** · topic or topics, check wiki master index

**9:45** · for matching topic folder. If the topic

**9:48** · exists, update or extend the relevant

**9:50** · articles and add backlinks from touched

**9:52** · pages. If the topic does not exist,

**9:54** · create a new folder under wiki with a

**9:56** · lowercase hyphenated name and create a

**9:59** · underscore index.md inside of it. Every

**10:01** · wiki article must include a top level

**10:04** · title, source which is path to raw md

**10:07** · file line, a two to four sentence intro

**10:10** · paragraph, a key takeaway section with

**10:12** · bullet points, a related section with

**10:14** · wiki links to three to eight related

**10:16** · pages, update the topic underscore

**10:18** · index.md,

**10:20** · update the wiki master index if a new

**10:22** · topic was created, append one line to

**10:25** · wiki.log.md

**10:27** · if the source spans multiple topics

**10:28** · create articles in both and cross link.

**10:32** · We have about 10 steps here and the

**10:33** · model's going to follow them in order

**10:35** · every single time because this file in

**10:37** · the cloud.md tells it what to do and

**10:39** · it's loaded in every single conversation

**10:41** · so you won't have to prompt it again.

**10:43** · Next we have the query section so this

**10:44** · is triggered when the human asks a

**10:45** · question so read wiki master index first

**10:48** · then read the matching topic index.md,

**10:51** · read one to three specific articles in

**10:53** · full, synthesize the answer with

**10:55** · citations, and then offer to file

**10:58** · substantial answers as new wiki

**10:59** · articles. So three to four file reads to

**11:02** · answer any question. No vectors, no

**11:05** · embeddings, no cosine similarity, BM25,

**11:08** · the index file is the retrieval here and

**11:11** · that's because the model maintains it

**11:13** · for you. All right, so next is the lint

**11:15** · which is the health check. So live is

**11:16** · the append only record and we're going

**11:18** · to run both the query and the lint live

**11:20** · in just a second and you can see here

**11:22** · this is going to be triggered simply by

**11:23** · just saying the word lint or audit the

**11:25** · wiki. It's basically going to read every

**11:27** · file in the wiki and produce a report

**11:29** · covering contradictions, stale claims,

**11:32** · orphan pages, missing concepts, missing

**11:34** · cross links, unsourced claims, and

**11:37** · suggested new articles and then output

**11:39** · the report to output-lint-report

**11:42** · and then the date here and then wait for

**11:43** · approval before fixing. And then for log

**11:45** · every operation appends one line to the

**11:48** · wiki.log.md in this

**11:51** · time, operation, short description, and

**11:53** · then the files touched. And this is

**11:54** · append only it never rewrites existing

**11:57** · lines. And then we have conventions so

**11:59** · things like citations are required every

**12:01** · wiki article includes source line, key

**12:03** · takeaway section is required on every

**12:05** · article, file names are lower case

**12:07** · hyphenated, use wiki links for every

**12:10** · cross reference, bullets over

**12:11** · paragraphs, never invent claims, flag

**12:14** · gaps and open questions, and then flag

**12:16** · contradictions when found. And then when

**12:18** · the human asks something outside of the

**12:19** · rules ask a clarifying question, do not

**12:22** · silently invent a new operation. So the

**12:24** · citation rule right here is the

**12:25** · hallucination fix. Every article has to

**12:28** · name the raw file it came from. If the

**12:30** · model writes something that the source

**12:31** · doesn't say that in the next lint pass

**12:33** · catches it. And that's how we're going

**12:35** · to keep this wiki honest at scale. And

**12:37** · that's literally the entire system. It's

**12:38** · essentially a 60 line or so cloud.md

**12:41** · markdown file. And this essentially is

**12:43** · the brain of the entire system and

**12:45** · that's why I went through it for you

**12:46** · guys because it's very important for you

**12:48** · guys to know it. Now just so you guys

**12:49** · know in our template we do have some

**12:51** · additional things that Karpathy doesn't

**12:53** · even cover and that I just felt did add

**12:55** · value to this system so I'll quickly go

**12:57** · over them. We also have an AI-research

**13:00** · folder. So this is the AI's research

**13:02** · folder. So you're going to see in a

**13:04** · second yes we can ingest manually

**13:06** · through the means I just showed you with

**13:08** · the Obsidian Clipper or just you know

**13:10** · scraping our own podcast transcripts or

**13:12** · whatever the case is from different

**13:14** · sources. You can also get Claude code of

**13:16** · course to conduct autonomous research on

**13:18** · the web and save the full clean source

**13:20** · content into this folder as markdown

**13:22** · files. And you'll see here we're telling

**13:24** · Claude that it can write to this folder.

**13:27** · And files here are immutable once saved,

**13:29** · do not overwrite, create new files. And

**13:31** · this separates human curated sources

**13:33** · which are in the raw folder from AI

**13:36** · discovered sources which are in the AI

**13:38** · research folder. And you'll see research

**13:39** · is triggered when the human asks you to

**13:41** · research a topic or when a query reveals

**13:43** · gaps the wiki cannot answer from

**13:45** · existing sources. What it's going to do

**13:47** · is search the web for relevant high

**13:49** · quality sources on this topic and then

**13:51** · for each source found save the full

**13:53** · clean content not a summary as markdown

**13:56** · files in this folder. You can see the

**13:57** · format here and we're basically just

**13:59** · giving it some additional stuff for the

**14:01** · format that it's saving it as. So in the

**14:03** · doc here if you want to see more in

**14:04** · depth stuff such as the folder

**14:06** · structure, the page templates, entity

**14:08** · page templates that we have within the

**14:09** · system as well as the concept page

**14:11** · template, the source summary template,

**14:13** · you can see all that there. But we're

**14:15** · just going to move on to the query

**14:16** · pattern. So there's really three types

**14:18** · of queries that work well against the

**14:19** · wiki built this way. The first is the

**14:22** · direct lookup. We have direct lookup,

**14:24** · cross topic synthesis, and file back

**14:27** · synthesis. I'm going to run all three

**14:28** · against this vault that already has

**14:30** · about 10 plus articles as well as

**14:32** · transcripts from some of my YouTube

**14:33** · videos inside of it. All right, so I'm

**14:35** · actually just going to use the Obsidian

**14:36** · terminal right here but you can use

**14:38** · either or the IDE with cursor, VS code,

**14:41** · whatever the case is. I'm just going to

**14:42** · say what are the key points from my

**14:45** · cloud.md video. And you can see here I

**14:47** · have my YouTube transcripts which

**14:48** · includes the cloud.md video. So this is

**14:50** · a direct query. You can see here let me

**14:52** · find the relevant raw files and query

**14:54** · the wiki for additional coverage.

**14:56** · There's a wiki article specifically

**14:58** · about cloud.md best practices. And boom

**15:00** · here you can see this is exactly what I

**15:03** · covered in that video. If you didn't

**15:04** · haven't watched that video I definitely

**15:05** · suggest you to go watch it. We covered

**15:08** · two different research papers right

**15:09** · here. Why Claude ignores your

**15:11** · instructions, the fix so six different

**15:14** · sections right here, and then some

**15:16** · practical tips.

**15:17** · All right, so that's the first query

**15:18** · direct lookup. Next is the cross topic

**15:21** · synthesis. So I'm going to ask what

**15:23** · techniques are mentioned across multiple

**15:25** · videos. You can see here nine videos

**15:27** · across 11 topics. Let me read the topic

**15:29** · indexes to trace which videos feed into

**15:31** · which articles then identify overlapping

**15:34** · techniques. And boom here we got our

**15:36** · answers. So we can see technique number

**15:38** · one context/token management so that's

**15:40** · from videos one, two, three, four, five.

**15:43** · And we can see what it pulled there and

**15:44** · then we can see technique two prompt

**15:46** · caching from videos one, three, and

**15:47** · four.

**15:48** · And then we can see number three

**15:50** · composable general tools over task

**15:52** · specific tools video three, four, and

**15:54** · nine. And then dead weight pruning,

**15:56** · reevaluate assumptions videos two and

**15:59** · three, and then cost monitoring and

**16:01** · mitigation videos one, five, and nine,

**16:03** · security boundaries, and then persistent

**16:06** · always on agents. All right, so query

**16:07** · three file back synthesis. So this is

**16:10** · where the answer becomes a new wiki.

**16:12** · Basically the cool thing about this is

**16:13** · the exploration compounds into new

**16:16** · knowledge in your knowledge base. So

**16:18** · here we're saying based on everything in

**16:19** · the wiki what are the main approaches to

**16:22** · long-term memory for AI agents. Save

**16:25** · your answer as a new wiki article and

**16:27** · cross link in the sources you

**16:29** · referenced. And boom you can see here it

**16:30** · is now done so here's what it created a

**16:32** · new article right here. It's under the

**16:35** · wiki agent design patterns and we have

**16:37** · long-term memory approaches so you can

**16:39** · see this whole entire document right

**16:42** · here. You can see it has links to

**16:43** · related documents right here so you

**16:45** · could see multbook VPS setup, AI

**16:48** · workflow builder, cloud.md best

**16:50** · practices. So we can see it synthesizes

**16:52** · four approaches from across this wiki so

**16:55** · memory folders, compaction, structured

**16:58** · config files, external rag. The

**17:00** · overarching finding simpler model native

**17:03** · memory is replacing external

**17:04** · infrastructure as models get more

**17:06** · capable which we're kind of seeing right

**17:08** · here in front of our eyes with this

**17:10** · system. Now this query is great because

**17:12** · everything you ask adds value to the

**17:14** · system. You never lose a good answer to

**17:16** · chat history like you may have in the

**17:17** · past and this is the part that turns a

**17:20** · knowledge base into a research partner.

**17:23** · All right, so next we're going to do the

**17:24** · AI research query. So this is basically

**17:26** · a query that the AI shouldn't have

**17:28** · access to within the current knowledge

**17:30** · base. So I'm going to ask it research

**17:32** · what QMD is and how it works as a

**17:35** · research layer on top of markdown wikis.

**17:38** · Save what you find to AI research. You

**17:40** · can see here it is doing its research.

**17:42** · It's running the fetch multiple

**17:43** · different times for different things

**17:45** · right here. If you don't know about QMD

**17:47** · I'll dive deeper into this in future

**17:49** · videos. We do mention it in the resource

**17:51** · down below. This is a tool for BM25 rag

**17:54** · which is created by Toby who is the

**17:57** · founder of Shopify. Okay, and boom you

**17:59** · can see that it saved the different

**18:00** · research in our AI research folder right

**18:03** · here and you can see over here in our

**18:05** · knowledge search wiki we have QMD right

**18:08** · here and we can see all the different

**18:10** · stuff about it BM25, vector semantic,

**18:13** · hybrid plus re-ranking. Really cool

**18:15** · stuff and just to go over one more time

**18:17** · each wiki has its own index so we can

**18:20** · see all the different stuff within this

**18:22** · wiki right here. So QMD overview,

**18:24** · indexing and chunking, MCP integration.

**18:27** · And we have that for every single wiki

**18:29** · with its own index and then we have the

**18:30** · master index which links to each

**18:33** · specific wiki. So this is sort of like

**18:35** · progressive disclosure. This is exactly

**18:37** · progressive disclosure like we talk

**18:38** · about in some of our other videos. I

**18:40** · talked about it in the cloud markdown

**18:42** · video as well. This is how skills work.

**18:44** · We're giving it a short description

**18:46** · right here for each specific wiki and

**18:48** · then it's able to distinguish which wiki

**18:51** · it should actually go to based on this

**18:52** · description. And then once it's in this

**18:54** · wiki we can see as well another index

**18:58** · for the specific wiki where it has a

**18:59** · description for each specific article.

**19:01** · All right, so at this point if you

**19:02** · stopped right now you'd have a full

**19:04** · working system but in the next few

**19:05** · minutes I'm going to show you how to

**19:06** · actually keep this system healthy at

**19:09** · 100, 200, or 300 articles. So now all

**19:12** · I'm going to do is just simply run lint.

**19:14** · And once again the lint operation it

**19:16** · basically reads every file in this wiki,

**19:19** · cross references them, and returns a

**19:20** · report. So contradictions, stale claims,

**19:24** · orphan pages, missing cross links,

**19:26** · unsourced claims, all these things that

**19:28** · you know humans as us may miss this is

**19:30** · going to be able to detect. And now we

**19:32** · can see it's going to work. All right,

**19:34** · and boom the lint is complete so we can

**19:36** · see our report is saved right here in

**19:38** · the output folder.

**19:40** · So we can see here we had no

**19:41** · contradictions, no stale claims, no

**19:44** · orphan pages, but we did have six

**19:46** · missing cross links, three unsourced

**19:49** · claims, and then five suggested

**19:51** · articles. And in this report, we can see

**19:53** · all the different details for each

**19:54** · specific one. And then we can see here

**19:56** · it's waiting for our approval before it

**19:58** · actually applies those fixes. So I'm

**20:00** · going to go ahead and say I approve. All

**20:02** · right, and boom, we can see that all the

**20:03** · fixes are applied. So run this weekly or

**20:06** · after any big ingest batch. This will

**20:08** · take 5 to 10 minutes, give or take, give

**20:10** · you a healthy wiki and a log entry so

**20:13** · you can know when you last ran it. Now

**20:15** · the question everyone's been asking is

**20:16** · whether this actually replaces Vector

**20:19** · Rag. And the honest answer is below 500

**20:22** · articles or so, this wiki wins on four

**20:25** · or five factors. So on infrastructure,

**20:28** · Vector Rag needs a database and an

**20:30** · embedding model, you need hosting. It's

**20:33** · a lot more complex where the wiki is

**20:34** · literally just a folder of markdown

**20:36** · files. So the wiki wins in terms of

**20:39** · simplicity and setup time. Vector Rag

**20:41** · may take a few hours to maybe even a

**20:43** · couple days depending on how complex the

**20:45** · setup is. So the wiki wins with

**20:48** · literally just a 15-minute setup. You

**20:50** · can literally set it up and have it

**20:51** · fully running by the time you're done

**20:53** · watching this video. Now for scale,

**20:54** · there is a ceiling. So Vector Rag

**20:57** · handles millions of chunks. The wiki

**20:59** · starts breaking down past maybe 500 or a

**21:02** · few thousand articles. So in that case,

**21:05** · Vector is going to win. And this here is

**21:07** · one of the axes that actually matters.

**21:09** · Next for human browsability, Vector Rag

**21:12** · is literally just a black box. So the

**21:14** · wiki is a set of pages that you can read

**21:17** · and navigate and you can view in a nice

**21:19** · GUI interface like Obsidian. So in that

**21:21** · case, the wiki wins. And the cool thing

**21:23** · is with the wiki, outputs compound. With

**21:25** · Vector Rag, the chat is ephemeral. So

**21:27** · wiki queries file back as new articles.

**21:30** · So in this case, the wiki would win. So

**21:31** · four out of five below 500 sources, the

**21:34** · wiki wins. Above that, a hybrid approach

**21:37** · makes sense. So wiki for structured

**21:40** · synthesis and Vector for semantic

**21:42** · fallback across long-tail retrieval. Now

**21:44** · this could change as models progress and

**21:46** · whatnot, but that's also why I reference

**21:49** · QMD which you can definitely take a look

**21:51** · at and I'll do more videos talking about

**21:53** · QMD and showing you guys how to actually

**21:55** · use it, but it is linked in the

**21:56** · resources well. Now you could also use

**21:58** · other vector or embedding strategies

**22:00** · besides QMD, but that's just one I'm

**22:02** · referencing here. There's a few

**22:03** · objections that have been coming up

**22:04** · every time people have been posting this

**22:06** · on X and whatnot and let me handle some

**22:08** · of them directly here for you guys. So

**22:09** · the first objection is scale. So we

**22:11** · talked about this already, but just as a

**22:13** · baseline, the wiki starts breaking at

**22:15** · around 500 articles because the index

**22:17** · stops being a reliable navigation layer.

**22:19** · Similar to when you bloat Claude Code

**22:21** · with too many different skills, you will

**22:23** · start to see some degradation in

**22:25** · quality. Now above that, you either want

**22:26** · to split it into multiple topic specific

**22:28** · vaults or you would want to bolt on a

**22:31** · small search tool over the markdown

**22:33** · files. Like I said, I'm linking to QMD

**22:35** · which is the same search tool that

**22:36** · Karpathy actually uses, so that will be

**22:38** · in the doc. And you probably won't hit a

**22:39** · ceiling for quite a while depending on

**22:41** · what your usage is with your actual

**22:42** · vault, but then you may want to actually

**22:44** · scale it and look at some of these other

**22:46** · methods. So either a different vault or

**22:49** · a hybrid strategy using something like

**22:51** · QMD. The next objection is

**22:53** · hallucinations. This is huge when

**22:54** · dealing with really anything with AI

**22:56** · models. So if the model writes a wiki

**22:58** · page that drifts from the actual source,

**23:01** · the error propagates into every future

**23:03** · query. So it's essentially like a virus.

**23:05** · So the fix for this is that Claude.md

**23:08** · file and that's why we took a deep look

**23:10** · at it so you have an understanding how

**23:12** · this actually works. Now every article

**23:14** · sites the raw file that it came from. So

**23:16** · every lint pass that you do in future,

**23:19** · checks those citations against the

**23:21** · actual sources. Flags anything that's

**23:23** · unsourced, it reviews it, corrects it.

**23:26** · Now this is not automatic safety, but it

**23:28** · is a maintenance loop for the model that

**23:30** · runs for you. And like I said guys, this

**23:31** · entire document breaking down everything

**23:33** · that we covered in depth as well as some

**23:35** · additional things that you can read

**23:36** · through and our complete Karpathy

**23:38** · Obsidian Vault Starter Kit is available

**23:41** · for free in our school community, Stride

**23:43** · AI Academy. So make sure to check that

**23:45** · out. It's 100% for free to join, no

**23:47** · paywall or anything like that. And you

**23:49** · can network with myself as well as other

**23:51** · like-minded AI entrepreneurs,

**23:53** · enthusiasts. We have some really cool

**23:54** · people in there and I'm excited to

**23:55** · continue building this community with

**23:57** · you guys. So that's pretty much it for

**23:58** · this video guys. I hope you guys got

**24:00** · some value from this. I definitely tried

**24:01** · to explain everything and be as in-depth

**24:04** · as possible because I know on the

**24:05** · surface just reading his tweet, it's

**24:08** · maybe a little bit difficult to

**24:09** · understand. So I wanted to cover

**24:10** · everything and show you the exact

**24:11** · process and literally just give you the

**24:13** · starter kit so you can get going with

**24:15** · this as soon as possible because it is

**24:17** · very valuable when you start using

**24:19** · Claude Code with something like Obsidian

**24:21** · and you actually start managing your

**24:23** · second brain in an efficient way.

**24:26** · Now I've personally been using Obsidian

**24:27** · probably for about the last four to five

**24:30** · months. I have a few different vaults

**24:32** · that I've been using and it's helped me

**24:33** · tremendously on many different facets

**24:36** · from content creation, business,

**24:38** · personal life, really anything for

**24:40** · knowledge management. And I'm excited to

**24:42** · share more about my custom Obsidian

**24:44** · Vaults in the future. So if you want to

**24:45** · stay up-to-date with that as well as

**24:47** · Claude Code tutorials, AI tutorials,

**24:49** · make sure to like this video, comment

**24:50** · down below your thoughts. If I missed

**24:52** · anything or if you have any insights or

**24:54** · ideas about this Obsidian Vault or

**24:56** · Karpathy or really just anything about

**24:58** · Claude Code and this video in general,

**25:00** · let me know on down below and stay tuned

**25:02** · for future uploads because I plan on

**25:04** · giving you guys a immense amount of

**25:05** · value on this channel. So if you're new

**25:07** · here, smash that subscribe button to

**25:08** · stay up-to-date, join the Stride AI

**25:10** · Academy down below. And I hope you guys

**25:12** · have an amazing week. I will see you in

**25:13** · the next video guys. Keep hustling, keep

**25:15** · grinding and of course guys, accelerate

**25:17** · your stride. Take care.
