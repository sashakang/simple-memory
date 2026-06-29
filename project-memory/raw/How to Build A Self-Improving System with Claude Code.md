---
title: "How to Build A Self-Improving System with Claude Code"
source: "https://www.youtube.com/watch?v=2fc0NX9vIJ8"
author:
  - "[[Austin Marchese]]"
published: 2026-06-28
created: 2026-06-29
description: "Austin Marchese presents a five-step B.U.I.L.D. framework for Claude Code: knowledge base, bulk ingest, inflow pipelines, improvement loops, and pragmatic execution."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=2fc0NX9vIJ8)

Get my free 5-day AI playbook (what I used to build a $25M+ startup): https://the-ai-playbook.com/sis

In this video, I break down the exact 5-step B.U.I.L.D. Framework I use to turn Claude Code into a self-improving system. After studying Andrej Karpathy, the Anthropic team, and running my own setup, this is everything you need to ingest your own data, automate the pipelines, and let the system get smarter every week. Most people get "self-improving" completely wrong, and I'll show you why.

Timestamps:
(0:00) - How to Build a Self-Improving System with Claude Code
(0:20) - Step 1: BASE — Create the Framework
(1:59) - Step 2: UPLOAD — Bulk Ingest Your Data
(4:26) - Step 3: INFLOW — Set Up Your Data Pipelines
(9:39) - Step 4: LOOP — The Improvement Loop
(14:46) - Step 5: DRIVE — Run It, Don't Over-Engineer

## Transcript

**0:00** · I've been obsessed with building my own self-improving system with Claude code.

**0:03** · self-improving system with Claude code. And after studying Andrej Karpathy, the

**0:05** · And after studying Andrej Karpathy, the Anthropic team, and running my own

**0:06** · Anthropic team, and running my own system, I've identified a five-step

**0:09** · system, I've identified a five-step build framework that lets anyone create

**0:11** · build framework that lets anyone create a self-improving system with Claude

**0:13** · a self-improving system with Claude code. Today, I'm walking through all

**0:14** · code. Today, I'm walking through all five steps, exactly how to implement

**0:16** · five steps, exactly how to implement them, and the lessons I've learned from

**0:17** · them, and the lessons I've learned from teaching hundreds of people the same

**0:19** · teaching hundreds of people the same system. Step one is base, create the

**0:21** · system. Step one is base, create the framework for improving. Before you do

**0:23** · framework for improving. Before you do anything, you need to create a project.

**0:24** · anything, you need to create a project. This is where you store all the data so

**0:26** · This is where you store all the data so you can enhance it over time. To create

**0:27** · you can enhance it over time. To create this project, there are two parts. One,

**0:29** · this project, there are two parts. One, a knowledge base where you store the

**0:30** · a knowledge base where you store the data, and two, the skills that let you

**0:33** · data, and two, the skills that let you work 10 times faster. So, part one, the

**0:35** · work 10 times faster. So, part one, the knowledge base. Andrej Karpathy went

**0:37** · knowledge base. Andrej Karpathy went viral for his concept called LLM

**0:39** · viral for his concept called LLM knowledge base. I have videos on my

**0:41** · knowledge base. I have videos on my channel diving deep into this, but the

**0:42** · channel diving deep into this, but the concept is fairly simple. You have a raw

**0:44** · concept is fairly simple. You have a raw folder, which includes any raw resources

**0:46** · folder, which includes any raw resources you ingest. For example, this could be a

**0:48** · you ingest. For example, this could be a call transcript you record. And then you

**0:50** · call transcript you record. And then you have a wiki folder, which references

**0:52** · have a wiki folder, which references files in your raw folder to help AI know

**0:54** · files in your raw folder to help AI know where to look. Think of this like a

**0:56** · where to look. Think of this like a table of contents in a book, so AI can

**0:57** · table of contents in a book, so AI can locate information without reading the

**0:59** · locate information without reading the entire book. Here's a prompt, which will

**1:01** · entire book. Here's a prompt, which will help you set this up from scratch or in

**1:03** · help you set this up from scratch or in an existing project that you're

**1:04** · an existing project that you're currently working on. And to enforce

**1:06** · currently working on. And to enforce this, we'll update the claude.md file to

**1:08** · this, we'll update the claude.md file to explain how it's all set up. This file

**1:10** · explain how it's all set up. This file essentially serves as a consistent

**1:12** · essentially serves as a consistent reminder to Claude about the framework.

**1:13** · reminder to Claude about the framework. Part two is skills for repetitive tasks.

**1:16** · Part two is skills for repetitive tasks. If you're doing the same thing twice

**1:18** · If you're doing the same thing twice with Claude, you should create a skill.

**1:19** · with Claude, you should create a skill. And a skill is your way of telling

**1:21** · And a skill is your way of telling Claude exactly how to handle a task.

**1:23** · Claude exactly how to handle a task. It's the same process every single time,

**1:25** · It's the same process every single time, so you don't have to go back and forth.

**1:27** · so you don't have to go back and forth. The first skill that I set up with every

**1:28** · The first skill that I set up with every person I work with is add new resource.

