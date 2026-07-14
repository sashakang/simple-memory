---
title: "Claude Built the Ultimate Second Brain"
source: "https://www.youtube.com/watch?v=cwf2vEAigKA"
author:
  - "[[Wes Roth]]"
published: 2026-07-14
created: 2026-07-14
description: "Second-brain / LLM-wiki walkthrough: Obsidian as local-first markdown store, raw/wiki split, graph view, ingest flow, Kanban, and AI-generated outputs."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=cwf2vEAigKA)

The guide to building a "second brain" (give it to your chatbot)
https://natural20.com/using-claude-code-to-setup-a-second-brain-aka-llm-wiki

Video walkthrough of a Karpathy-style LLM Wiki / second-brain system using Obsidian, Claude Code (or Codex/ChatGPT-class tools), ingest flow, graph view, Kanban, and output generation.

Timestamps:
00:00 LLM Wiki aka "Second Brain"
05:38 tour of the "Second Brain"
16:23 Obsidian
19:06 Ingesting New Info
21:20 Kanban Board
26:26 the final "output"
29:56 How to Build This

## Transcript

**0:00** · So this is my second brain. It holds all the knowledge that I have. Everything

**0:04** · the knowledge that I have. Everything about YouTube videos, everything about

**0:07** · about YouTube videos, everything about AI labs, the latest papers, even my

**0:09** · AI labs, the latest papers, even my sponsors. Everything that I know gets

**0:11** · sponsors. Everything that I know gets automatically logged, connected, and

**0:14** · automatically logged, connected, and summarized for me in my second brain.

**0:17** · summarized for me in my second brain. And I didn't write most of it anywhere

**0:19** · And I didn't write most of it anywhere really. The AI did. And as it slowly

**0:22** · really. The AI did. And as it slowly aggregates all the information, it's

**0:23** · aggregates all the information, it's able to parse it. and I'm able to ask it

**0:26** · able to parse it. and I'm able to ask it a question and get immediate answers

**0:28** · a question and get immediate answers based on my context and all of the data

**0:31** · based on my context and all of the data that I have access to. For example,

**0:33** · that I have access to. For example, these little clusters here are different

**0:35** · these little clusters here are different YouTube creators. For example, this node

**0:37** · YouTube creators. For example, this node is me. It connects me to all of my

**0:40** · is me. It connects me to all of my videos, the various topics that I've

**0:42** · videos, the various topics that I've talked about, all my content and

**0:43** · talked about, all my content and performance on YouTube, on X

**0:45** · performance on YouTube, on X newsletters, etc. Here's an example of

**0:47** · newsletters, etc. Here's an example of how I would use it. So, here's Cloud

**0:49** · how I would use it. So, here's Cloud Code, the desktop app. Recently, I've

**0:51** · Code, the desktop app. Recently, I've started using the desktop app for pretty

**0:53** · started using the desktop app for pretty much everything. Before, I was running

**0:54** · much everything. Before, I was running most of my stuff in the command line

**0:56** · most of my stuff in the command line interface. Now, it's pretty much all

**0:58** · interface. Now, it's pretty much all here. So, I'm going to ask it based on

**1:00** · here. So, I'm going to ask it based on the data we have available. What topics

**1:01** · the data we have available. What topics haven't I covered that are very popular

**1:03** · haven't I covered that are very popular in the AI sphere? And here's the answer.

**1:05** · in the AI sphere? And here's the answer. Grock, Deepseek, Copilot, Codeex, etc.

**1:08** · Grock, Deepseek, Copilot, Codeex, etc. It's taking into account the velocity of

**1:10** · It's taking into account the velocity of the different videos, kind of which

**1:12** · the different videos, kind of which topics are trending right now, and

**1:14** · topics are trending right now, and pulling from the entire database to

**1:16** · pulling from the entire database to provide the best possible answer. So

**1:18** · provide the best possible answer. So does this from its own notes. The notes

**1:20** · does this from its own notes. The notes that it wrote and that it keeps updated

**1:23** · that it wrote and that it keeps updated every single day. It knows my sponsor

**1:25** · every single day. It knows my sponsor deadlines better than I do. And it keeps

**1:27** · deadlines better than I do. And it keeps track of a million different things that

**1:29** · track of a million different things that I could not possibly keep track of. This

**1:32** · I could not possibly keep track of. This whole idea came from one of the most

**1:33** · whole idea came from one of the most respected names in AI, and that is Andre

**1:36** · respected names in AI, and that is Andre Karpathy. And by the end of this video,

**1:38** · Karpathy. And by the end of this video, you'll know exactly what to do to build

**1:40** · you'll know exactly what to do to build your own. I also had to create some

**1:42** · your own. I also had to create some slides for me so I can do this

**1:43** · slides for me so I can do this presentation without losing track of

**1:45** · presentation without losing track of what I'm talking about. So, first and

**1:47** · what I'm talking about. So, first and foremost, what is a second brain? This

**1:50** · foremost, what is a second brain? This idea has been around for some time. It

**1:51** · idea has been around for some time. It went by many different names, but the

**1:53** · went by many different names, but the core idea was how do we get all the

**1:55** · core idea was how do we get all the stuff that we're dealing with, all the

**1:56** · stuff that we're dealing with, all the little notes and ideas and the to-do

**1:58** · little notes and ideas and the to-do lists and meeting minutes and just

**2:00** · lists and meeting minutes and just everything, everything everything, how

**2:02** · everything, everything everything, how do we sort of collect it all, then

**2:03** · do we sort of collect it all, then organize it all and have it available

**2:06** · organize it all and have it available for when it's actually actionable. And

**2:08** · for when it's actually actionable. And back in the days, you would write it

**2:09** · back in the days, you would write it down in a notebook and you'd hope that

**2:11** · down in a notebook and you'd hope that that page was there when you needed it.

**2:13** · that page was there when you needed it. Apps improved it a little bit. You could

**2:15** · Apps improved it a little bit. You could write things down. you can save it. All

**2:16** · write things down. you can save it. All of us at some point had some system for

**2:19** · of us at some point had some system for the intake of all the information that

**2:21** · the intake of all the information that life throws at us. But just saving

**2:24** · life throws at us. But just saving information, hoarding it, you know, all

**2:25** · information, hoarding it, you know, all the bookmarks you have saved in X, that

**2:28** · the bookmarks you have saved in X, that was never really the problem. The

**2:29** · was never really the problem. The problem was trying to maintain it,

**2:31** · problem was trying to maintain it, trying to stay on top of it and using it

**2:34** · trying to stay on top of it and using it when you needed to use it, having that

**2:35** · when you needed to use it, having that information available to you when you

**2:38** · information available to you when you need it. So the first brain, the one in

**2:40** · need it. So the first brain, the one in your skull right now, gently floating

**2:42** · your skull right now, gently floating there, it's great at thinking. It's

**2:45** · there, it's great at thinking. It's terrible at storing and organizing. We

**2:48** · terrible at storing and organizing. We forget most of the things that we're

**2:49** · forget most of the things that we're supposed to do, most of the things that

**2:51** · supposed to do, most of the things that we read. There's some very small

**2:53** · we read. There's some very small percentage of the population that have

**2:54** · percentage of the population that have amazing memory and they just remember

**2:56** · amazing memory and they just remember everything where they need to. And you

**2:57** · everything where they need to. And you know, hooray for them, but that's not

**3:00** · know, hooray for them, but that's not most of us. And then we got LMS. And

**3:03** · most of us. And then we got LMS. And then these LMS got good. And we're now

**3:06** · then these LMS got good. And we're now at a point where that LM, well, it can

**3:09** · at a point where that LM, well, it can be a librarian for all the data that you

**3:12** · be a librarian for all the data that you have. So you just throw all of your

**3:14** · have. So you just throw all of your notes and data and recordings and

**3:16** · notes and data and recordings and everything everything everything into

**3:17** · everything everything everything into this vault. Some of it you do manually.

**3:19** · this vault. Some of it you do manually. Some of it you set up various collection

**3:21** · Some of it you set up various collection processes for that. So it's done

**3:22** · processes for that. So it's done automatically. But you just throw it in

**3:24** · automatically. But you just throw it in the vault. The librarian, this AI, it

**3:27** · the vault. The librarian, this AI, it reads everything. It files it correctly.

**3:29** · reads everything. It files it correctly. It puts it on the right shelf, so to

**3:31** · It puts it on the right shelf, so to speak. It connects all those things in

**3:34** · speak. It connects all those things in some way that makes sense. Some things

**3:36** · some way that makes sense. Some things you might need for work, some things you

**3:38** · you might need for work, some things you might need for the house, for what I'm

**3:40** · might need for the house, for what I'm doing. I like to organize it by topic

**3:42** · doing. I like to organize it by topic clusters and this AI it keeps all that

**3:44** · clusters and this AI it keeps all that information tidy every day forever on

**3:47** · information tidy every day forever on autopilot. So the idea I got to give

**3:49** · autopilot. So the idea I got to give credit to Andre Karpathy. So he called

**3:51** · credit to Andre Karpathy. So he called it the LM wiki and before that it was

**3:53** · it the LM wiki and before that it was called the second brain. Before that

**3:55** · called the second brain. Before that there was a book called getting things

**3:56** · there was a book called getting things done the GTD system and it goes back

**3:59** · done the GTD system and it goes back even even further. In fact this original

**4:01** · even even further. In fact this original idea predates LMS. It predates even

**4:05** · idea predates LMS. It predates even computers. This idea of a machine that

**4:07** · computers. This idea of a machine that organizes all of your thoughts and ideas

**4:09** · organizes all of your thoughts and ideas that comes from 1945. So as Andre

**4:12** · that comes from 1945. So as Andre Karpathy said, Obsidian is the IDE. So

**4:14** · Karpathy said, Obsidian is the IDE. So the ID is your development environment.

**4:16** · the ID is your development environment. It's kind of where you shape software,

**4:18** · It's kind of where you shape software, where you build software. If you're not

**4:19** · where you build software. If you're not familiar with Obsidian, don't worry, you

**4:21** · familiar with Obsidian, don't worry, you will be. And I think you're going to