**1:30** · person I work with is add new resource. This tells Claude exactly how to add a

**1:32** · This tells Claude exactly how to add a new file into the system. It will take a

**1:34** · new file into the system. It will take a raw file, ingest it into raw, and then

**1:36** · raw file, ingest it into raw, and then Claude will analyze it and update or

**1:38** · Claude will analyze it and update or create any wiki entries that should

**1:40** · create any wiki entries that should reference it. These utility skills will

**1:42** · reference it. These utility skills will come into play later when I go through

**1:44** · come into play later when I go through orchestration skills, which call

**1:45** · orchestration skills, which call multiple utility skills together to

**1:48** · multiple utility skills together to create a bigger output. To set up both

**1:49** · create a bigger output. To set up both parts, both the knowledge and the

**1:51** · parts, both the knowledge and the skills, here is a single prompt that

**1:52** · skills, here is a single prompt that combines the two. This prompt will help

**1:54** · combines the two. This prompt will help you create the project, which will set

**1:55** · you create the project, which will set the foundation for the entire system.

**1:57** · the foundation for the entire system. Now you have the project set up, but

**1:58** · Now you have the project set up, but step two is about creating your own data

**2:00** · step two is about creating your own data lake. Step two, upload, identify your

**2:03** · lake. Step two, upload, identify your data plus bulk ingest. Before creating a

**2:05** · data plus bulk ingest. Before creating a self-improving system, you need to

**2:07** · self-improving system, you need to ingest everything you've already done.

**2:08** · ingest everything you've already done. We want to work smarter, not harder. So

**2:10** · We want to work smarter, not harder. So let's look at all of our historical

**2:12** · let's look at all of our historical training data that's already exists and

**2:14** · training data that's already exists and bring that all together in one place. To

**2:16** · bring that all together in one place. To do this, we're going to look in three

**2:17** · do this, we're going to look in three places. Place one is your AI inputs.

**2:19** · places. Place one is your AI inputs. This is the data you generate just by

**2:21** · This is the data you generate just by using AI. So this is your conversation

**2:24** · using AI. So this is your conversation history and in my eyes, this is the most

**2:26** · history and in my eyes, this is the most relevant training data that you'll ever

**2:28** · relevant training data that you'll ever find because it's literally you inside

**2:31** · find because it's literally you inside the terminal asking the AI ecosystem

**2:33** · the terminal asking the AI ecosystem questions. And the beauty of this is

**2:35** · questions. And the beauty of this is that Claude already saves all of its

**2:37** · that Claude already saves all of its session history locally. So there's a

**2:38** · session history locally. So there's a file that you can analyze historical

**2:40** · file that you can analyze historical conversations with. Here's a prompt that

**2:42** · conversations with. Here's a prompt that you can run that will analyze your

**2:43** · you can run that will analyze your session history for you and provide your

**2:44** · session history for you and provide your project with clear learnings and skill

**2:46** · project with clear learnings and skill suggestions. The key part here is the

**2:48** · suggestions. The key part here is the phrase suggest ways we can improve my

**2:50** · phrase suggest ways we can improve my system. The second place is personal

**2:52** · system. The second place is personal ecosystem data. Everywhere you interact

**2:54** · ecosystem data. Everywhere you interact online, you create your own data

**2:56** · online, you create your own data footprint. So this is the process of

**2:58** · footprint. So this is the process of grabbing as much data from those

**3:00** · grabbing as much data from those footprints as possible and bringing it

**3:02** · footprints as possible and bringing it into the system. Now there are a lot of

**3:03** · into the system. Now there are a lot of ways that you can do this, but two

**3:05** · ways that you can do this, but two specific ways to do this that apply to

**3:06** · specific ways to do this that apply to everyone watching this video is the

**3:08** · everyone watching this video is the first, which is use Claude to mine your

**3:10** · first, which is use Claude to mine your own computer. Open Claude code and say

**3:12** · own computer. Open Claude code and say analyze my computer and identify any

**3:14** · analyze my computer and identify any files you think would be helpful to

**3:16** · files you think would be helpful to ingest into the system. This will

**3:17** · ingest into the system. This will surface any information you already have

**3:19** · surface any information you already have on your machine that will be valuable

**3:20** · on your machine that will be valuable for the system you're building. And the

**3:21** · for the system you're building. And the second is to pull your email history. If

**3:23** · second is to pull your email history. If you use Google, there's a feature called

**3:25** · you use Google, there's a feature called Google Takeout. If you use Outlook,

**3:27** · Google Takeout. If you use Outlook, there's a feature called Outlook Export.

**3:29** · there's a feature called Outlook Export. You can then take this export and bring

**3:30** · You can then take this export and bring it into Claude to analyze your writing

**3:32** · it into Claude to analyze your writing style and any potential places to use AI

**3:34** · style and any potential places to use AI that you're not already using it. And if

**3:36** · that you're not already using it. And if you are concerned with data privacy,

**3:38** · you are concerned with data privacy, okay, just skip this part. This prompt

**3:40** · okay, just skip this part. This prompt will help you ingest these two data

**3:41** · will help you ingest these two data sets. The third place to look is your