**4:23** · will be. And I think you're going to like it. It's free. Then the LM is the

**4:25** · like it. It's free. Then the LM is the programmer. That's the thing that goes

**4:27** · programmer. That's the thing that goes in there and manipulates things and

**4:29** · in there and manipulates things and builds things and creates structure. And

**4:31** · builds things and creates structure. And the wiki is the codebase. So in plain

**4:33** · the wiki is the codebase. So in plain English, Obsidian, that's this app. Just

**4:35** · English, Obsidian, that's this app. Just think of it like a notebook. It's this

**4:36** · think of it like a notebook. It's this app that you look through to see your

**4:38** · app that you look through to see your notes. Then we have the LM, the AI. It

**4:41** · notes. Then we have the LM, the AI. It writes the pages, interlinks them, and

**4:43** · writes the pages, interlinks them, and keeps them updated. And the wiki becomes

**4:45** · keeps them updated. And the wiki becomes sort of the product, the codebase. It's

**4:47** · sort of the product, the codebase. It's the thing from which you draw all the

**4:49** · the thing from which you draw all the insights and the knowledge. It's a

**4:51** · insights and the knowledge. It's a growing library of interconnected pages.

**4:54** · growing library of interconnected pages. Your job is to make sure that it's

**4:55** · Your job is to make sure that it's getting fed with the various raw data

**4:58** · getting fed with the various raw data that you want in there. And then on the

**4:59** · that you want in there. And then on the other side, you ask it questions or you

**5:02** · other side, you ask it questions or you have it deliver the insights to you in

**5:04** · have it deliver the insights to you in some scheduled manner. Here's the thing,

**5:06** · some scheduled manner. Here's the thing, humans, we've been dreaming about this

**5:07** · humans, we've been dreaming about this for a long, long time. This dream is 80

**5:10** · for a long, long time. This dream is 80 years old. Someone named Venevver Bush

**5:13** · years old. Someone named Venevver Bush thought of this in 1945. He originally

**5:15** · thought of this in 1945. He originally called it the Mimics. Mimics meme X

**5:18** · called it the Mimics. Mimics meme X sounds cooler, I got to say. So, it's

**5:20** · sounds cooler, I got to say. So, it's basically a desk that recorded

**5:22** · basically a desk that recorded everything you've ever read with trails

**5:24** · everything you've ever read with trails connecting related ideas. So, we had

**5:26** · connecting related ideas. So, we had that idea 80 years ago. We just never

**5:27** · that idea 80 years ago. We just never had anything capable of maintaining this

**5:30** · had anything capable of maintaining this database, making it useful on autopilot.

**5:32** · database, making it useful on autopilot. We do now. It's large language models.

**5:35** · We do now. It's large language models. It's Chad GPT, Grock, Gemini, Claude,

**5:38** · It's Chad GPT, Grock, Gemini, Claude, you name it. All right, so first and

**5:39** · you name it. All right, so first and foremost, what is Obsidian? Obsidian is

**5:42** · foremost, what is Obsidian? Obsidian is a pretty simple app that has been built

**5:44** · a pretty simple app that has been built on a radical idea. This is going to blow

**5:47** · on a radical idea. This is going to blow your mind. You know, like all your notes

**5:48** · your mind. You know, like all your notes and the stuff you write down. What if

**5:51** · and the stuff you write down. What if instead of you putting it on somebody

**5:53** · instead of you putting it on somebody else's computer like the cloud somewhere

**5:55** · else's computer like the cloud somewhere some large enterprise what if bear with

**5:57** · some large enterprise what if bear with me here what if you just kept them all

**5:59** · me here what if you just kept them all on your computer like there your files

**6:02** · on your computer like there your files your data your notes what if they were

**6:04** · your data your notes what if they were just uh on your computer if Obsidian

**6:06** · just uh on your computer if Obsidian vanishes tomorrow all the stuff that you

**6:08** · vanishes tomorrow all the stuff that you have saved it's still there people call

**6:10** · have saved it's still there people call this local first software and it uses

**6:13** · this local first software and it uses something called markdown if you're

**6:14** · something called markdown if you're working for a lot of chatbots you you've

**6:16** · working for a lot of chatbots you you've probably heard about markdown so they're

**6:19** · probably heard about markdown so they're markdown files All right. So, that MD

**6:21** · markdown files All right. So, that MD extension like claude.m MD, skill.md,

**6:25** · extension like claude.m MD, skill.md, those are your markdown files. Markdown

**6:26** · those are your markdown files. Markdown files are super simple. They're

**6:28** · files are super simple. They're basically just text plus a few symbols

**6:32** · basically just text plus a few symbols that do something. You've probably seen

**6:34** · that do something. You've probably seen something like this, right? So, you just

**6:35** · something like this, right? So, you just type your text. If you want a heading,

**6:37** · type your text. If you want a heading, you just use one hashtag for heading

**6:40** · you just use one hashtag for heading one, the big one, or two hashtags or or

**6:42** · one, the big one, or two hashtags or or three for heading three. Two asterisks

**6:44** · three for heading three. Two asterisks around something makes it bold. One

**6:46** · around something makes it bold. One asterisk around it makes it italicized.

**6:48** · asterisk around it makes it italicized. and simple ways to add code blocks or

**6:50** · and simple ways to add code blocks or links, etc. It's super super simple. So,

**6:53** · links, etc. It's super super simple. So, a 10-year-old can learn this in 10

**6:55** · a 10-year-old can learn this in 10 minutes. So, this right here is

**6:57** · minutes. So, this right here is Obsidian. This is kind of what it looks

**6:59** · Obsidian. This is kind of what it looks like. And this is the graph view. It's

**7:02** · like. And this is the graph view. It's pretty cool. Kind of a way to visualize

**7:04** · pretty cool. Kind of a way to visualize all of the things, all the topic

**7:06** · all of the things, all the topic clusters, whatever you have saved in

**7:08** · clusters, whatever you have saved in there. Each one of these little dots is

**7:10** · there. Each one of these little dots is a file. So, for example, here's this

**7:12** · a file. So, for example, here's this cluster. Let's zoom in and see what this

**7:14** · cluster. Let's zoom in and see what this is. It's my sponsor content flow with my

**7:17** · is. It's my sponsor content flow with my sponsors. These sponsors are not real.

**7:20** · sponsors. These sponsors are not real. They're fake. I can't actually show you

**7:22** · They're fake. I can't actually show you the real data. So, I had cloud code come

**7:24** · the real data. So, I had cloud code come up with some fake data just to be able

**7:25** · up with some fake data just to be able to kind of showcase the idea. But this

**7:27** · to kind of showcase the idea. But this is more or less exactly the system that

**7:29** · is more or less exactly the system that I use to keep track of things. Each

**7:32** · I use to keep track of things. Each sponsor gets its own node and then all

**7:34** · sponsor gets its own node and then all the information that is needed is

**7:35** · the information that is needed is uploaded to that. Based on that, we work

**7:37** · uploaded to that. Based on that, we work out what needs to be done, when the due

**7:39** · out what needs to be done, when the due date is, any assets that I need to know

**7:42** · date is, any assets that I need to know about is in there. For me, it's kind of

**7:44** · about is in there. For me, it's kind of like homework. You know, if you think

**7:46** · like homework. You know, if you think back to the days you went to school, you

**7:47** · back to the days you went to school, you got homework and you know, you you hoped

**7:49** · got homework and you know, you you hoped that you remember about it and when the

**7:51** · that you remember about it and when the due date is. I had struggle with that.

**7:54** · due date is. I had struggle with that. Sometimes I would forget to write down

**7:55** · Sometimes I would forget to write down the due date. I would forget when things

**7:57** · the due date. I would forget when things were due. And sometimes I had trouble

**7:59** · were due. And sometimes I had trouble kind of like breaking up the work into

**8:01** · kind of like breaking up the work into manageable tasks so that slowly over

**8:03** · manageable tasks so that slowly over time you completed the project. So, if

**8:05** · time you completed the project. So, if you've ever had trouble with the same

**8:06** · you've ever had trouble with the same thing or paying the bills on time or

**8:08** · thing or paying the bills on time or filing some specific paperwork that you

**8:10** · filing some specific paperwork that you needed to file, that's sometimes

**8:12** · needed to file, that's sometimes referred to as the ADHD tax. And for a

**8:14** · referred to as the ADHD tax. And for a lot of people, this is a very real thing

**8:16** · lot of people, this is a very real thing that they struggle with on a daily

**8:18** · that they struggle with on a daily basis. If you're fortunate enough to be

**8:20** · basis. If you're fortunate enough to be able to afford an executive assistant or

**8:22** · able to afford an executive assistant or somebody that just like handles those

**8:23** · somebody that just like handles those things for you, that's great. For most

**8:25** · things for you, that's great. For most of us, there wasn't an easy solution for

**8:28** · of us, there wasn't an easy solution for most of our lives until recently. Now I

**8:30** · most of our lives until recently. Now I just have to find a way to get all those

**8:32** · just have to find a way to get all those important things and funnel them into my

**8:35** · important things and funnel them into my second brain. Then I work with my

**8:37** · second brain. Then I work with my favorite assistant cla code or Chad GBT

**8:40** · favorite assistant cla code or Chad GBT or whatever to then set up systems,

**8:42** · or whatever to then set up systems, automated systems that make sure that I

**8:44** · automated systems that make sure that I get notified, hey, this is coming up.

**8:46** · get notified, hey, this is coming up. Maybe you should start working on this.

**8:48** · Maybe you should start working on this. Also, I don't have to open five

**8:50** · Also, I don't have to open five different tabs and hunt for different

**8:52** · different tabs and hunt for different pieces of information all over the

**8:53** · pieces of information all over the place. Everything is connected. Let's

**8:55** · place. Everything is connected. Let's zoom out and I'll give you another

**8:56** · zoom out and I'll give you another example. For example, let's zoom over

**8:58** · example. For example, let's zoom over here. Each one of these things is a

**9:00** · here. Each one of these things is a paper or blog post from a FrontierI lab.

**9:02** · paper or blog post from a FrontierI lab. There's something that I've talked about

**9:04** · There's something that I've talked about in the previous videos that I might need

**9:06** · in the previous videos that I might need to talk about in the future. So, for

**9:07** · to talk about in the future. So, for example, there's a page about Alph Go

**9:09** · example, there's a page about Alph Go and Tree of Thoughts. Some of you might

**9:11** · and Tree of Thoughts. Some of you might have been following me from those days

**9:13** · have been following me from those days of years and years ago when we covered

**9:15** · of years and years ago when we covered tree of thoughts. Who remembers that?

**9:17** · tree of thoughts. Who remembers that? And all of these are interconnected and

**9:19** · And all of these are interconnected and they're linked. So, anything that has to

**9:21** · they're linked. So, anything that has to do with Meta AI or Demisabus or Sam

**9:23** · do with Meta AI or Demisabus or Sam Alman, they're all connected to each

**9:25** · Alman, they're all connected to each other through these nodes. If you're

**9:26** · other through these nodes. If you're wondering what this mess of a cloud is,

**9:29** · wondering what this mess of a cloud is, these are the various people that

**9:31** · these are the various people that publish about AI. For example, this is

**9:33** · publish about AI. For example, this is me. All those little purple lines point

**9:36** · me. All those little purple lines point to things that are connected to me. All

**9:37** · to things that are connected to me. All of my videos. Recently, I started

**9:39** · of my videos. Recently, I started cataloging some of my tweets, although I

**9:41** · cataloging some of my tweets, although I don't think this is hooked up to that

**9:42** · don't think this is hooked up to that yet. We're we're in the process of doing

**9:44** · yet. We're we're in the process of doing that. It also connects to topics that

**9:46** · that. It also connects to topics that I've talked about. So, when we ask the

**9:48** · I've talked about. So, when we ask the question like, "What topics haven't I

**9:51** · question like, "What topics haven't I talked about in the last whatever 6

**9:52** · talked about in the last whatever 6 months, it has all that data. It's not

**9:54** · months, it has all that data. It's not guessing. It's not going online and

**9:56** · guessing. It's not going online and searching. It knows all the data is

**9:59** · searching. It knows all the data is here. It also knows what everyone else

**10:00** · here. It also knows what everyone else is posting. And notice that goes to a

**10:03** · is posting. And notice that goes to a number of these lines here that connects

**10:05** · number of these lines here that connects all those videos, for example, to the

**10:08** · all those videos, for example, to the topics that they discuss to the

**10:10** · topics that they discuss to the analytics behind those videos to what

**10:12** · analytics behind those videos to what works, what doesn't. And these red dots

**10:14** · works, what doesn't. And these red dots here, that's what Claude decided to call

**10:17** · here, that's what Claude decided to call beats, like on the beat or my beat. By

**10:20** · beats, like on the beat or my beat. By the way, I have Claude naming a lot of

**10:21** · the way, I have Claude naming a lot of these things. So, some of them look a

**10:23** · these things. So, some of them look a little bit weird, like it decided to

**10:24** · little bit weird, like it decided to call something the armory. The armory is

**10:27** · call something the armory. The armory is all the things that it thinks I should

**10:29** · all the things that it thinks I should build. Things that would be useful and

**10:31** · build. Things that would be useful and helpful to me, but I need to sit down,

**10:33** · helpful to me, but I need to sit down, you know, plan it out, tell Fable or

**10:35** · you know, plan it out, tell Fable or whatever model I'm using to go ahead and

**10:37** · whatever model I'm using to go ahead and build it out. These are the things that

**10:39** · build it out. These are the things that are on that list. The priority board,

**10:40** · are on that list. The priority board, analytics, demon, x wide funnel,

**10:43** · analytics, demon, x wide funnel, packaging lab, first responder pipeline,

**10:45** · packaging lab, first responder pipeline, retention, minor, comment archive, clip

**10:48** · retention, minor, comment archive, clip engine. Now, if you're wondering what

**10:49** · engine. Now, if you're wondering what are these projects that they're talking

**10:50** · are these projects that they're talking about, for example, this is one of them.

**10:52** · about, for example, this is one of them. So, this is what we called the X data

**10:55** · So, this is what we called the X data ingestion engine. We're getting tons of

**10:57** · ingestion engine. We're getting tons of data from X/ Twitter about the

**10:59** · data from X/ Twitter about the performance of various tweets from my

**11:02** · performance of various tweets from my own account as well as some other

**11:03** · own account as well as some other people's accounts. So, step one was to

**11:05** · people's accounts. So, step one was to build the engine, sort of the data

**11:07** · build the engine, sort of the data collection engine. By the way, if you're

**11:09** · collection engine. By the way, if you're wondering, oh, are you going to show us

**11:10** · wondering, oh, are you going to show us how how you did that? I I I also want to

**11:12** · how how you did that? I I I also want to know how to do that. Yeah, sure. I

**11:14** · know how to do that. Yeah, sure. I opened up Fable 5 on High Effort. By the

**11:17** · opened up Fable 5 on High Effort. By the way, this is, I think, one of the best

**11:19** · way, this is, I think, one of the best ways to use it. I found that this is

**11:20** · ways to use it. I found that this is kind of the sweet spot. Not extra high,

**11:23** · kind of the sweet spot. Not extra high, not ultra fable 5 high. So, I opened it

**11:26** · not ultra fable 5 high. So, I opened it up and I said, "This is what I want.

**11:28** · up and I said, "This is what I want. Tell me what you need for me. What kind

**11:29** · Tell me what you need for me. What kind of API keys? What services should I sign

**11:31** · of API keys? What services should I sign up for?" And then go build it. Once that

**11:34** · up for?" And then go build it. Once that X engine is built, on top of that, you

**11:37** · X engine is built, on top of that, you build the things that are actually

**11:38** · build the things that are actually useful to you. So, for example,

**11:39** · useful to you. So, for example, something that alerts you when a new

**11:42** · something that alerts you when a new trending topic is developing. Or in this

**11:44** · trending topic is developing. Or in this case, as you can see, we sort of broke

**11:46** · case, as you can see, we sort of broke down how well different format of tweets

**11:48** · down how well different format of tweets work. What if it's a standalone tweet

**11:50** · work. What if it's a standalone tweet with a native video or a quote and a

**11:52** · with a native video or a quote and a video clip, quote plus image, quote or

**11:54** · video clip, quote plus image, quote or link, or just bare text. What I realized

**11:57** · link, or just bare text. What I realized by looking at the data is that the

**11:59** · by looking at the data is that the Twitter algorithm changed a few months

**12:01** · Twitter algorithm changed a few months ago, and I didn't realize it. And so

**12:04** · ago, and I didn't realize it. And so what that meant was that my impressions

**12:06** · what that meant was that my impressions used to keep going up and up and up

**12:08** · used to keep going up and up and up month over month. That huge line in

**12:10** · month over month. That huge line in January 26th, that was a few viral hits.

**12:13** · January 26th, that was a few viral hits. So that's not really kind of

**12:14** · So that's not really kind of representative, but that was a good

**12:16** · representative, but that was a good month. One of those tweets was shown in

**12:18** · month. One of those tweets was shown in a fire ship video. So yes, as seen on

**12:21** · a fire ship video. So yes, as seen on fire, he was a little bit sarcastic

**12:23** · fire, he was a little bit sarcastic about the tweets, but he's a little bit

**12:24** · about the tweets, but he's a little bit sarcastic about everything. So and

**12:27** · sarcastic about everything. So and totally love that guy. So I I was just

**12:30** · totally love that guy. So I I was just happy to be mentioned. But notice

**12:31** · happy to be mentioned. But notice there's a steep drop off, right? You can

**12:34** · there's a steep drop off, right? You can look at it. You can see it. You know

**12:36** · look at it. You can see it. You know something happened. What? So, as you can

**12:38** · something happened. What? So, as you can see here, I have one of this these

**12:40** · see here, I have one of this these folders X analytics. So, we have all of

**12:42** · folders X analytics. So, we have all of our data that we are ingesting.

**12:45** · our data that we are ingesting. Ingesting is a special word that we use

**12:46** · Ingesting is a special word that we use here to basically say collect the data,

**12:48** · here to basically say collect the data, take the data into the vault into our

**12:51** · take the data into the vault into our second brain. Not just using that word

**12:53** · second brain. Not just using that word because I'm hungry. That's the correct

**12:55** · because I'm hungry. That's the correct terminology. Here we have all our

**12:56** · terminology. Here we have all our important accounts that we're keeping

**12:58** · important accounts that we're keeping track of. a weekly scorecard of how well

**13:02** · track of. a weekly scorecard of how well my tweets are performing and also the X

**13:05** · my tweets are performing and also the X engine. The X engine is the actual thing

**13:06** · engine. The X engine is the actual thing that runs it. So right now within the

**13:08** · that runs it. So right now within the second brain, this is the amount of data

**13:11** · second brain, this is the amount of data that we have. 22,000 posts archived,

**13:14** · that we have. 22,000 posts archived, almost 6 billion views represented,

**13:16** · almost 6 billion views represented, 4,400 unique authors. There's a lot

**13:20** · 4,400 unique authors. There's a lot there. How quickly can I reference one

**13:22** · there. How quickly can I reference one of them? Quickly pull out some piece of

**13:24** · of them? Quickly pull out some piece of information that I need. Instant. It's

**13:26** · information that I need. Instant. It's offline. No API needed. How much did

**13:28** · offline. No API needed. How much did this cost? Under a hundred bucks. I

**13:30** · this cost? Under a hundred bucks. I don't know the exact number. I know it's

**13:31** · don't know the exact number. I know it's under a hundred because I purchased $100

**13:33** · under a hundred because I purchased $100 in credits and that was enough. I just

**13:35** · in credits and that was enough. I just don't know exactly how much it spent.

**13:37** · don't know exactly how much it spent. And also, this isn't a static database.

**13:39** · And also, this isn't a static database. It's being watched. So, for example, it

**13:41** · It's being watched. So, for example, it lets us compute velocity of the trending

**13:44** · lets us compute velocity of the trending topic or tweet. Which post is getting

**13:46** · topic or tweet. Which post is getting 600 likes an hour right now, tracking

**13:48** · 600 likes an hour right now, tracking breaking AI news. It's also seeing which