**3:43** · sets. The third place to look is your life story and project goals. This one

**3:46** · life story and project goals. This one is simple and most people don't think to

**3:47** · is simple and most people don't think to do it. Just sit down and record yourself

**3:49** · do it. Just sit down and record yourself talking about your life, your project

**3:50** · talking about your life, your project goals, and what you want to accomplish.

**3:52** · goals, and what you want to accomplish. Then upload that recording to Claude and

**3:54** · Then upload that recording to Claude and say, "Analyze this recording and

**3:55** · say, "Analyze this recording and interview me to fill in anything I may

**3:57** · interview me to fill in anything I may have missed, and once finalized, add

**4:00** · have missed, and once finalized, add this as training data to my project."

**4:01** · this as training data to my project." Claude will then interview you, and by

**4:03** · Claude will then interview you, and by the end you have a file that you can

**4:04** · the end you have a file that you can bring anywhere with you that gives

**4:06** · bring anywhere with you that gives context to AI that it probably didn't

**4:08** · context to AI that it probably didn't already have. Here is a prompt that will

**4:10** · already have. Here is a prompt that will run the entire bulk ingest in one

**4:12** · run the entire bulk ingest in one session. At this point, we've set up our

**4:14** · session. At this point, we've set up our system, we've ingested historical data,

**4:16** · system, we've ingested historical data, and created custom skills based on what

**4:18** · and created custom skills based on what we actually do, not hypothetical skills.

**4:21** · we actually do, not hypothetical skills. Now, this next step is the most

**4:22** · Now, this next step is the most important thing to get right so that we

**4:24** · important thing to get right so that we can create a self-improving system. Step

**4:26** · can create a self-improving system. Step three is inflow. This is about setting

**4:28** · three is inflow. This is about setting up your data pipelines. Think of your

**4:30** · up your data pipelines. Think of your system like a lake. In step two, we

**4:32** · system like a lake. In step two, we filled the lake up, but the problem is

**4:34** · filled the lake up, but the problem is if there's no new water keeping the lake

**4:36** · if there's no new water keeping the lake full, it will evaporate and no longer be

**4:39** · full, it will evaporate and no longer be useful. So, in this step, we create data

**4:41** · useful. So, in this step, we create data pipelines, which will act as rivers for

**4:43** · pipelines, which will act as rivers for our lake. And these rivers will

**4:44** · our lake. And these rivers will automatically flow into the lake, and

**4:46** · automatically flow into the lake, and you won't have to think about it. The

**4:47** · you won't have to think about it. The way we'll do this is what I call

**4:48** · way we'll do this is what I call skill-driven data ingestion. For each

**4:51** · skill-driven data ingestion. For each pipeline, we first need to set up a

**4:53** · pipeline, we first need to set up a skill that is well tested that we know

**4:55** · skill that is well tested that we know processes raw data exactly how we want

**4:58** · processes raw data exactly how we want it. In step four, we'll use this to

**4:59** · it. In step four, we'll use this to create our automated improvement loops,

**5:01** · create our automated improvement loops, but you can't do that without this

**5:03** · but you can't do that without this because this is a step where 99% of

**5:05** · because this is a step where 99% of people get it wrong. There are four

**5:06** · people get it wrong. There are four different types of data pipelines that

**5:08** · different types of data pipelines that you want to set up. Pipeline one is your

**5:09** · you want to set up. Pipeline one is your own inputs. Like I said earlier, there's

**5:12** · own inputs. Like I said earlier, there's really no better training data than your

**5:13** · really no better training data than your own conversation history with Claude.

**5:15** · own conversation history with Claude. And we process that as part of the

**5:16** · And we process that as part of the initial data dump, but we need to

**5:18** · initial data dump, but we need to continuously process this to get

**5:20** · continuously process this to get learnings from our conversation history.

**5:22** · learnings from our conversation history. So, to do this, we're going to create a

**5:23** · So, to do this, we're going to create a skill called sync Claude sessions. The

**5:26** · skill called sync Claude sessions. The skill is pretty simple. It'll take your

**5:27** · skill is pretty simple. It'll take your past conversation history, bring it into

**5:29** · past conversation history, bring it into your project, and then ingest it into a

**5:31** · your project, and then ingest it into a process folder. Here's a prompt that

**5:33** · process folder. Here's a prompt that will create this sync Claude session

**5:35** · will create this sync Claude session skill. And with every one of these

**5:36** · skill. And with every one of these prompts, when you do create these

**5:38** · prompts, when you do create these skills, it's super important that you

**5:40** · skills, it's super important that you actually test the skill. Make sure it

**5:42** · actually test the skill. Make sure it works on your machine, please. The

**5:43** · works on your machine, please. The second pipeline that you'll set up is

**5:45** · second pipeline that you'll set up is your personal ecosystem data capture.

**5:47** · your personal ecosystem data capture. Again, a lot like the bulk upload, you

**5:49** · Again, a lot like the bulk upload, you need to figure out the places where

**5:51** · need to figure out the places where you're creating data on a recurring

**5:52** · you're creating data on a recurring basis. So, for me, I hop on client and