**13:51** · breaking AI news. It's also seeing which strategies started breaking down at that

**13:54** · strategies started breaking down at that algorithmic change that we saw a few

**13:56** · algorithmic change that we saw a few months ago. and it's benchmarking me

**13:58** · months ago. and it's benchmarking me against some of the other accounts,

**14:00** · against some of the other accounts, right? So, if something that I'm doing

**14:01** · right? So, if something that I'm doing is underperforming, it allows me to

**14:03** · is underperforming, it allows me to pinpoint exactly what it is that I'm

**14:06** · pinpoint exactly what it is that I'm doing wrong. And notice that it's

**14:08** · doing wrong. And notice that it's storing all these insights and updating

**14:10** · storing all these insights and updating them and curating them. And it's a

**14:12** · them and curating them. And it's a living document, which Claude decided to

**14:14** · living document, which Claude decided to call X Growth Playbook. Now, again, the

**14:17** · call X Growth Playbook. Now, again, the reason I want to bring that up is

**14:18** · reason I want to bring that up is because I I wouldn't have called it that

**14:20** · because I I wouldn't have called it that necessarily. The point isn't let's grow.

**14:23** · necessarily. The point isn't let's grow. It's not a growth playbook. It's not a

**14:25** · It's not a growth playbook. It's not a growth hacks. I'm thinking of it more as

**14:27** · growth hacks. I'm thinking of it more as a don't shoot yourself in the foot Wes

**14:30** · a don't shoot yourself in the foot Wes playbook. The whole point is basically

**14:31** · playbook. The whole point is basically to understand kind of how the algorithm

**14:33** · to understand kind of how the algorithm functions if it changes so I don't get

**14:36** · functions if it changes so I don't get caught up in the changes and just lose

**14:38** · caught up in the changes and just lose all my views etc. So the point isn't

**14:41** · all my views etc. So the point isn't growth hacks. The point is what are the

**14:43** · growth hacks. The point is what are the best practices right now? By the way,

**14:45** · best practices right now? By the way, the next level up I think is to turn it

**14:48** · the next level up I think is to turn it into something like this. This is kind

**14:50** · into something like this. This is kind of what I'm building right now. This

**14:52** · of what I'm building right now. This also brings in ideas like for example

**14:54** · also brings in ideas like for example which apps are connected to claude. So I

**14:57** · which apps are connected to claude. So I have things like Obsidian, Social Blade

**15:00** · have things like Obsidian, Social Blade X, the X API, etc., etc. As your little

**15:04** · X, the X API, etc., etc. As your little sort of branching empire starts growing

**15:06** · sort of branching empire starts growing larger and larger, it really helps to

**15:08** · larger and larger, it really helps to have just one place where you can at a

**15:09** · have just one place where you can at a glance see, okay, what are all of the

**15:11** · glance see, okay, what are all of the things that are connected? What are all

**15:13** · things that are connected? What are all the apps and APIs that are hooked into

**15:15** · the apps and APIs that are hooked into the system? This is pretty important

**15:16** · the system? This is pretty important from a lot of different angles.

**15:18** · from a lot of different angles. Security, doing basic security checks.

**15:20** · Security, doing basic security checks. It's important to have this visualized

**15:22** · It's important to have this visualized somewhere saving money, right? You can

**15:23** · somewhere saving money, right? You can see at a glance what you're paying for,

**15:25** · see at a glance what you're paying for, what services you need to cancel. By the

**15:27** · what services you need to cancel. By the way, all these systems are getting

**15:28** · way, all these systems are getting pretty good at actually doing computer

**15:30** · pretty good at actually doing computer use, running their own browser. So, at

**15:31** · use, running their own browser. So, at some point, they'll be able to cancel a

**15:33** · some point, they'll be able to cancel a lot of the recurring and billing for us.

**15:35** · lot of the recurring and billing for us. I've already been testing it, trying to

**15:36** · I've already been testing it, trying to use the browser within cloud code to do

**15:38** · use the browser within cloud code to do certain tasks. It's pretty good so far,

**15:41** · certain tasks. It's pretty good so far, and I'm planning to start ramping it up

**15:42** · and I'm planning to start ramping it up more and more. Then, we have our

**15:44** · more and more. Then, we have our routine. So, these are actually the

**15:45** · routine. So, these are actually the things that are running on a daily

**15:48** · things that are running on a daily basis. So if you want to see all the

**15:49** · basis. So if you want to see all the things that are running the cron jobs,

**15:51** · things that are running the cron jobs, the things ingesting new data into the

**15:53** · the things ingesting new data into the second brain, all those routines,

**15:54** · second brain, all those routines, everything is there. Then we also have

**15:57** · everything is there. Then we also have our various skills. So those are like

**15:59** · our various skills. So those are like the skill.md files and everything

**16:01** · the skill.md files and everything everything. Now if you're wondering what

**16:03** · everything. Now if you're wondering what this doctrine is, again I have Claude

**16:05** · this doctrine is, again I have Claude naming a lot of these things. So bear

**16:07** · naming a lot of these things. So bear that in mind. So I told it to put all of

**16:09** · that in mind. So I told it to put all of the things like the learnings about the

**16:11** · the things like the learnings about the X algorithm. All of the sort of final

**16:13** · X algorithm. All of the sort of final insights, all of the juicy information

**16:15** · insights, all of the juicy information that we're squeezing out of this thing

**16:17** · that we're squeezing out of this thing into a folder. I'm like, call it

**16:19** · into a folder. I'm like, call it something cool. And I was like, oh, I

**16:20** · something cool. And I was like, oh, I know the doctrine. I was like, all

**16:22** · know the doctrine. I was like, all right, whatever, Claude. All right. So,

**16:24** · right, whatever, Claude. All right. So, so far we've talked about our first tool

**16:26** · so far we've talked about our first tool that you need. It's Obsidian. That's

**16:28** · that you need. It's Obsidian. That's this on the left. It's free. It's

**16:30** · this on the left. It's free. It's wonderful. It's local first. And

**16:32** · wonderful. It's local first. And Obsidian is basically just a bunch of

**16:35** · Obsidian is basically just a bunch of markdown files. So again, those markdown

**16:37** · markdown files. So again, those markdown files is just text plus a few simple

**16:39** · files is just text plus a few simple symbols that make it functional and it's

**16:41** · symbols that make it functional and it's really good for cross linking

**16:43** · really good for cross linking everything. So for example, here is

**16:45** · everything. So for example, here is Carpathy's LLM wiki. That's kind of the

**16:48** · Carpathy's LLM wiki. That's kind of the idea that kick this whole thing off. So

**16:50** · idea that kick this whole thing off. So let's click on it. This is part of the

**16:51** · let's click on it. This is part of the wiki. It's the database around that

**16:54** · wiki. It's the database around that subject, that topic. And markdown is

**16:56** · subject, that topic. And markdown is super simple. So let's say I wanted to

**16:58** · super simple. So let's say I wanted to add that he worked at OpenAI. We'll do

**17:00** · add that he worked at OpenAI. We'll do two hashtags for heading two. I'm going

**17:02** · two hashtags for heading two. I'm going to say used to work at. And notice how

**17:05** · to say used to work at. And notice how it turns into heading two. And I'll say

**17:07** · it turns into heading two. And I'll say Andre used to work at and I'm going to

**17:09** · Andre used to work at and I'm going to say OpenAI, but I will cross-link those

**17:12** · say OpenAI, but I will cross-link those two documents. I'll do double brackets.

**17:14** · two documents. I'll do double brackets. Notice how it prefills the other two

**17:16** · Notice how it prefills the other two double brackets. Now everything that you

**17:17** · double brackets. Now everything that you type between those two becomes a link.

**17:19** · type between those two becomes a link. So I'll type in Open AI. Notice it

**17:21** · So I'll type in Open AI. Notice it already gives me all of the other pages

**17:22** · already gives me all of the other pages that we have on OpenAI the topic, OpenAI

**17:25** · that we have on OpenAI the topic, OpenAI the entity, and various transcripts that

**17:28** · the entity, and various transcripts that include OpenAI in the title. So in this

**17:30** · include OpenAI in the title. So in this case, we'll say OpenAI the entity. And

**17:32** · case, we'll say OpenAI the entity. And now that links to that page. So you do

**17:35** · now that links to that page. So you do this enough times and these stop being

**17:38** · this enough times and these stop being just pages and they become a network. By

**17:40** · just pages and they become a network. By the way, when you don't have any tabs

**17:42** · the way, when you don't have any tabs open, if you hit CtrlG, that opens up

**17:44** · open, if you hit CtrlG, that opens up the graph view that lets you visualize

**17:47** · the graph view that lets you visualize that entire network. And if you hit

**17:49** · that entire network. And if you hit animate here, you can kind of see how

**17:51** · animate here, you can kind of see how page by page by page through

**17:53** · page by page by page through cross-linking, the whole thing takes

**17:55** · cross-linking, the whole thing takes shape as you add more and more data,

**17:57** · shape as you add more and more data, more and more pages, both raw pages that

**18:00** · more and more pages, both raw pages that are just from the internet or from

**18:02** · are just from the internet or from whatever data you're pulling in to

**18:03** · whatever data you're pulling in to actual summaries that are made by the LM

**18:06** · actual summaries that are made by the LM to all of the different stuff that

**18:07** · to all of the different stuff that you're adding to it. This slowly becomes

**18:09** · you're adding to it. This slowly becomes that kind of knowledge graph. It slowly

**18:12** · that kind of knowledge graph. It slowly becomes your second brain. Once you

**18:14** · becomes your second brain. Once you build this whole thing and you hit that

**18:15** · build this whole thing and you hit that animate button, this is just kind of

**18:17** · animate button, this is just kind of rewarding. just watching all that

**18:19** · rewarding. just watching all that information slowly come together. We're

**18:21** · information slowly come together. We're not going to watch it cuz I have too

**18:22** · not going to watch it cuz I have too much stuff in here. It'll take forever.

**18:24** · much stuff in here. It'll take forever. But this is your tool number one,

**18:26** · But this is your tool number one, Obsidian. And your second tool is Claude

**18:29** · Obsidian. And your second tool is Claude Code or Chad GPT or Codeex. Now, if

**18:32** · Code or Chad GPT or Codeex. Now, if you've been following this channel,

**18:32** · you've been following this channel, you've seen me use these models through

**18:34** · you've seen me use these models through a lot of different interfaces. For a

**18:36** · a lot of different interfaces. For a long time, I dealt more or less

**18:37** · long time, I dealt more or less exclusively with Open Claw. I would use

**18:39** · exclusively with Open Claw. I would use a Telegram to talk to it. I've used the

**18:41** · a Telegram to talk to it. I've used the command line interface, tons of

**18:43** · command line interface, tons of different ways of interacting with it.

**18:44** · different ways of interacting with it. Currently now with this new iteration of

**18:47** · Currently now with this new iteration of claude code desktop which is what you're

**18:49** · claude code desktop which is what you're seeing here. At this point I'm pretty

**18:50** · seeing here. At this point I'm pretty much exclusively using this. They added

**18:52** · much exclusively using this. They added a lot of functionality to where you

**18:54** · a lot of functionality to where you really don't need to leave this at all.

**18:56** · really don't need to leave this at all. It has claude code. You can switch over

**18:58** · It has claude code. You can switch over to the home tab which has your regular

**18:59** · to the home tab which has your regular kind of ability to talk to Claude as

**19:01** · kind of ability to talk to Claude as well as Claude co-working

**19:05** · kind of on this side. So what I did was I created a second brain directory or

**19:10** · I created a second brain directory or folder and I just told Claude to build

**19:12** · folder and I just told Claude to build everything in there. So now whatever new

**19:14** · everything in there. So now whatever new information we're ingesting, it finds a

**19:16** · information we're ingesting, it finds a place somewhere in there. So for

**19:17** · place somewhere in there. So for example, recently Anthropic released

**19:19** · example, recently Anthropic released this a global workspace in language

**19:21** · this a global workspace in language models. So it's basically talking about

**19:23** · models. So it's basically talking about if Claude could be conscious on some

**19:26** · if Claude could be conscious on some level or they're not suggesting that

**19:28** · level or they're not suggesting that that's what's happening. They're just

**19:29** · that's what's happening. They're just finding a lot of very interesting

**19:30** · finding a lot of very interesting similarities in how Claude's brain works

**19:34** · similarities in how Claude's brain works and how LM work. In some ways, it's very

**19:36** · and how LM work. In some ways, it's very similar to how the human brain works. So

**19:38** · similar to how the human brain works. So this idea of a global workspace is

**19:39** · this idea of a global workspace is something that exists in human brains.

**19:41** · something that exists in human brains. It's a mechanism by which we sort of

**19:43** · It's a mechanism by which we sort of find things that are unconscious and

**19:44** · find things that are unconscious and kind of bring it to the surface so that

**19:46** · kind of bring it to the surface so that we're able to interact with it in our

**19:47** · we're able to interact with it in our brains and they're finding something

**19:48** · brains and they're finding something that is analogous or similar in claude.

**19:51** · that is analogous or similar in claude. So definitely kind of a big deal of a of

**19:53** · So definitely kind of a big deal of a of a publishing of a paper. So we want to

**19:55** · a publishing of a paper. So we want to ingest this into our second brain. By

**19:57** · ingest this into our second brain. By the way, a lot of this should be handled

**19:59** · the way, a lot of this should be handled automatically here. I'm just showing you

**20:00** · automatically here. I'm just showing you how you would deal with it, how you

**20:02** · how you would deal with it, how you would do it manually if you needed to.

**20:04** · would do it manually if you needed to. So I'm going to take this URL or just

**20:06** · So I'm going to take this URL or just copy this and paste it. And we're going

**20:08** · copy this and paste it. And we're going to go into cloud. We're going to say

**20:09** · to go into cloud. We're going to say ingest and I'll just paste the link and

**20:12** · ingest and I'll just paste the link and we'll click go. Another really good

**20:13** · we'll click go. Another really good feature of Claude Code Desktop is you

**20:16** · feature of Claude Code Desktop is you can just dictate your commands. Click

**20:17** · can just dictate your commands. Click this microphone button and just say what

**20:20** · this microphone button and just say what you want it to do. Now, by the way, one

**20:22** · you want it to do. Now, by the way, one recent thing that they've added is an

**20:24** · recent thing that they've added is an actual built-in browser. So, if you

**20:26** · actual built-in browser. So, if you click on that, you can actually just

**20:27** · click on that, you can actually just type in whatever URL and it will open

**20:29** · type in whatever URL and it will open within this built-in browser within

**20:31** · within this built-in browser within Cloud Code Desktop. So I can go to

**20:33** · Cloud Code Desktop. So I can go to google.com for example and I can

**20:35** · google.com for example and I can actually tell it to open up web pages,

**20:37** · actually tell it to open up web pages, interact with those web pages, whatever

**20:38** · interact with those web pages, whatever you want. But here we'll actually open

**20:40** · you want. But here we'll actually open up a file. This is my second brain just

**20:42** · up a file. This is my second brain just a folder with a number of other folders

**20:44** · a folder with a number of other folders in it. And at the bottom I had to create

**20:46** · in it. And at the bottom I had to create this. So that is just this this kind of

**20:48** · this. So that is just this this kind of a visual representation of kind of like

**20:51** · a visual representation of kind of like the second brain 2.0 that I'm trying to

**20:53** · the second brain 2.0 that I'm trying to build that is going to have all the

**20:54** · build that is going to have all the skills and routines and everything else

**20:56** · skills and routines and everything else on top of it with a different

**20:57** · on top of it with a different visualization. And notice here as it's

**20:59** · visualization. And notice here as it's building out, ingesting that content

**21:01** · building out, ingesting that content from the anthropic website, it's saying

**21:03** · from the anthropic website, it's saying now the ripple. So they're cross linking

**21:06** · now the ripple. So they're cross linking all these pages, adding more information

**21:07** · all these pages, adding more information about it. So they're adding it to the

**21:09** · about it. So they're adding it to the interpretability concept page and

**21:11** · interpretability concept page and updating all the other entity pages. So

**21:13** · updating all the other entity pages. So I give it one link, it adds it, and now

**21:16** · I give it one link, it adds it, and now it's rippling through and adding it and

**21:18** · it's rippling through and adding it and interconnecting it within the network.

**21:20** · interconnecting it within the network. All right, so that's how we ingest

**21:22** · All right, so that's how we ingest information. That's how we add

**21:23** · information. That's how we add information to our second brain. All

**21:25** · information to our second brain. All right, but this is where it stops being

**21:26** · right, but this is where it stops being just a research engine and starts kind

**21:29** · just a research engine and starts kind of running my life because your second

**21:31** · of running my life because your second brain shouldn't just know about the news

**21:34** · brain shouldn't just know about the news and what's going on in the world. It

**21:35** · and what's going on in the world. It should know about your life. So, you've

**21:37** · should know about your life. So, you've probably heard about the conbon board.

**21:39** · probably heard about the conbon board. So, it's usually something that you have

**21:41** · So, it's usually something that you have maybe like on the wall you have sticky

**21:42** · maybe like on the wall you have sticky notes and you move those sticky notes

**21:44** · notes and you move those sticky notes from place to place. Each sticky note is

**21:46** · from place to place. Each sticky note is a project or a to-do item that kind of

**21:49** · a project or a to-do item that kind of goes through stages. So, maybe going

**21:50** · goes through stages. So, maybe going from to-do to doing to done. In

**21:53** · from to-do to doing to done. In Obsidian, it's very easy to create a

**21:56** · Obsidian, it's very easy to create a conbon board. So, for example, we might

**21:57** · conbon board. So, for example, we might have a flow like this if we're doing a

**22:00** · have a flow like this if we're doing a content calendar where videos get

**22:01** · content calendar where videos get produced from idea to research to

**22:04** · produced from idea to research to scripted to filmed, edited, and

**22:06** · scripted to filmed, edited, and published. Now, currently, my process of

**22:08** · published. Now, currently, my process of creating videos is a lot more chaotic,

**22:11** · creating videos is a lot more chaotic, let's say. And also, I don't script

**22:13** · let's say. And also, I don't script them. And I apologize if I'm stating the

**22:16** · them. And I apologize if I'm stating the obvious. If you ever seen me go on some

**22:18** · obvious. If you ever seen me go on some wild tangent and forget my original

**22:19** · wild tangent and forget my original idea, you probably can tell that none of

**22:21** · idea, you probably can tell that none of this is scripted. But now to try to keep

**22:24** · this is scripted. But now to try to keep up with the sheer amount of information

**22:26** · up with the sheer amount of information and releases, I am trying to be a little

**22:28** · and releases, I am trying to be a little bit more organized about how I release

**22:29** · bit more organized about how I release things, having certain ideas, some from

**22:32** · things, having certain ideas, some from me, some that Claude or some other

**22:34** · me, some that Claude or some other chatbot comes up with automatically

**22:35** · chatbot comes up with automatically based on the information available on

**22:37** · based on the information available on the trending news. So you might have

**22:39** · the trending news. So you might have tons of ideas ranked by some metric, how

**22:42** · tons of ideas ranked by some metric, how relevant it is, how interesting it is.

**22:44** · relevant it is, how interesting it is. So let's say I want to create one of

**22:46** · So let's say I want to create one of these. So recently I published a video

**22:48** · these. So recently I published a video called the $20,000 revenue apps with one

**22:51** · called the $20,000 revenue apps with one person teams or something like that. So

**22:53** · person teams or something like that. So I would pick it out of my list of ideas

**22:55** · I would pick it out of my list of ideas and I would move it to kind of this

**22:57** · and I would move it to kind of this packaging gate. So if it scores good on

**22:59** · packaging gate. So if it scores good on some metric about how viable it is as a

**23:01** · some metric about how viable it is as a video idea. So it gets put there. Once

**23:03** · video idea. So it gets put there. Once it's scored, we can move it to research.

**23:05** · it's scored, we can move it to research. And by the way, a lot of this stuff can

**23:07** · And by the way, a lot of this stuff can be automated. So if I move it there,