**5:55** · basis. So, for me, I hop on client and team calls, I write Slack messages, and

**5:57** · team calls, I write Slack messages, and I post videos on YouTube. I'm really a

**5:59** · I post videos on YouTube. I'm really a simple man. So, to set this up for

**6:01** · simple man. So, to set this up for myself, here's how I would do it. First,

**6:03** · myself, here's how I would do it. First, for meetings, I would use Grainola

**6:05** · for meetings, I would use Grainola because it records in the background

**6:06** · because it records in the background without an AI bot sitting on the call,

**6:08** · without an AI bot sitting on the call, which feels a little too intrusive for

**6:10** · which feels a little too intrusive for me. And I use their MCP to pull the full

**6:12** · me. And I use their MCP to pull the full transcripts from that call and then

**6:14** · transcripts from that call and then ingest it into my project. For Slack, I

**6:16** · ingest it into my project. For Slack, I can set up a direct Slack connection in

**6:18** · can set up a direct Slack connection in Claude to pull chat history. For

**6:19** · Claude to pull chat history. For YouTube, I post videos publicly with

**6:21** · YouTube, I post videos publicly with transcripts enabled. So, I can reference

**6:23** · transcripts enabled. So, I can reference the final product to see what was

**6:25** · the final product to see what was actually said and pull that into my

**6:27** · actually said and pull that into my system. The most important thing when

**6:28** · system. The most important thing when you're thinking about all of these

**6:29** · you're thinking about all of these different nodes for data capture is make

**6:32** · different nodes for data capture is make sure that you're actually capturing the

**6:33** · sure that you're actually capturing the content. If you can't figure out the

**6:35** · content. If you can't figure out the connection today, that doesn't matter as

**6:36** · connection today, that doesn't matter as long as the raw information is there,

**6:38** · long as the raw information is there, and eventually you'll figure out the

**6:39** · and eventually you'll figure out the connection. Now, I went through the

**6:40** · connection. Now, I went through the three of those pretty quickly, but on

**6:42** · three of those pretty quickly, but on screen, this will showcase three unique

**6:44** · screen, this will showcase three unique ways to connect to external data

**6:46** · ways to connect to external data sources. Now, this may sound

**6:48** · sources. Now, this may sound complicated, but you can just lean on

**6:49** · complicated, but you can just lean on Claude to help with this connection.

**6:51** · Claude to help with this connection. Here is a prompt that will create a sync

**6:53** · Here is a prompt that will create a sync ecosystem data skill based on whatever

**6:56** · ecosystem data skill based on whatever you're trying to connect. This will go

**6:57** · you're trying to connect. This will go through each connection source, pull

**6:59** · through each connection source, pull anything that's new, and then process it

**7:01** · anything that's new, and then process it into our actual project. Pipeline number

**7:03** · into our actual project. Pipeline number three is your curated content pipeline.

**7:05** · three is your curated content pipeline. This is data from external resources

**7:07** · This is data from external resources that can help you create a better

**7:09** · that can help you create a better output. For example, this could be a

**7:10** · output. For example, this could be a book, a blog, or a YouTube video. Now,

**7:12** · book, a blog, or a YouTube video. Now, there are a lot of ways to do this, but

**7:13** · there are a lot of ways to do this, but my favorite is using newsletters because

**7:16** · my favorite is using newsletters because no matter what niche you're in, there is

**7:18** · no matter what niche you're in, there is somebody writing a newsletter with a ton

**7:21** · somebody writing a newsletter with a ton of valuable information about your

**7:23** · of valuable information about your specific topic. And the best part is

**7:25** · specific topic. And the best part is everyone watching this has an email. So,

**7:26** · everyone watching this has an email. So, if you don't want to get flooded with

**7:28** · if you don't want to get flooded with topic-specific newsletters, what you can

**7:30** · topic-specific newsletters, what you can do is add an alias domain. So, whatever

**7:32** · do is add an alias domain. So, whatever your normal email is, let's say it's

**7:34** · your normal email is, let's say it's Brad, shout out all the Brads out there,

**7:36** · Brad, shout out all the Brads out there, you would do Brad plus newsletter at

**7:38** · you would do Brad plus newsletter at gmail.com where the plus newsletter

**7:40** · gmail.com where the plus newsletter creates an email alias that lets you

**7:42** · creates an email alias that lets you easily filter for emails to that

**7:44** · easily filter for emails to that specific location. So, for example, if

**7:46** · specific location. So, for example, if you're looking for AI best practices,

**7:48** · you're looking for AI best practices, you would click the link below, which

**7:50** · you would click the link below, which has my email newsletter, which has a ton

**7:52** · has my email newsletter, which has a ton of juice, and then you would ingest that

**7:54** · of juice, and then you would ingest that into your pipeline, and you would get

**7:56** · into your pipeline, and you would get better insight in how to best use AI.

**7:58** · better insight in how to best use AI. And if needed, you can create that alias

**8:00** · And if needed, you can create that alias domain to help you with filtering. Now,

**8:01** · domain to help you with filtering. Now, the skill that will power all of this is

**8:03** · the skill that will power all of this is sync curated content. This will pull