**23:09** · be automated. So if I move it there, Claude can go ahead and start working on

**23:12** · Claude can go ahead and start working on it. So here, as you can see, Claude

**23:13** · it. So here, as you can see, Claude already wrote some suggested hooks for

**23:16** · already wrote some suggested hooks for me. The first one is, "Three years ago,

**23:17** · me. The first one is, "Three years ago, I showed you a dad selling Excel

**23:19** · I showed you a dad selling Excel formulas for $25,000 a month. The number

**23:22** · formulas for $25,000 a month. The number today made me doublech checkck my

**23:24** · today made me doublech checkck my sources." In that video, I used the hook

**23:26** · sources." In that video, I used the hook about 6 minutes in. The first 6 minutes

**23:28** · about 6 minutes in. The first 6 minutes was me rambling. And then after 6

**23:30** · was me rambling. And then after 6 minutes or so, I got to the hook. Claude

**23:32** · minutes or so, I got to the hook. Claude tries and does a great job. I still find

**23:35** · tries and does a great job. I still find ways to mess it up, but that's on me.

**23:36** · ways to mess it up, but that's on me. So, let's say once we've done all the

**23:38** · So, let's say once we've done all the research, we move that to, you know,

**23:40** · research, we move that to, you know, scripting the video. Now again, I don't

**23:42** · scripting the video. Now again, I don't script my videos, but I do like to have

**23:44** · script my videos, but I do like to have these little cheat sheets with the

**23:47** · these little cheat sheets with the numbers and the claims, dates, things

**23:49** · numbers and the claims, dates, things like that written out that ensures that

**23:51** · like that written out that ensures that what I say on camera is accurate. So, I

**23:53** · what I say on camera is accurate. So, I tell Claude that I did a video 3 years

**23:56** · tell Claude that I did a video 3 years ago about this thing. I want to do a

**23:57** · ago about this thing. I want to do a follow-up. So, keep in mind, it has the

**24:00** · follow-up. So, keep in mind, it has the transcript of the video that I did 3

**24:01** · transcript of the video that I did 3 years ago that's in the vault. It knows

**24:03** · years ago that's in the vault. It knows every word I said on that video. Take a

**24:05** · every word I said on that video. Take a look at this. We covered a product back

**24:07** · look at this. We covered a product back then 3 years ago in 2023 that was doing

**24:09** · then 3 years ago in 2023 that was doing 20,000 a month. It was called

**24:11** · 20,000 a month. It was called thumbnailest.com and it was ab testing

**24:14** · thumbnailest.com and it was ab testing thumbnails by the way. And this is why I

**24:17** · thumbnails by the way. And this is why I love Claude. He's insufferable. Look at

**24:19** · love Claude. He's insufferable. Look at that. It says the thing your war room

**24:21** · that. It says the thing your war room now does for free with that grinning

**24:23** · now does for free with that grinning kind of smiley face like it's up to

**24:25** · kind of smiley face like it's up to something. So, it built that AB testing

**24:27** · something. So, it built that AB testing thumbnail software for me. And this is

**24:29** · thumbnail software for me. And this is it just being kind of smug about it's

**24:31** · it just being kind of smug about it's like, "Oh yeah, like I built that thing

**24:32** · like, "Oh yeah, like I built that thing for you." I, as you can imagine, did not

**24:34** · for you." I, as you can imagine, did not ask for that to be in the show notes in

**24:37** · ask for that to be in the show notes in the in the thing that I'm going to use

**24:38** · the in the thing that I'm going to use to prepare for my video for Cloud to be

**24:40** · to prepare for my video for Cloud to be like, "What's up?" That was not asked

**24:42** · like, "What's up?" That was not asked for. But notice what it did here. So, it

**24:44** · for. But notice what it did here. So, it found what happened to that case study

**24:46** · found what happened to that case study that I did in 2023. What happened to

**24:48** · that I did in 2023. What happened to thumbnailest.com? Is it still making

**24:50** · thumbnailest.com? Is it still making 20,000? Is it making more? It found that

**24:52** · 20,000? Is it making more? It found that it sold for six figures in 2024. By the

**24:55** · it sold for six figures in 2024. By the way, since then, YouTube actually

**24:57** · way, since then, YouTube actually launched their own internal thumb

**24:59** · launched their own internal thumb testing split testing tool. And as Cloud

**25:01** · testing split testing tool. And as Cloud is saying here, the platform ate the

**25:03** · is saying here, the platform ate the moat. And notice what it's saying here.

**25:04** · moat. And notice what it's saying here. This is the exact platform risk warning

**25:07** · This is the exact platform risk warning from your 2023 video. When Openi

**25:10** · from your 2023 video. When Openi announced Whisper, everyone building

**25:11** · announced Whisper, everyone building that was gone. So this is kind of why

**25:14** · that was gone. So this is kind of why having a second brain like this is so

**25:15** · having a second brain like this is so important because it's going back and

**25:17** · important because it's going back and checking my notes from 3 years ago. It's

**25:20** · checking my notes from 3 years ago. It's also updating it from doing internet

**25:22** · also updating it from doing internet search, kind of seeing what happened

**25:24** · search, kind of seeing what happened since then to now. It's doing all of

**25:26** · since then to now. It's doing all of that while while being smug about it.

**25:28** · that while while being smug about it. What's not to love here? So, while I

**25:30** · What's not to love here? So, while I don't use the content calendar in that

**25:32** · don't use the content calendar in that conbon style dashboard, I'm planning to

**25:35** · conbon style dashboard, I'm planning to do that a little bit more to kind of

**25:36** · do that a little bit more to kind of automate more of the research and

**25:38** · automate more of the research and information gathering, but here is a

**25:41** · information gathering, but here is a sponsor flow conbon board. This I

**25:44** · sponsor flow conbon board. This I actually do use to help me visualize

**25:46** · actually do use to help me visualize where I am in the process. These are

**25:48** · where I am in the process. These are dummy names, kind of dummy sponsors.

**25:50** · dummy names, kind of dummy sponsors. They're not real. I can't put the actual

**25:52** · They're not real. I can't put the actual sponsors in there because often times

**25:53** · sponsors in there because often times there's nondisclosure things. So, I

**25:56** · there's nondisclosure things. So, I can't use the real sponsors. But this is

**25:58** · can't use the real sponsors. But this is literally what it looks like. like we

**25:59** · literally what it looks like. like we have the script, the the sponsor

**26:01** · have the script, the the sponsor approval, recording, editing, and all

**26:03** · approval, recording, editing, and all the way once it's approved into

**26:05** · the way once it's approved into publishing. As I get approvals, I just

**26:07** · publishing. As I get approvals, I just drag it over, and this updates its

**26:09** · drag it over, and this updates its status. Once it's published, I put it

**26:11** · status. Once it's published, I put it into the done category, and I'm done.

**26:13** · into the done category, and I'm done. This, by the way, can be very easily

**26:15** · This, by the way, can be very easily hooked into some sort of a system that

**26:17** · hooked into some sort of a system that notifies you on your phone through a

**26:19** · notifies you on your phone through a text message or email if you're running

**26:21** · text message or email if you're running behind on something. If you're keeping

**26:22** · behind on something. If you're keeping up with things like this through Slack,

**26:24** · up with things like this through Slack, for example, we can pull that

**26:25** · for example, we can pull that information in here as well. And

**26:27** · information in here as well. And finally, it brings us to maybe the most

**26:30** · finally, it brings us to maybe the most important piece of this whole thing.

**26:31** · important piece of this whole thing. Kind of the point of the second brain.

**26:34** · Kind of the point of the second brain. It's called the doctrine. And again, I

**26:36** · It's called the doctrine. And again, I have to remind you here, I I don't come

**26:37** · have to remind you here, I I don't come up with these names. This is all claude.

**26:40** · up with these names. This is all claude. I think it knows that I like those RPG

**26:42** · I think it knows that I like those RPG games. So, it tries to kind of flavor

**26:44** · games. So, it tries to kind of flavor everything in that style. So, as it

**26:46** · everything in that style. So, as it wrote here, right? So, this is the

**26:47** · wrote here, right? So, this is the output layer of the second brain. So, we

**26:49** · output layer of the second brain. So, we have raw data flowing into it. The wiki

**26:52** · have raw data flowing into it. The wiki organizes everything that's known and

**26:54** · organizes everything that's known and the doctrine is what comes out the other

**26:55** · the doctrine is what comes out the other end. It's Fable Analyze. So, this is

**26:57** · end. It's Fable Analyze. So, this is done by Fable 5, which I found is

**26:59** · done by Fable 5, which I found is incredibly good at this kind of deep

**27:02** · incredibly good at this kind of deep data analysis and coming up with

**27:04** · data analysis and coming up with insights. So, it's Fable Analyze

**27:06** · insights. So, it's Fable Analyze receipts backed actionable strategy.

**27:08** · receipts backed actionable strategy. Every doc here answers, what do we

**27:10** · Every doc here answers, what do we actually do? And every claim in here

**27:12** · actually do? And every claim in here traces back to the data that we've

**27:14** · traces back to the data that we've collected. So, the war room gathers

**27:16** · collected. So, the war room gathers intelligence. So, I have this mini PC

**27:18** · intelligence. So, I have this mini PC that's always on. So, it's kind of like

**27:19** · that's always on. So, it's kind of like a Mac Mini and it just sits there. It's

**27:21** · a Mac Mini and it just sits there. It's hooked up to Wi-Fi. It doesn't take up a

**27:23** · hooked up to Wi-Fi. It doesn't take up a lot of electricity. Doesn't take up a

**27:25** · lot of electricity. Doesn't take up a lot of room. It just kind of looks like

**27:26** · lot of room. It just kind of looks like this. And I think it cost about 200

**27:28** · this. And I think it cost about 200 bucks on Amazon. And it runs 24/7. It

**27:31** · bucks on Amazon. And it runs 24/7. It never turns off. It doesn't have a

**27:32** · never turns off. It doesn't have a screen saver. It's just like a little

**27:33** · screen saver. It's just like a little box that's always on. And so that's sort

**27:35** · box that's always on. And so that's sort of the war room, if you will. It kind of