**8:05** · sync curated content. This will pull newsletters from alias inbox, extract

**8:07** · newsletters from alias inbox, extract the key claims from each one, and then

**8:09** · the key claims from each one, and then process it into our wiki. This is

**8:11** · process it into our wiki. This is specific for email, but it's similar for

**8:12** · specific for email, but it's similar for other resources. You just need to

**8:13** · other resources. You just need to configure it based on where you want to

**8:15** · configure it based on where you want to gather the information. Now, when you're

**8:17** · gather the information. Now, when you're gathering the information, be careful

**8:18** · gathering the information, be careful not to just pump it with everything. At

**8:20** · not to just pump it with everything. At the end of the day, less is more here.

**8:23** · the end of the day, less is more here. Be very selective with what you're

**8:24** · Be very selective with what you're ingesting, because you only want

**8:26** · ingesting, because you only want high-signal resources. Pipeline number

**8:28** · high-signal resources. Pipeline number four is periodic data dumps. Similar to

**8:30** · four is periodic data dumps. Similar to the life story step earlier, I try and

**8:33** · the life story step earlier, I try and end my day or my weeks talking through

**8:35** · end my day or my weeks talking through any lessons that I learned. And this is

**8:37** · any lessons that I learned. And this is just me downloading my lived experience

**8:39** · just me downloading my lived experience into Claude to help get more context

**8:41** · into Claude to help get more context about what I'm doing. So, I'll just rant

**8:43** · about what I'm doing. So, I'll just rant into Claude code using Hex or Whisper

**8:45** · into Claude code using Hex or Whisper Flow, which are voice-to-text tools, and

**8:47** · Flow, which are voice-to-text tools, and then I'll run the add new resource

**8:49** · then I'll run the add new resource skill, which we already created to

**8:51** · skill, which we already created to ingest this information. Now, putting

**8:53** · ingest this information. Now, putting that all together, here is a single

**8:54** · that all together, here is a single prompt that will create all three of

**8:56** · prompt that will create all three of these sync skills that I've mentioned.

**8:58** · these sync skills that I've mentioned. This helps create a constant stream of

**8:59** · This helps create a constant stream of data into the data lake that you're

**9:01** · data into the data lake that you're creating. Now, one question you may be

**9:03** · creating. Now, one question you may be asking is how do we make it so that it

**9:04** · asking is how do we make it so that it automatically improves over time? We'll

**9:06** · automatically improves over time? We'll get to that in the next step. Before we

**9:08** · get to that in the next step. Before we get to that, if this is your first video

**9:10** · get to that, if this is your first video mine, welcome the channel. But if it's

**9:11** · mine, welcome the channel. But if it's your second or more, here is our

**9:12** · your second or more, here is our anti-slop agreement. The visuals, the

**9:14** · anti-slop agreement. The visuals, the testing, the hours of research that went

**9:16** · testing, the hours of research that went into this video, this is entirely built

**9:18** · into this video, this is entirely built for humans, not for these AI robot

**9:21** · for humans, not for these AI robot scrapers. So, all that I ask is you

**9:23** · scrapers. So, all that I ask is you subscribe as part of this agreement to

**9:25** · subscribe as part of this agreement to help this content reach more people.

**9:26** · help this content reach more people. Also, every video I give away a Claude

**9:28** · Also, every video I give away a Claude Max subscription. This video's winner is

**9:30** · Max subscription. This video's winner is Gregory Horn, who's building an AI

**9:32** · Gregory Horn, who's building an AI native video studio for his Hermes

**9:34** · native video studio for his Hermes agent. Now, for this video, comment

**9:36** · agent. Now, for this video, comment below with what you're building to

**9:37** · below with what you're building to enter. Now to step four, which is where

**9:39** · enter. Now to step four, which is where most people get self-improving wrong,

**9:41** · most people get self-improving wrong, and I'm going to show you why. Step

**9:42** · and I'm going to show you why. Step four, loop. Determine and set up the

**9:44** · four, loop. Determine and set up the improvement loop. Most people think

**9:46** · improvement loop. Most people think self-improving means the system runs

**9:48** · self-improving means the system runs entirely on its own without any human

**9:51** · entirely on its own without any human input. And yes, that is possible, and

**9:53** · input. And yes, that is possible, and I'm going to show you how you can do

**9:54** · I'm going to show you how you can do that, but I do want to explain the

**9:56** · that, but I do want to explain the downside of this. Let me give you a

**9:58** · downside of this. Let me give you a workout analogy that might hit home a

**10:00** · workout analogy that might hit home a little too hard for some people. Imagine

**10:02** · little too hard for some people. Imagine a system that was automatically

**10:03** · a system that was automatically improving your fitness. So the scenario

**10:05** · improving your fitness. So the scenario one, a fully automated system. This

**10:07** · one, a fully automated system. This system will work out for you. You don't

**10:09** · system will work out for you. You don't have to lift a finger, and you get

**10:10** · have to lift a finger, and you get jacked without any effort. Now that

**10:12** · jacked without any effort. Now that sounds amazing, but what if the system

**10:14** · sounds amazing, but what if the system only ever trains chest? Six months from