**27:37** · of the war room, if you will. It kind of just sits there, collects data. It's

**27:39** · just sits there, collects data. It's looking at what's happening on YouTube,

**27:41** · looking at what's happening on YouTube, on X, on various news platforms. It's

**27:44** · on X, on various news platforms. It's the 247 kind of home of the agents that

**27:47** · the 247 kind of home of the agents that just gather data. Then the wiki

**27:49** · just gather data. Then the wiki remembers it, organizes it, cross-links

**27:52** · remembers it, organizes it, cross-links it, all the stuff that we talked about

**27:53** · it, all the stuff that we talked about before. And the doctrine decides how we

**27:55** · before. And the doctrine decides how we fight. Again, I'm sure we could have

**27:56** · fight. Again, I'm sure we could have used some corporate speak to make these

**27:59** · used some corporate speak to make these names and describe what they do, but I

**28:01** · names and describe what they do, but I think I would just like fall asleep here

**28:02** · think I would just like fall asleep here at my keyboard. And then the armory

**28:04** · at my keyboard. And then the armory tracks what we're building next. So

**28:06** · tracks what we're building next. So those future projects, those nice to

**28:08** · those future projects, those nice to have that that's all in there largely

**28:10** · have that that's all in there largely selected and suggested by Fable. Now, of

**28:13** · selected and suggested by Fable. Now, of course, at the end of the day, I'm the

**28:15** · course, at the end of the day, I'm the one that's choosing what to focus on,

**28:16** · one that's choosing what to focus on, what to do. But a lot of the heavy

**28:18** · what to do. But a lot of the heavy lifting, the analysis, the data

**28:20** · lifting, the analysis, the data collection, all of that is handled by

**28:23** · collection, all of that is handled by Claude. By the way, the next big step

**28:25** · Claude. By the way, the next big step will be once we have kind of like our

**28:27** · will be once we have kind of like our to-do actions from the doctrine, we're

**28:29** · to-do actions from the doctrine, we're going to execute on them and collect

**28:31** · going to execute on them and collect data about how it works. So, the next,

**28:33** · data about how it works. So, the next, let's say, few quarters, 6 months, 12

**28:35** · let's say, few quarters, 6 months, 12 months, whatever. that will become its

**28:37** · months, whatever. that will become its own sort of flywheel where we're putting

**28:39** · own sort of flywheel where we're putting together strategies, we're executing on

**28:41** · together strategies, we're executing on them, we're seeing the results, and

**28:43** · them, we're seeing the results, and we're updating in real time how well

**28:44** · we're updating in real time how well it's working. So, the longer it runs,

**28:47** · it's working. So, the longer it runs, the more it compounds, not just in terms

**28:48** · the more it compounds, not just in terms of the sheer data that's coming in, but

**28:50** · of the sheer data that's coming in, but also in terms of the the learning that

**28:52** · also in terms of the the learning that the system is doing, both in terms of of

**28:54** · the system is doing, both in terms of of just what it knows, but also of making

**28:57** · just what it knows, but also of making strategies, executing them, and and

**28:59** · strategies, executing them, and and getting feedback. So, sort of that udal

**29:00** · getting feedback. So, sort of that udal loop. So, for those who are not

**29:02** · loop. So, for those who are not familiar, so observe, orient, decide,

**29:04** · familiar, so observe, orient, decide, and act. and then it becomes a loop. So

**29:06** · and act. and then it becomes a loop. So observe is the data collection orient is

**29:09** · observe is the data collection orient is the wiki and the summaries and in fact

**29:11** · the wiki and the summaries and in fact the the doctrine then deciding is like

**29:13** · the the doctrine then deciding is like kind of like what we're doing with that.

**29:14** · kind of like what we're doing with that. They act as the actual action the

**29:16** · They act as the actual action the execution of that strategy and then

**29:18** · execution of that strategy and then we're taking that data and we're adding

**29:20** · we're taking that data and we're adding it into the UDA loop. By the way since

**29:23** · it into the UDA loop. By the way since Fable designed a lot of this even if

**29:25** · Fable designed a lot of this even if Fable does go away eventually we don't

**29:27** · Fable does go away eventually we don't get it back a lot of the stuff that it's

**29:28** · get it back a lot of the stuff that it's built will still be helpful. So a lot of

**29:30** · built will still be helpful. So a lot of this doesn't necessarily rely on Fable

**29:33** · this doesn't necessarily rely on Fable to to continue. A lot of the data

**29:35** · to to continue. A lot of the data collection is automatic. But think about

**29:37** · collection is automatic. But think about this. As time goes on, this system, what

**29:40** · this. As time goes on, this system, what happens as better and better models come

**29:42** · happens as better and better models come out? Does the system become better,

**29:44** · out? Does the system become better, worse, or stay the same? I think we can

**29:46** · worse, or stay the same? I think we can safely say that the system not only just

**29:48** · safely say that the system not only just gets better the longer it runs, it also

**29:50** · gets better the longer it runs, it also gets better and better with stronger and

**29:52** · gets better and better with stronger and smarter models being released and and

**29:54** · smarter models being released and and used to run the system to to improve the

**29:57** · used to run the system to to improve the system. So, let me show you how to build

**29:59** · system. So, let me show you how to build this for yourself. And my advice to you

**30:01** · this for yourself. And my advice to you is take the time to do this. This might

**30:03** · is take the time to do this. This might take some time to set up. Maybe there's

**30:06** · take some time to set up. Maybe there's going to be some new skills that you

**30:07** · going to be some new skills that you have to learn. Learning can and probably

**30:09** · have to learn. Learning can and probably should be a little bit uncomfortable.

**30:10** · should be a little bit uncomfortable. There's a certain feeling that comes

**30:12** · There's a certain feeling that comes with doing new stuff. It's not just like

**30:14** · with doing new stuff. It's not just like pure joy. There's there's a little bit

**30:16** · pure joy. There's there's a little bit of a difficulty of resistance. Just push

**30:18** · of a difficulty of resistance. Just push through that. Build this because once

**30:19** · through that. Build this because once it's in place, it starts compounding. It

**30:22** · it's in place, it starts compounding. It starts growing. I honestly wish I did

**30:24** · starts growing. I honestly wish I did this on day one whenever Karpathy talked

**30:26** · this on day one whenever Karpathy talked about it. I knew it was a good idea. I

**30:28** · about it. I knew it was a good idea. I should have jumped on it right then and

**30:29** · should have jumped on it right then and there. All right. So this is how you

**30:31** · there. All right. So this is how you build this for yourself. I don't want to

**30:33** · build this for yourself. I don't want to say it's super fast. Some of these steps

**30:35** · say it's super fast. Some of these steps take time. For some of them, you have to

**30:37** · take time. For some of them, you have to wait for for Claude to build some of it,

**30:39** · wait for for Claude to build some of it, to organize some of it, but you can

**30:41** · to organize some of it, but you can probably do this in a single afternoon.

**30:43** · probably do this in a single afternoon. So first and foremost, you need two

**30:44** · So first and foremost, you need two tools. Obsidian and Claude Code. So

**30:47** · tools. Obsidian and Claude Code. So Obsidian is the note takingaking app,

**30:49** · Obsidian is the note takingaking app, although it's a little bit more than

**30:50** · although it's a little bit more than that. So it's over here. Obsidian.md.

**30:52** · that. So it's over here. Obsidian.md. Here it is. Again, free to start. Most

**30:55** · Here it is. Again, free to start. Most of it is free. It has a huge community.

**30:57** · of it is free. It has a huge community. It's a pretty cool tool if I do say so

**31:00** · It's a pretty cool tool if I do say so myself. There's a lot to like here and

**31:02** · myself. There's a lot to like here and it's free without limits. No sign up

**31:04** · it's free without limits. No sign up required. No strings attached. It's a

**31:06** · required. No strings attached. It's a cool tool by by cool people. Then get

**31:08** · cool tool by by cool people. Then get Cloud Code Desktop. Again, you don't

**31:10** · Cloud Code Desktop. Again, you don't have to get the desktop app. If you're

**31:13** · have to get the desktop app. If you're already settled in certain routine, you

**31:14** · already settled in certain routine, you know what you're doing, do that. But I

**31:16** · know what you're doing, do that. But I got to say, if you haven't tried it,

**31:18** · got to say, if you haven't tried it, they've really been making a lot of good

**31:19** · they've really been making a lot of good strides with it, and it does seem like

**31:21** · strides with it, and it does seem like it's becoming that super app that we've

**31:23** · it's becoming that super app that we've been waiting for. And I don't know that

**31:25** · been waiting for. And I don't know that that might be the the final form, at

**31:27** · that might be the the final form, at least for me. I'm really wondering what

**31:29** · least for me. I'm really wondering what else they can do to to improve on it.

**31:31** · else they can do to to improve on it. Like if you haven't realized that this

**31:33** · Like if you haven't realized that this is it. I'm using the browser within it

**31:35** · is it. I'm using the browser within it to search for the stuff that I need. I

**31:37** · to search for the stuff that I need. I can even ask Claude to go and download

**31:39** · can even ask Claude to go and download and install it. By the way, if I need to

**31:40** · and install it. By the way, if I need to take this on the road and use it from my

**31:43** · take this on the road and use it from my phone, I just type in / remote control.

**31:45** · phone, I just type in / remote control. I hit enter and then that allows it for

**31:48** · I hit enter and then that allows it for me to use it from the Anthropic or Cloud

**31:50** · me to use it from the Anthropic or Cloud app on my phone. And as they say here

**31:52** · app on my phone. And as they say here also to view and control the session

**31:53** · also to view and control the session from cloud.ai/code.

**31:55** · from cloud.ai/code. So you're able to remote control this

**31:57** · So you're able to remote control this from anywhere. All right. So you got

**31:59** · from anywhere. All right. So you got Obsidian, you got Cloud Code. Both are

**32:02** · Obsidian, you got Cloud Code. Both are free to start. My recommendation is you

**32:04** · free to start. My recommendation is you do purchase a subscription either

**32:06** · do purchase a subscription either anthropic or OpenAI or whatever chatbot

**32:09** · anthropic or OpenAI or whatever chatbot you think is best. But at this point, I