**10:16** · only ever trains chest? Six months from now, your chest is huge, and your legs

**10:18** · now, your chest is huge, and your legs are toothpicks. The system thought it

**10:20** · are toothpicks. The system thought it was improving you, but it was actually

**10:22** · was improving you, but it was actually breaking you. Now scenario two,

**10:23** · breaking you. Now scenario two, augmented. You get a workout plan, but

**10:25** · augmented. You get a workout plan, but before it runs it for you, you sign off

**10:28** · before it runs it for you, you sign off on what the workout is. Then it does the

**10:29** · on what the workout is. Then it does the workout without you lifting a finger.

**10:31** · workout without you lifting a finger. Both these scenarios handle the heavy

**10:32** · Both these scenarios handle the heavy lifting, but the first one just removes

**10:34** · lifting, but the first one just removes your judgment, which in some cases,

**10:36** · your judgment, which in some cases, unless you love working out only chest,

**10:39** · unless you love working out only chest, you just can't afford to lose this. So

**10:41** · you just can't afford to lose this. So when should you automate and when should

**10:42** · when should you automate and when should you review? Now I'll cover that, but

**10:44** · you review? Now I'll cover that, but first, how do we actually analyze the

**10:46** · first, how do we actually analyze the ingested data and propose improvements?

**10:49** · ingested data and propose improvements? I like having a single skill called

**10:51** · I like having a single skill called improve system. Here's a prompt to set

**10:53** · improve system. Here's a prompt to set it up, which once set up will categorize

**10:55** · it up, which once set up will categorize any improvement that you do into three

**10:57** · any improvement that you do into three buckets. Bucket one, auto approve. This

**10:59** · buckets. Bucket one, auto approve. This is low-risk stuff like data bloat,

**11:01** · is low-risk stuff like data bloat, missed linkages, obvious fixes and

**11:03** · missed linkages, obvious fixes and improvements. This is what we'll have

**11:05** · improvements. This is what we'll have Claude automatically apply as part of

**11:07** · Claude automatically apply as part of the skill. It puts it in a change log,

**11:08** · the skill. It puts it in a change log, and you don't see any of these changes

**11:09** · and you don't see any of these changes unless you want to. Bucket number two is

**11:11** · unless you want to. Bucket number two is need sign off. This is higher-stakes

**11:13** · need sign off. This is higher-stakes stuff like editing a scale or creating a

**11:15** · stuff like editing a scale or creating a new skill. Anything where the wrong

**11:16** · new skill. Anything where the wrong choice could degrade the output quality

**11:19** · choice could degrade the output quality of your system. These will get written

**11:20** · of your system. These will get written to output/review with the date.md. And

**11:23** · to output/review with the date.md. And within the file itself, there will be a

**11:24** · within the file itself, there will be a checkbox with one of three options:

**11:27** · checkbox with one of three options: approve, reject, or approve and don't

**11:29** · approve, reject, or approve and don't ask again. Bucket number three is more

**11:30** · ask again. Bucket number three is more context required. This is stuff that's

**11:33** · context required. This is stuff that's analyzed, but the skill can't decide on

**11:35** · analyzed, but the skill can't decide on its own how to handle it. Essentially,

**11:36** · its own how to handle it. Essentially, it's just things that you need to

**11:37** · it's just things that you need to provide more information on. In both

**11:39** · provide more information on. In both buckets two and bucket three, what needs

**11:41** · buckets two and bucket three, what needs approval and what needs more context,

**11:43** · approval and what needs more context, get added to the same file, so you can

**11:45** · get added to the same file, so you can review it all at once. On screen, you

**11:46** · review it all at once. On screen, you can see what an example review file

**11:48** · can see what an example review file looks like as the system suggests

**11:50** · looks like as the system suggests improvements, which I use in Obsidian to

**11:52** · improvements, which I use in Obsidian to view it. And now you may be asking, what

**11:54** · view it. And now you may be asking, what if I want to automatically approve

**11:56** · if I want to automatically approve everything? And you can, you can just

**11:57** · everything? And you can, you can just adjust the skill accordingly, but I do

**11:59** · adjust the skill accordingly, but I do want you to be aware of the spectrum and

**12:01** · want you to be aware of the spectrum and the pros and cons of it. On one end of

**12:03** · the pros and cons of it. On one end of the spectrum, you have full automation.

**12:05** · the spectrum, you have full automation. This is where you auto approve anything,

**12:06** · This is where you auto approve anything, and it requires the least amount of

**12:08** · and it requires the least amount of work, but it's the most likely to lead

**12:10** · work, but it's the most likely to lead to system drift. And then on the other

**12:12** · to system drift. And then on the other end is review every change. This is

**12:15** · end is review every change. This is safe, but it's too much work and you're

**12:17** · safe, but it's too much work and you're likely just not going to do it. The

**12:18** · likely just not going to do it. The bucketing strategy, which is what I just

**12:20** · bucketing strategy, which is what I just went through, is exactly where I sit,

**12:22** · went through, is exactly where I sit, and it's in the middle of the spectrum.

**12:23** · and it's in the middle of the spectrum. AI handles the low stake work on its

**12:25** · AI handles the low stake work on its own, and you only handle what is

**12:26** · own, and you only handle what is considered high stakes calls. And over

**12:28** · considered high stakes calls. And over the time, the system will learn what is

**12:30** · the time, the system will learn what is high stakes and what isn't. We're having

**12:31** · high stakes and what isn't. We're having AI make the easy calls, and I prefer

**12:34** · AI make the easy calls, and I prefer making the hard ones. So at this point,

**12:35** · making the hard ones. So at this point, we understand the tradeoffs, and we've

**12:37** · we understand the tradeoffs, and we've decided to go with a bucketed approach.

**12:39** · decided to go with a bucketed approach. But how do we begin and start automating

**12:41** · But how do we begin and start automating the entire thing? We're going to use

**12:42** · the entire thing? We're going to use Claude Code's desktop app to create

**12:44** · Claude Code's desktop app to create routines. Routine one is data ingestion.

**12:47** · routines. Routine one is data ingestion. Routines are how you schedule things to

**12:49** · Routines are how you schedule things to run inside the desktop app. We're going

**12:51** · run inside the desktop app. We're going to set up local routines because this

**12:53** · to set up local routines because this gives it direct access to your file

**12:55** · gives it direct access to your file system, so you can easily edit and

**12:57** · system, so you can easily edit and manage files without worrying about

**12:59** · manage files without worrying about version control. To get to this, you can

**13:00** · version control. To get to this, you can go to routines and then click the

**13:02** · go to routines and then click the drop-down and then select local. To help

**13:04** · drop-down and then select local. To help simplify all the data ingestion into a

**13:06** · simplify all the data ingestion into a single routine, I create a skill called

**13:08** · single routine, I create a skill called /dataingestion.

**13:09** · /dataingestion. This is an orchestration skill that runs

**13:11** · This is an orchestration skill that runs the three skills that we created

**13:12** · the three skills that we created earlier, sync Claude sessions, sync

**13:14** · earlier, sync Claude sessions, sync ecosystem data, and sync curated content

**13:17** · ecosystem data, and sync curated content skills. Using this prompt, which will

**13:18** · skills. Using this prompt, which will create it, I then create a new routine

**13:21** · create it, I then create a new routine and have it run this data ingestion

**13:23** · and have it run this data ingestion skill on Tuesdays, and then another one

**13:25** · skill on Tuesdays, and then another one for Fridays at 9:00 a.m. And the actual

**13:27** · for Fridays at 9:00 a.m. And the actual routine is super simple. I just have it

**13:30** · routine is super simple. I just have it reference the skill I've already

**13:31** · reference the skill I've already created. The key to any successful

**13:33** · created. The key to any successful routine is you want to reference skills

**13:35** · routine is you want to reference skills so that it's easy to update. And so if

**13:37** · so that it's easy to update. And so if you update the skill directly through

**13:38** · you update the skill directly through Claude code, it'll automatically update

**13:40** · Claude code, it'll automatically update the routine. The second routine we'll

**13:42** · the routine. The second routine we'll create is system improvements. I then do

**13:44** · create is system improvements. I then do the same thing for the slash improve

**13:46** · the same thing for the slash improve system skill. This will run at the end

**13:48** · system skill. This will run at the end of the day on Tuesday and on Fridays,

**13:50** · of the day on Tuesday and on Fridays, where it will review the data ingested

**13:52** · where it will review the data ingested earlier in the day and suggest

**13:53** · earlier in the day and suggest improvements. The reason I've separated

**13:55** · improvements. The reason I've separated these two is I feel like they're two

**13:56** · these two is I feel like they're two distinct processes, [music] and I think

**13:58** · distinct processes, [music] and I think of routines as an individual process. So

**14:01** · of routines as an individual process. So rather than bucketing, I have

**14:02** · rather than bucketing, I have individual, and that way if something

**14:04** · individual, and that way if something fails, I know which part of the process

**14:06** · fails, I know which part of the process failed. And the third routine is human

**14:08** · failed. And the third routine is human review. This is your human process, and

**14:10** · review. This is your human process, and this is so important because you are

**14:11** · this is so important because you are driving the system. And we've already

**14:13** · driving the system. And we've already created a very simple way to do this

**14:15** · created a very simple way to do this where you just have to check boxes on

**14:17** · where you just have to check boxes on what you actually want to be improved

**14:19** · what you actually want to be improved and what you don't want to be improved.

**14:21** · and what you don't want to be improved. If you want, you can make a slash human

**14:22** · If you want, you can make a slash human improve system skill, which will help

**14:24** · improve system skill, which will help you walk through the process or notify

**14:27** · you walk through the process or notify you through Slack if you are getting

**14:29** · you through Slack if you are getting lazy or I forgot to provide feedback.

**14:31** · lazy or I forgot to provide feedback. The important part here is that you are

**14:33** · The important part here is that you are part of the process because this is your

**14:35** · part of the process because this is your system and you need to own it. So far,

**14:37** · system and you need to own it. So far, we've covered the first four steps and