**32:10** · you think is best. But at this point, I feel like you kind of need one. If you

**32:13** · feel like you kind of need one. If you understand kind of the significance of

**32:15** · understand kind of the significance of what these companies are are building, I

**32:17** · what these companies are are building, I would say it's time to invest if you

**32:19** · would say it's time to invest if you don't yet have a subscription. Then we

**32:21** · don't yet have a subscription. Then we make the vault. We do that by opening up

**32:23** · make the vault. We do that by opening up obsidian. When you open up for the first

**32:25** · obsidian. When you open up for the first time, the button is create new vault or

**32:27** · time, the button is create new vault or something like that. And that will get

**32:28** · something like that. And that will get you started. Inside you make three

**32:30** · you started. Inside you make three folders. Inbox, raw, and wiki. Inside

**32:33** · folders. Inbox, raw, and wiki. Inside the wiki, you can make folders like

**32:35** · the wiki, you can make folders like concepts, entities, summaries, plus two

**32:37** · concepts, entities, summaries, plus two empty notes, index, and log. Here's the

**32:39** · empty notes, index, and log. Here's the thing. I didn't do any of this. I told

**32:41** · thing. I didn't do any of this. I told Claude to build me this thing. It made

**32:43** · Claude to build me this thing. It made all of the folders, all the files,

**32:45** · all of the folders, all the files, everything, everything, everything. By

**32:46** · everything, everything, everything. By the way, quick note. Notice how flat the

**32:48** · the way, quick note. Notice how flat the structure is. So, we don't have 50

**32:50** · structure is. So, we don't have 50 subpages beneath each page. Everything

**32:53** · subpages beneath each page. Everything is pretty flat. This is not me being

**32:55** · is pretty flat. This is not me being lazy or Claude being lazy. This is by

**32:57** · lazy or Claude being lazy. This is by design. Also, notice that the folders

**32:59** · design. Also, notice that the folders aren't topics. So, there isn't a folder

**33:02** · aren't topics. So, there isn't a folder called AI news. The folders are the

**33:04** · called AI news. The folders are the different layers. What goes in, what it

**33:06** · different layers. What goes in, what it knows, and what it concludes. In fact,

**33:08** · knows, and what it concludes. In fact, some of these things like templates, I

**33:10** · some of these things like templates, I shouldn't even have it on here. And the

**33:12** · shouldn't even have it on here. And the topics, those topics, they live in the

**33:14** · topics, those topics, they live in the links. So, OpenAI is a topic. It's the

**33:17** · links. So, OpenAI is a topic. It's the link that we use to cross-link all of

**33:18** · link that we use to cross-link all of the different pages that have anything

**33:20** · the different pages that have anything to do with OpenAI. Creating too many

**33:23** · to do with OpenAI. Creating too many subfolders, those kind of deep nested

**33:25** · subfolders, those kind of deep nested structures, it becomes a nightmare for

**33:27** · structures, it becomes a nightmare for LLMs. Keep it very, very flat. Next step

**33:30** · LLMs. Keep it very, very flat. Next step to creating this would be to write the

**33:32** · to creating this would be to write the rulebook aka claude.md. Now again, I

**33:35** · rulebook aka claude.md. Now again, I didn't write this. Claude did. By the

**33:37** · didn't write this. Claude did. By the way, I'll have a template down below

**33:39** · way, I'll have a template down below that you can just download and give to

**33:41** · that you can just download and give to your agent and it will execute

**33:43** · your agent and it will execute everything for you. But the cloud.md

**33:45** · everything for you. But the cloud.md file that's the rulebook that's the

**33:47** · file that's the rulebook that's the employee rulebook. Every morning cloud

**33:49** · employee rulebook. Every morning cloud wakes up and reads the rule book and

**33:51** · wakes up and reads the rule book and goes to work. So for example the raw

**33:52** · goes to work. So for example the raw files those are the immutable source

**33:54** · files those are the immutable source documents. So those are the things

**33:56** · documents. So those are the things directly from the source. We don't

**33:58** · directly from the source. We don't change them. The wiki is the LM wiki.

**34:00** · change them. The wiki is the LM wiki. The summaries the entities concepts

**34:02** · The summaries the entities concepts those are the compounding knowledge

**34:04** · those are the compounding knowledge maintained by our AI librarian. So just

**34:07** · maintained by our AI librarian. So just start there. Later you can add all the

**34:09** · start there. Later you can add all the other things like I added the doctrine

**34:11** · other things like I added the doctrine etc. The inbox are quick captures from

**34:13** · etc. The inbox are quick captures from me waiting to be processed. So, this is

**34:15** · me waiting to be processed. So, this is going to have to be in a different

**34:16** · going to have to be in a different video, but there are ways to do, for

**34:18** · video, but there are ways to do, for example, voice notes where you dictate

**34:19** · example, voice notes where you dictate something or certain emails or even

**34:21** · something or certain emails or even creating a little Chrome plugin to

**34:23** · creating a little Chrome plugin to whenever you see something that you want

**34:24** · whenever you see something that you want to add to this, you just talk it into

**34:26** · to add to this, you just talk it into your phone or you just record your voice

**34:28** · your phone or you just record your voice or you just click a button so that it

**34:30** · or you just click a button so that it goes to the inbox and then later gets

**34:31** · goes to the inbox and then later gets processed by Claude. Then the next step

**34:34** · processed by Claude. Then the next step is optional, but if you wanted to have

**34:36** · is optional, but if you wanted to have that graph, that data view, that's a

**34:38** · that graph, that data view, that's a plugin in Obsidian. Same with the conbon

**34:41** · plugin in Obsidian. Same with the conbon board. The next step is optional and

**34:43** · board. The next step is optional and that's adding two plugins, data view and

**34:46** · that's adding two plugins, data view and conbon. Data view builds those automatic

**34:48** · conbon. Data view builds those automatic tables. Conbon is that conbon view where

**34:50** · tables. Conbon is that conbon view where you drag little stickers across the

**34:52** · you drag little stickers across the board. You can skip those on day one if

**34:53** · board. You can skip those on day one if you want. This works very well without

**34:55** · you want. This works very well without them, but you can find those in settings

**34:57** · them, but you can find those in settings and they have core plugins and they also

**34:59** · and they have core plugins and they also have community plugins. You have to turn

**35:01** · have community plugins. You have to turn them on. So approve the fact that those

**35:02** · them on. So approve the fact that those can be used and I'm using here data view

**35:04** · can be used and I'm using here data view and conbon. And then you start feeding

**35:06** · and conbon. And then you start feeding your second brain. You start ingesting

**35:08** · your second brain. You start ingesting data. If you do it 10 times around 10

**35:10** · data. If you do it 10 times around 10 those dots start to become a web. So

**35:13** · those dots start to become a web. So take one afternoon to set this up. Then

**35:16** · take one afternoon to set this up. Then daily just start adding maybe one link a

**35:18** · daily just start adding maybe one link a day or whatever you think is best.

**35:20** · day or whatever you think is best. Ideally you also set up some automation

**35:22** · Ideally you also set up some automation so it pulls the data that you care

**35:23** · so it pulls the data that you care about. You can do it for your personal

**35:25** · about. You can do it for your personal tasks for your business or job or

**35:28** · tasks for your business or job or school. You can do it for your health or

**35:30** · school. You can do it for your health or whatever you want. Check out the link

**35:32** · whatever you want. Check out the link below. So I'll have a PDF that kind of

**35:34** · below. So I'll have a PDF that kind of explains it. You can read it or just

**35:37** · explains it. You can read it or just hand it to cloud code or whatever

**35:38** · hand it to cloud code or whatever chatbot you're using and tell it to set

**35:41** · chatbot you're using and tell it to set it up for you. So what we built is a

**35:43** · it up for you. So what we built is a Wikipedia that you care about. It's

**35:46** · Wikipedia that you care about. It's maintained entirely by AI. It can run

**35:48** · maintained entirely by AI. It can run your work life plus create certain

**35:51** · your work life plus create certain actionable playbooks from your own data,

**35:53** · actionable playbooks from your own data, things that you care about. Everything's

**35:55** · things that you care about. Everything's stored on your computer as basically

**35:57** · stored on your computer as basically text files. It's on your computer. You

**35:59** · text files. It's on your computer. You own it forever. You're not tied down to

**36:01** · own it forever. You're not tied down to any application, any model. As new

**36:04** · any application, any model. As new things come out, this stays useful.

**36:06** · things come out, this stays useful. Obsidian or cloud code, they don't

**36:08** · Obsidian or cloud code, they don't control those files. Those files are

**36:10** · control those files. Those files are text files. No one can lock them down or

**36:13** · text files. No one can lock them down or take them away. Why this matters is

**36:15** · take them away. Why this matters is because notes that get maintained this

**36:17** · because notes that get maintained this way, they actually get used. They're

**36:20** · way, they actually get used. They're useful. They also don't take a lot of

**36:21** · useful. They also don't take a lot of bandwidth for you to to figure them out

**36:23** · bandwidth for you to to figure them out and organize them. This was an

**36:25** · and organize them. This was an 80-year-old dream at this point that is

**36:27** · 80-year-old dream at this point that is finally possible. It's your own personal

**36:29** · finally possible. It's your own personal library with a librarian that never

**36:31** · library with a librarian that never sleeps. So, make sure you're subscribed

**36:33** · sleeps. So, make sure you're subscribed to this channel because more stuff is

**36:35** · to this channel because more stuff is coming that's going to utilize this and

**36:37** · coming that's going to utilize this and build on top of this. If you have any

**36:39** · build on top of this. If you have any questions, comments, tips, leave them

**36:41** · questions, comments, tips, leave them below. And if anything didn't make

**36:43** · below. And if anything didn't make sense, definitely let me know so I can

**36:44** · sense, definitely let me know so I can kind of troubleshoot and hopefully

**36:46** · kind of troubleshoot and hopefully improve the next time that I'm talking

**36:48** · improve the next time that I'm talking about this. If you made this far, thank

**36:49** · about this. If you made this far, thank you so much for watching. I will see you

**36:51** · you so much for watching. I will see you in the next