**14:39** · we've covered the first four steps and how this will transform how you work.

**14:40** · how this will transform how you work. But the reality is that you are the one

**14:42** · But the reality is that you are the one putting this thing together, which is

**14:44** · putting this thing together, which is why the fifth step matters the most.

**14:46** · why the fifth step matters the most. Step five, drive. Run it, don't

**14:49** · Step five, drive. Run it, don't over-engineer it. This step is the

**14:51** · over-engineer it. This step is the mindset you need to actually run the

**14:52** · mindset you need to actually run the system you just built. From first-hand

**14:54** · system you just built. From first-hand experience, you can have all the skills

**14:56** · experience, you can have all the skills and knowledge, but if you don't apply

**14:57** · and knowledge, but if you don't apply these four strategies, you are

**14:59** · these four strategies, you are absolutely cooked. The first is slow is

**15:01** · absolutely cooked. The first is slow is smooth, smooth is fast. Don't try and do

**15:03** · smooth, smooth is fast. Don't try and do everything at once. Move slow, move

**15:06** · everything at once. Move slow, move methodical. Everything in this video is

**15:08** · methodical. Everything in this video is teed up for you. Just go one step at a

**15:09** · teed up for you. Just go one step at a time and don't be discouraged. Two is

**15:12** · time and don't be discouraged. Two is you're the leader, the system serves

**15:13** · you're the leader, the system serves you. If a piece of the system isn't

**15:15** · you. If a piece of the system isn't actively making it better, just get rid

**15:17** · actively making it better, just get rid of it. You don't have to have it. If you

**15:18** · of it. You don't have to have it. If you added a skill and you don't like it,

**15:20** · added a skill and you don't like it, just delete it. You don't have to wait

**15:21** · just delete it. You don't have to wait for someone's permission to do

**15:22** · for someone's permission to do something, just do it. Three, compress

**15:25** · something, just do it. Three, compress your feedback loops. Self-improving

**15:26** · your feedback loops. Self-improving systems are valuable because they

**15:28** · systems are valuable because they compress feedback loops, but the loops

**15:30** · compress feedback loops, but the loops only learn if you're actually using the

**15:31** · only learn if you're actually using the tools, and even though it's

**15:33** · tools, and even though it's automatically improving, don't wait for

**15:35** · automatically improving, don't wait for it to automatically improve. If a skill

**15:37** · it to automatically improve. If a skill didn't work the way you wanted and you

**15:39** · didn't work the way you wanted and you already went back and forth with Claude

**15:40** · already went back and forth with Claude to actually fix the final output, just

**15:43** · to actually fix the final output, just say, "Based on this conversation,

**15:44** · say, "Based on this conversation, improve this skill." You are pushing the

**15:46** · improve this skill." You are pushing the system forward, so continuously do it.

**15:48** · system forward, so continuously do it. Four, it is not that serious, buy is to

**15:50** · Four, it is not that serious, buy is to action. People always ask me, "What tool

**15:51** · action. People always ask me, "What tool should I use? Should I make it

**15:53** · should I use? Should I make it raw/inputs? Should I make it

**15:55** · raw/inputs? Should I make it raw/sessions folder? Should I run these

**15:56** · raw/sessions folder? Should I run these things at 6:00 a.m. or 9:00 a.m.?" The

**15:58** · things at 6:00 a.m. or 9:00 a.m.?" The honest answer for any of those smaller

**16:00** · honest answer for any of those smaller things, it just doesn't matter. The only

**16:02** · things, it just doesn't matter. The only choice that's genuinely wrong is

**16:04** · choice that's genuinely wrong is overthinking it. AI is really good, so

**16:07** · overthinking it. AI is really good, so just use it and build things. These

**16:09** · just use it and build things. These systems sharpen through reps, not

**16:12** · systems sharpen through reps, not whiteboard sessions. One of my favorite

**16:13** · whiteboard sessions. One of my favorite quotes of all time is from Brian

**16:15** · quotes of all time is from Brian Armstrong, the CEO of Coinbase. He said,

**16:17** · Armstrong, the CEO of Coinbase. He said, "Action produces information." If you're

**16:19** · "Action produces information." If you're not sure if something works, just do it,

**16:22** · not sure if something works, just do it, and you'll learn faster, and you'll have

**16:23** · and you'll learn faster, and you'll have more confidence about the answer because

**16:26** · more confidence about the answer because you've already done it and you've seen

**16:27** · you've already done it and you've seen it through. And that's exactly what

**16:29** · it through. And that's exactly what we're doing with the build framework

**16:30** · we're doing with the build framework here. It's all about action over

**16:32** · here. It's all about action over analysis, so just start doing. Now, if

**16:33** · analysis, so just start doing. Now, if you like this video, you'll love this

**16:35** · you like this video, you'll love this video where I dive into loop

**16:36** · video where I dive into loop engineering, a process that you can use

**16:39** · engineering, a process that you can use in parallel with what we discussed here

**16:41** · in parallel with what we discussed here to make your self-improving system go

**16:43** · to make your self-improving system go from good to great. I'll see you in the

**16:45** · from good to great. I'll see you in the next one. Peace.
