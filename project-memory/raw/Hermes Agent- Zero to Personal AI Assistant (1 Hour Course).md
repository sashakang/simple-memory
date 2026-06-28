---
title: "Hermes Agent: Zero to Personal AI Assistant (1 Hour Course)"
source: "https://www.youtube.com/watch?v=gb5TlGw6Uks"
author:
  - "[[Nate Herk | AI Automation]]"
published: 2026-05-10
created: 2026-06-28
description: "Code NATEHERK for 10% off Hermes VPS: http://hostinger.com/natehermes My FREE AI OS Course: https://www.skool.com/ai-automation-society/about?el=hermes-course&hcategory=youtube-vid..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=gb5TlGw6Uks)

Code NATEHERK for 10% off Hermes VPS: http://hostinger.com/natehermes
My FREE AI OS Course: https://www.skool.com/ai-automation-society/about?el=hermes-course&hcategory=youtube-videos&utm_campaign=free-group
Full courses + unlimited support: https://www.skool.com/ai-automation-society-plus/about?el=hermes-course&hcategory=youtube-videos&utm_campaign=ais-plus
Apply for my YT podcast: https://podcast.nateherk.com/apply
Work with me: https://uppitai.com/

My Tools💻
FREE MONTH voice to text: https://get.glaido.com/nate
Code NATEHERK for 10% off VPS (annual plan): https://www.hostinger.com/vps/claude-code-hosting

This is a complete walkthrough of getting Hermes Agent set up from scratch on a VPS. 

You'll see how to install it on Hostinger, connect it to Telegram, set up your first skill and cron job, and back everything up to GitHub. By the end you'll understand the five pillars of Hermes, when to use it instead of Claude Code, and how to scale to multiple agents without breaking anything.

Sponsorship Inquiries:
📧 nate@smoothmedia.co

Connect with me:
https://www.linkedin.com/in/nateherkelman/
https://x.com/nateherk
https://www.instagram.com/nateherk/

TIMESTAMPS 
0:00 Intro
3:30 What Is Hermes Agent
4:30 Hermes vs Claude Code vs OpenClaw
7:30 The Five Pillars
16:30 VPS Setup
25:30 Onboarding & Telegram
33:00 GitHub Backup & First Cron
46:30 Best Practices & Security
50:30 Scaling Multiple Agents
56:00 Final Thoughts

## Transcript

_Caption track: English auto-generated or provided._

**0:00** · Hermes' agent is one of the most

**0:01** · powerful AI agents that I've ever played

**0:02** · with. So, in today's video, I'm going to

**0:04** · take you from absolutely nothing to

**0:05** · being able to get one set up. And by the

**0:07** · end, you're going to understand exactly

**0:08** · how to actually get the most out of the

**0:10** · super powerful AI agent. This is the

**0:11** · landing page for Hermes' agent. It is an

**0:13** · agent that grows with you. So, it has

**0:15** · like sort of that self-improving loop

**0:16** · with skills and stuff. So, it's very,

**0:18** · very cool. And it's a lot easier to set

**0:19** · up than you'd think. We're not going to

**0:20** · have to use a Mac mini or anything. I'm

**0:22** · going to show you how you can just set

**0:23** · one up on a private server. Now, this

**0:25** · thing out of the box is already super

**0:26** · powerful. If I go to docs and then I

**0:28** · click on skills, you can see that

**0:29** · there's like a 684 total skills, but

**0:32** · there's 91 that are already basically

**0:34** · just built in once you install Hermes.

**0:36** · So, for example, you can see that it

**0:37** · generated me some Excalidraw diagrams,

**0:39** · which we'll look at in a sec. But, I

**0:41** · didn't have it install any sort of

**0:42** · Excalidraw skill. It just had that

**0:44** · already. And I never gave it a

**0:45** · transcription skill or a voice skill,

**0:47** · but take a look at this. "Hey there,

**0:49** · sir. Can you just go ahead and tell

**0:50** · YouTube who you are, what you do, and

**0:52** · what some of your crons are?" By the

**0:54** · way, when I say cron, that basically

**0:55** · just means like an automation. It's a

**0:57** · scheduled automation. And don't worry,

**0:58** · we're going to dive into all of that

**0:59** · later in the video. I'll also talk about

**1:01** · Hermes compared to Claude code, compared

**1:03** · to Open Claw, and the differences, and

**1:04** · why in this specific video I'm going

**1:06** · with Hermes. So, you can see that it

**1:08** · shot back an actual voice note as well

**1:10** · as text. So, this is a full minute and

**1:12** · 16 seconds. I'm not going to play the

**1:13** · whole thing, but let's take a quick

**1:14** · listen. Here's a YouTube-friendly

**1:15** · version. Hey YouTube, I'm Hermes' agent.

**1:17** · I'm Nick's AI assistant running on his

**1:18** · own infrastructure. I'm not just a

**1:20** · chatbot in a browser. I can use tools,

**1:21** · remember preferences, write reusable

**1:22** · skills, run scheduled automations,

**1:23** · search past conversations, work through

**1:25** · Telegram, and help manage real

**1:26** · workflows. The way I can

**1:27** · >> All right, thank you so much, Hermes.

**1:28** · But anyways, take a look at some of

**1:29** · these crons that my Hermes is running. A

**1:31** · daily AI news briefing, which is posted

**1:33** · inside of my school community. YouTube

**1:34** · comment monitoring. So, if you guys have

**1:36** · noticed on my YouTube videos lately,

**1:37** · I've had an AI agent that has access to

**1:39** · the transcript and knowledge about me,

**1:41** · and it's been responding to you guys'

**1:42** · comments. And that is this Hermes agent.

**1:44** · School community engagement, morning

**1:45** · business summaries, server checks,

**1:47** · research reports, follow-up reminders.

**1:48** · And that's just some of the crons that I

**1:50** · have this agent working on. And if you

**1:51** · guys have seen my videos on my channel

**1:53** · about hyperframes with Claude code,

**1:55** · basically to edit videos, I wanted to

**1:56** · see if Hermes could do that. So, I said,

**1:58** · "Hey, can you make me a video using

**1:59** · HyperFrames about what Hermes Agent is,

**2:01** · how you work, how you remember things?"

**2:03** · It ran all of these different things.

**2:04** · So, it has a skill called creative. It

**2:06** · had a skill called Man in Video.

**2:08** · >> [snorts]

**2:08** · >> It was searching for Hyper. It ran all

**2:10** · these terminal commands. And it also,

**2:11** · you can see here, it's using vision to

**2:13** · analyze the actual video to see how it

**2:14** · turned out.

**2:16** · Now, its first pass wasn't great. It

**2:17** · didn't even use HyperFrames. I'm not

**2:19** · exactly sure what this used. But, as you

**2:21** · can see, some of the spacing is off.

**2:22** · It's not amazing. But, you know, it's

**2:24** · not terrible for the fact that I just

**2:25** · said, "Hey, make me a video." So,

**2:26** · basically then I said, "Okay, what tool

**2:28** · did you use? I wanted you to use

**2:29** · HyperFrames." So, it had to look into

**2:31** · it. It did the research on its own. It

**2:32** · asked me if it could install

**2:33** · HyperFrames. I said, "Yes." And then it

**2:35** · comes back with a video that's actually

**2:36** · much, much better. So, I'm not going to

**2:38** · play the whole thing, but here's the

**2:39** · video that it actually came up with. It

**2:40** · looks a lot better. The spacing is a lot

**2:42** · better. It just has these diagrams that

**2:44** · actually like don't overlap and they're

**2:45** · not going out of bounds. So, think about

**2:47** · this. One natural language request. It

**2:50** · did the research. It wrote this. And all

**2:52** · I said, as you guys can see, is, "Hey,

**2:54** · make me a video about what Hermes Agent

**2:57** · is and how your memory and skills work.

**2:58** · It should feel fast-paced and exciting."

**3:00** · So, that's one mindset shift here is if

**3:02** · you are confused about anything to do

**3:03** · with Hermes, Hermes probably understands

**3:05** · it the best and it can also look up its

**3:07** · own documentation.

**3:09** · So, just ask it, "Hey, can you do this?"

**3:10** · If you see something cool on X, grab

**3:12** · that X post, give it the link and say,

**3:14** · "Hey, read this and then help me

**3:15** · implement it." It's really going to be

**3:16** · your best friend here by just

**3:18** · brainstorming and then you tell it to go

**3:20** · figure out how to do it. Okay, so that

**3:21** · was just a quick demo about what Hermes

**3:23** · Agent looks like when I'm using it

**3:24** · through Telegram. You can use it through

**3:26** · tons of other platforms as well. So,

**3:27** · let's just actually dive into this video

**3:29** · here. Hermes Agent from zero to your own

**3:31** · assistant. Okay, so what is Hermes

**3:33** · Agent? It is an open source AI Agent

**3:35** · from News Research and it is an MIT

**3:37** · licensed, like I said, open source

**3:38** · project. Right now, it has 140,000

**3:40** · GitHub stars and that is growing really

**3:42** · fast. It's one of the fastest growing

**3:43** · open source projects on GitHub. It runs

**3:45** · on your own infrastructure, whether that

**3:46** · is a Mac mini, a laptop, a VPS. It can

**3:49** · run inside a Docker container. Wherever

**3:51** · you want to put it. It can even run on

**3:52** · an Android via Termux. There are tons of

**3:55** · different messaging platforms. I'm going

**3:56** · to be showing you guys Telegram today.

**3:57** · You could also do Discord, Slack,

**3:59** · WhatsApp. You could even do iMessage if

**4:00** · you wanted to connect it to that. And

**4:02** · really the big thing that got me

**4:04** · interested in trying it out was the

**4:05** · self-improvement over time by writing

**4:07** · its own skills and updating those. And

**4:08** · it's kind of built on top of five main

**4:10** · pillars, which I'm going to talk to you

**4:11** · guys about in just a sec here. But

**4:13** · before we get into that, I wanted to

**4:14** · cover Hermes versus Cloud Code versus

**4:16** · Open Claw and kind of even like Codex,

**4:18** · too. So, this is just my comparison of

**4:20** · the way that I compartmentalize them in

**4:22** · my head. So, Cloud Code is still my

**4:24** · daily driver. That's where I do 90% of

**4:26** · my knowledge work throughout the day.

**4:27** · But there's a clear distinction in my

**4:28** · mind between the way that I'm going to

**4:29** · use Cloud Code and Open Claw or Hermes.

**4:32** · So, this is obviously Anthropic's coding

**4:34** · assistant. It lives in your terminal

**4:36** · next to your code, and you basically sit

**4:38** · there and you drive it. You could enact

**4:40** · like dispatch or remote control to use

**4:42** · it on the go, but honestly I don't

**4:44** · really do that too much. The way I think

**4:45** · about Cloud Code is when I'm sitting

**4:46** · down at my desk or I'm on my laptop and

**4:48** · I'm doing work. Now, Open Claw is where

**4:51** · I started to play around with it. I did

**4:52** · the trading video if you guys saw that

**4:54** · with Open Claw. And the way that I

**4:55** · started to think about this was I'm not

**4:57** · going to use Open Claw or Hermes to sit

**4:58** · down and do like my knowledge work and

**5:00** · my coding. I'm going to use Open Claw

**5:02** · and Hermes when I'm on the go. When I

**5:04** · want to be on my phone and be able to

**5:05** · set up crons really quick and have

**5:07** · everything kind of just be managed right

**5:08** · there in Telegram where I can talk to

**5:10** · something and it wakes up immediately

**5:12** · and responds to me back. And it's truly

**5:13** · been a game-changer for being able to go

**5:15** · on a walk and still do work or, you

**5:16** · know, be out and about. This was created

**5:18** · by Peter Steinberger, he then joined

**5:20** · OpenAI, and Open Claw is still an

**5:22** · independent, once again, also an

**5:24** · open-source project that has over

**5:26** · 350,000 GitHub stars now. There's a much

**5:28** · larger team around Open Claw compared to

**5:30** · Hermes, and they are also doing frequent

**5:32** · updates. Also, Nvidia built Nemo Claw on

**5:35** · top of Open Claw as a separate

**5:36** · enterprise stack. Now, Hermes and Open

**5:38** · Claw may seem kind of similar when you

**5:39** · just kind of take a first glance, but

**5:41** · there are a lot of differences. Hermes

**5:43** · is also lighter, faster, focused on

**5:44** · self-improvement, and they've come out

**5:46** · and say like, "Hey, you know, this is

**5:47** · built for people that want to tinker

**5:48** · with open source models, Claude, Llama."

**5:51** · I'm not necessarily using Hermes right

**5:52** · now with open source models, but

**5:54** · definitely something that I'm going to

**5:55** · start experimenting with. But one of the

**5:56** · main reasons that I started kind of

**5:57** · switching over to Hermes was my Open

**5:59** · Claude was just kind of breaking a lot.

**6:01** · They would push a lot of updates and

**6:02** · changes, and sometimes it would just

**6:03** · like crash my Open Claude, and I'd have

**6:05** · to get in there and fix some stuff. And

**6:07** · Hermes doesn't seem to do that as much,

**6:09** · fingers crossed. But a lot of people are

**6:11** · using these all together, and I'm

**6:12** · definitely using Claude Code with Hermes

**6:14** · together, for sure. Because I mean, if

**6:16** · you think about what are your coding

**6:18** · agents actually working in, they're

**6:19** · working in some sort of directory, which

**6:21** · is just a file structure, a folder

**6:22** · structure. And all of that we want to

**6:24** · sync to GitHub. So, if you have a GitHub

**6:25** · repo of all of your knowledge, all of

**6:27** · the business context, all of your

**6:28** · skills, you can pick out any of these

**6:31** · agents, even Codex, and just plop it on

**6:33** · top of your GitHub repo, and now you can

**6:35** · play with all these different tools and

**6:36** · see how they interact. There's just a

**6:38** · little bit of difference sometimes with

**6:39** · terminology, whether that's like a

**6:40** · Claude.md or an agents.md, or, you know,

**6:43** · a couple little tiny things, but each

**6:45** · agent understands its own terminology.

**6:47** · So, if you say, "Hey, take this repo and

**6:48** · make sure you can use it," it should be

**6:50** · able to make all the changes for you

**6:51** · very quick. And I'm going to show you

**6:52** · guys a way that I use Claude Code to

**6:54** · help me manage all of my Hermes agents

**6:56** · and Open Claude agents, which makes me

**6:57** · stay way more organized. I never forget

**6:59** · things, and trust me, it's definitely a

**7:02** · game changer. So, anyways, before we

**7:03** · jump in and we start doing the install

**7:05** · and the onboarding to Hermes, I just

**7:07** · want you guys understand some of these,

**7:09** · you know, main concepts to think about,

**7:11** · which are the five pillars. And what I

**7:12** · did is I actually copied this exact five

**7:15** · pillar structure, which by the way, my

**7:16** · Hermes agent helped me think of. I

**7:18** · copied this, I pasted it into Hermes, if

**7:20** · I scroll up a little bit here, and I

**7:22** · said, "Hey, can you just use the

**7:23** · Excalidraw skill to generate diagrams

**7:25** · for all of these, and make sure that all

**7:27** · of this information is correct?" It gave

**7:29** · me a zip file right here, and I took

**7:30** · that zip file, I put it into Excalidraw,

**7:33** · and let's now take a look at these five

**7:34** · pillar diagrams. Okay. So, the first

**7:37** · pillar is memory. Memory is the small,

**7:40** · durable context that Hermes should carry

**7:41** · across sessions. So, there's two main

**7:43** · files to be thinking about when it comes

**7:45** · to memory. The first one is the user.md,

**7:48** · who you are, your style, your

**7:49** · preferences, and things that you don't

**7:51** · like.

**7:51** · The second one is the memory.md. This is

**7:54** · like the environments, the projects

**7:56** · you're working on, some of your business

**7:58** · context potentially, and these two files

**7:59** · get loaded at the session start so that

**8:01** · it always kind of knows what's going on.

**8:03** · Because the way that you want to think

**8:04** · about AI in general is that it wakes up

**8:06** · stateless, meaning it wakes up with

**8:08** · basically no memory. If you guys have

**8:09** · ever seen the movie Memento, that's kind

**8:11** · of like how agents work. So, it's your

**8:13** · job to make sure that the context that

**8:15** · gets loaded in, Claude.md, user.md,

**8:17** · memory.md, agents.md, it's your job to

**8:20** · make sure that those files are pretty

**8:21** · holistic so that every time you wake up

**8:23** · an agent, you don't feel like you're

**8:25** · repeating yourself. And don't worry,

**8:26** · these files Hermes agent understands and

**8:28** · it's automatically going to start

**8:29** · extracting things about you and

**8:31** · extracting things from your projects and

**8:33** · putting these files together so you

**8:34** · don't actually have to like manually,

**8:36** · consciously think about it. As you can

**8:37** · see, the session would start, you would

**8:39** · go ahead and start talking, building

**8:41** · skills, doing knowledge work, and as

**8:42** · you're starting to add tools, and as

**8:44** · you're starting to give more info and

**8:45** · make changes, it's going to

**8:46** · automatically come back and update these

**8:48** · files for you. Now, that doesn't mean to

**8:49** · just be completely oblivious to it. You

**8:51** · still want to say, "Hey, by the way,

**8:52** · chuck that in the memory." Or, "Hey,

**8:54** · make sure you don't ever do this again,

**8:55** · throw that in the user.md." Stuff like

**8:56** · that. And you see the SQL diagram wasn't

**8:58** · perfect, I had to expand that a little

**8:59** · bit, but here's some beginner nuance.

**9:01** · Save durable preferences and facts to

**9:03** · memory. Use session search for old

**9:05** · conversations. So, it's basically able

**9:07** · to store all of your sessions into a SQL

**9:10** · database and it can go search through

**9:11** · those. And do not store secrets or

**9:12** · temporary task status. So, we'll talk

**9:14** · about API keys and the way that you

**9:15** · should be putting them into your Hermes

**9:17** · agent responsibly once we get into the

**9:19** · setup. So, that is the first pillar,

**9:20** · memory.

**9:21** · The second pillar we have here is

**9:23** · skills. So, skills are procedural

**9:25** · memory, reusable playbooks for how to do

**9:27** · a task well. If you guys have already

**9:28** · been working with Codex or Claude Code

**9:30** · or all these other things, you probably

**9:31** · understand skills, but I'll give you the

**9:32** · real quick lowdown. Basically, think of

**9:34** · a skill as a recipe. Someone asks you,

**9:36** · "Hey, can you make me some chocolate

**9:37** · chip pancakes?" You want to pull up a

**9:39** · recipe, and then you're going to follow

**9:40** · that recipe to a T. And that's how your

**9:42** · pancakes turn out the same and, you

**9:44** · know, yummy every time. Otherwise, if

**9:46** · you were just going off of memory of how

**9:47** · to make the chocolate chip pancakes,

**9:49** · sometimes they might be a little more

**9:50** · burnt than the other times, sometimes

**9:51** · they would have less chocolate chips

**9:53** · than other times.

**9:54** · You just want them to be consistently

**9:56** · done in the same way, and that is your

**9:58** · skill or your recipe. So, all of these

**9:59** · skills are in a file called skill.md.

**10:02** · They have a YAML front matter, which is

**10:03** · basically just like a little front

**10:05** · matter that that tells the agent, "Hey,

**10:06** · this skill does this, so use it for X,

**10:09** · Y, and Z." And that's basically a

**10:10** · concept called progressive disclosure,

**10:12** · which helps make sure that you're not

**10:14** · loading full skills, full context load

**10:16** · into a session if you don't actually

**10:18** · need to use that skill. So, Hermes will

**10:19** · understand the use case for the skill.

**10:21** · It will then invoke the skill and read

**10:23** · it, and then it will ship that

**10:24** · information into the session and then

**10:26** · invoke the skill and do what you need.

**10:28** · And what's cool about the Hermes agent

**10:30** · is that if you're doing things

**10:31** · frequently, if you forget, "Hey, let's

**10:33** · build a skill out of this," it will

**10:34** · analyze conversations, it will analyze

**10:36** · your workflow, and it will turn things

**10:37** · into skills. And then, of course, as you

**10:39** · use skills more and more, if you're

**10:40** · giving feedback, it's going to update

**10:41** · those skills as well. As you can see,

**10:43** · these uh Excalidraw diagrams keep

**10:44** · messing up right here, which is

**10:46** · basically just the beginner nuance. So,

**10:48** · memory equals what to remember, skill

**10:50** · equals how to do it again. Hermes can

**10:52** · create or patch skills after real work.

**10:55** · So, super cool.

**10:56** · And of course, there's a skills hub. So,

**10:58** · any skills you've already built can be

**10:59** · used in Hermes, or you can go to the

**11:01** · skills hub, and you can see that there's

**11:03** · over 520 community skills. There's

**11:05** · different categories, so you can

**11:07** · definitely search through here to see

**11:08** · what you can add to your Hermes to make

**11:10** · it even more powerful. It looks like

**11:12** · there's actually 16 right here that are

**11:13** · Anthropic um

**11:15** · official skills. We have Canvas design,

**11:17** · front-end design. We have a skill

**11:19** · creator skill. So, you can pull all of

**11:21** · these into your Hermes agent super super

**11:23** · easily. You just have to basically run

**11:25** · this command, or, you know, you could

**11:27** · drop in this URL to your Hermes agent

**11:29** · and say, "Hey, install this skill right

**11:31** · now." All right, so that's pillar two.

**11:32** · Pillar three is the soul. Now, soul.md

**11:35** · basically shapes the assistant. This

**11:37** · shapes your Hermes agent. So that if you

**11:39** · have six different Hermes agents, they

**11:40** · all have basically a different vibe.

**11:43** · Some can be concise, some can be rude,

**11:45** · some can be

**11:46** · I don't know. But anyways, the soul.md

**11:48** · is another markdown file that gets put

**11:50** · into the context of the agent. And now

**11:53** · it's able to just have a bit of a

**11:53** · personality. So, if you're also letting

**11:55** · other people interact with your Hermes,

**11:57** · they will feel the personality. If your

**11:58** · Hermes is, you know, commenting on

**12:00** · YouTube videos like mine, there will be

**12:02** · some sort of personality.

**12:04** · The one in my YouTube comments, I told

**12:05** · it to be like very sarcastic, but not

**12:07** · rude. And by the way, guys, it's not

**12:08** · super super important that you need to

**12:10** · like know what a skill file looks like

**12:12** · or know exactly what a markdown file

**12:14** · looks like. But don't get intimidated.

**12:15** · Here is a skill. So, this is skill.md.

**12:18** · This one's called generate image. So,

**12:20** · everything in between these two lines up

**12:21** · here, that is the the YAML front matter

**12:24** · that I was talking about. This is what

**12:25** · your agent reads in order to understand,

**12:27** · okay, should I use this skill or not? If

**12:29** · it then decides,

**12:31** · Then it's going to read all of this

**12:33** · other stuff, which is just markdown. And

**12:35** · markdown just basically means that it's

**12:36** · using like headers and bullets, and it's

**12:38** · just a way for agents to read structure

**12:41** · within a block of text. Like this means

**12:43** · bold. Anyways, that's what a markdown

**12:45** · file is, and that's what a skill file

**12:47** · looks like. So, a soul file would look

**12:48** · like that, but there wouldn't be that

**12:50** · YAML front matter. But as you might have

**12:51** · guessed, the soul file will also evolve

**12:53** · over time based on the feedback that

**12:55** · you're giving your Hermes.

**12:57** · So, what is pillar number four? This is

**12:59** · where it gets super cool, and this is

**13:00** · one of the main value props for me over

**13:03** · something like Cloud Code is the fact

**13:05** · that I can just say, "Hey, spin up a

**13:06** · cron job to do this at this time." And

**13:08** · it just does it. Cloud Code, obviously,

**13:10** · you have your routines, you have your

**13:11** · loops, but that usually requires you to

**13:13** · leave some sort of infrastructure on.

**13:15** · Unless you're using like the that new

**13:17** · cloud routine, but you're only limited

**13:18** · to 15 of those, at least on the the max

**13:20** · plan, 15 of those a day. So, once again,

**13:23** · Hermes doesn't replace Cloud Code for

**13:24** · me, but it's kind of my on-the-go spin

**13:27** · up things really quick, and that's why I

**13:28** · love it. So, Cron's turn Hermes from

**13:30** · reactive into a proactive scheduled

**13:32** · automation, and you're still getting

**13:34** · that full agentic loop if you want it.

**13:35** · So, you could say in natural language,

**13:37** · "Hey, every morning at 6:00 a.m., I want

**13:39** · you to do X, Y, and Z." It will go ahead

**13:41** · and use a skill and use its tools to

**13:42** · create that Cron job, and then when that

**13:44** · time hits, it will basically invoke like

**13:46** · a fresh isolated session. It doesn't

**13:48** · inherit any of the context that you're

**13:50** · currently, you know, having that

**13:51** · conversation about, and then it will

**13:52** · just run that skill. After that happens,

**13:54** · it will send that result back to the

**13:55** · original chat, and it will maybe update

**13:58** · any local files or do whatever it needs

**14:00** · to do based on the skill requirements.

**14:02** · So, some useful pieces of advice down

**14:04** · here, context underscore from is to pass

**14:07** · one job output into another. Work dir

**14:09** · is, you know, work directory, and it

**14:11** · runs tools from a project folder, and

**14:13** · then you can do this flag for no agent,

**14:15** · which is just a script. So, hey, I just

**14:17** · want you to run this Python script. I

**14:18** · don't want the agentic harness loop

**14:20** · inside of that. I just want the script

**14:22** · to be ran. So, if you think back to the

**14:23** · WAT framework, workflow, agent, tools,

**14:25** · you basically just be deploying the

**14:27** · workflow on something like Modal. You're

**14:28** · not deploying the agent as well. So,

**14:30** · safety nuance, Cron sessions cannot

**14:32** · recursively create more Cron jobs. So,

**14:34** · the prompts need to be self-contained.

**14:36** · And if any of this is starting to feel a

**14:37** · little bit overwhelming, I just want you

**14:39** · to understand this terminology so that

**14:41** · when we hop into the setup and the

**14:42** · onboarding, it all clicks a little bit

**14:44** · better. So, just stick with me. All

**14:46** · right, and then the last pillar here is

**14:47** · the self-improving loop. Hermes improves

**14:49** · when useful experience gets persisted as

**14:51** · memory, skills, and searchable history.

**14:54** · So, if you think about the loop like

**14:55** · this, you do the work, the agent learns,

**14:58** · you save things to memory or to agent.md

**15:00** · or to, you know, user.md, and then you

**15:03** · turn those repeatable steps into skills

**15:05** · or your preferences into more memory.

**15:07** · And then, the agent's able to search

**15:09** · past sessions when old context matters,

**15:11** · and then you basically just go in that

**15:12** · loop over and over. So, the more you use

**15:14** · your Hermes agent, the better it's going

**15:16** · to get, and the more it's going to

**15:17** · understand you. So, the nuance here is

**15:19** · that automatic does not mean magic. The

**15:21** · loop works best when the user corrects

**15:23** · Hermes, asks it to save things to

**15:25** · memory, and lets it create and update

**15:26** · skills after you've done some complex

**15:28** · work. And there is one more kind of

**15:30** · honorable mention, which is the context

**15:32** · file. So, agents.md, if you're using

**15:34** · Codex, you know what that is. If you're

**15:35** · using Cloud Code, this is the cloud.md,

**15:37** · which is kind of just like the overall

**15:39** · project goal, kind of like the structure

**15:41** · of the project. So, this is something

**15:43** · that you're more so going to use if

**15:45** · you're like coding in different projects

**15:47** · with Hermes, and I would say more so if

**15:49** · you're in like the terminal using

**15:51** · Hermes. In today's video, I'm not going

**15:52** · to focus too hard on the terminal. I am

**15:54** · going to talk about the difference

**15:55** · between using it in the terminal or

**15:56** · using it through Telegram or whatever

**15:58** · other channel you use, but this is not

**15:59** · going to be a deep dive on Hermes in the

**16:01** · terminal because once again, any

**16:02** · terminal style work that I'd be doing, I

**16:04** · would just be doing that in Cloud Code.

**16:06** · That's the way that my workflow

**16:08** · currently exists. But anyways, this

**16:10** · honestly works pretty similar to the way

**16:11** · like the memory or the soul file works,

**16:14** · but those are all global. And this one's

**16:16** · more of like a local project. This is

**16:18** · what we're working on in this contained

**16:19** · environment. So anyways, hopefully you

**16:22** · guys aren't too bored yet. Let's

**16:23** · actually go ahead and get your guys's

**16:25** · hands-on. I am going to say before we

**16:27** · jump into this, all of this video, I'm

**16:29** · going to have broken down into a

**16:30** · resource guide, which might even be

**16:31** · helpful for you to just give your Hermes

**16:33** · agent the document and say, "Hey, help

**16:35** · me get all this set up." But if you want

**16:36** · to access that free resource guide that

**16:37** · breaks down everything that we're going

**16:38** · to talk about today, that will be in my

**16:40** · free school community. The link for that

**16:41** · is down in the description. You'll go

**16:42** · into here, you'll click on classroom,

**16:44** · you'll click on all YouTube resources,

**16:45** · and you'll be able to find every doc,

**16:47** · skill, GitHub repo, everything I've ever

**16:49** · dropped for free on YouTube right in

**16:51** · there. Okay. So, now let's get into the

**16:53** · setup of Hermes agent. All right, so the

**16:56** · way that we're going to be doing this is

**16:57** · on a VPS, which stands for a virtual

**16:59** · private server. Now, I'm going to be

**17:00** · using Hostinger for my Hermes agent. I

**17:03** · have been using Hostinger for hosting N

**17:05** · and N and for Open Claw and for Cloud

**17:07** · Code. So, this is my VPS provider of

**17:09** · choice. There's a link in the

**17:10** · description if you guys want to go here.

**17:11** · You can see there's also basically like

**17:13** · a one-click install for Hermes agent

**17:15** · when you spin up one of these VPS. So,

**17:17** · very, very cool. Now, the first thing

**17:18** · you have to do is choose the plan. So,

**17:20** · on here you can see KVM 1, 2, 4, or 8.

**17:23** · I'm just going to go ahead and start

**17:23** · with two for now. This basically just

**17:25** · changes like how much CPU and RAM you

**17:28** · have and your bandwidth in your server.

**17:30** · So, you could definitely start on one

**17:32** · and if you need to just scale up, you

**17:33** · can scale up later. But, I'm just going

**17:35** · to go ahead and pick KVM 2. And then I'm

**17:37** · just going to go ahead and click on

**17:38** · deploy. So, you have to choose your

**17:40** · period. So, 24 months, 12 months, or 1

**17:42** · month. Um I think that you should just

**17:44** · probably go for the annual at least cuz

**17:46** · you're going to save more money, but

**17:47** · also, you know, you pay about 100 bucks

**17:49** · and then you have this just set up

**17:50** · forever. And you can also, or for a

**17:53** · year, I guess. But, you can also deploy

**17:55** · multiple different Hermes agents or even

**17:57** · multiple Open Claws and Cloud Codes on

**17:59** · your VPS as long as you can support the

**18:01** · RAM and the CPU. And if you choose an

**18:03** · annual plan, so 12 months or 24, you can

**18:06** · use code NATEHERK and you can save an

**18:07** · additional 10% on that plan. So, you can

**18:10** · see right here, it says, "Hermes agent

**18:11** · auto deploys with your VPS." You can

**18:13** · also get daily auto backups and then

**18:15** · you're going to choose your server

**18:16** · location. And then once you've made your

**18:17** · payment, you just have to go ahead and

**18:19** · get started with setting up your VPS.

**18:21** · So, you'll choose your server location,

**18:23** · click on next. This is where you can see

**18:24** · the actual OS that you want to use. So,

**18:26** · I'm going to do Ubuntu and I'm going to

**18:27** · do 24.04 LTS. And what else you can see

**18:30** · here is that there's tons of different

**18:31** · apps that you could also deploy, and

**18:32** · then Nemo Claw. And this is where you

**18:34** · could come in here and you could search

**18:36** · Hermes agent as well. And if you do want

**18:37** · to do the one-click install, then go

**18:38** · ahead and do Hermes agent. But, if you

**18:40** · want to do it on the root of your VPS,

**18:42** · then just stick with me here. I'm going

**18:43** · to do a breakdown of the differences

**18:44** · there in just like a minute. So, if you

**18:46** · want to wait until you see that, then

**18:48** · just wait for a sec. So, you're going to

**18:49** · have to go ahead and create a root

**18:50** · password. I'm going to go ahead and

**18:51** · click next. If you forget that later,

**18:53** · you can obviously just um regenerate it.

**18:55** · So, it's not a huge deal, but obviously,

**18:57** · you probably want to remember that. You

**18:58** · can add a malware scanner for free, so

**19:00** · I'll just check that box and hit finish

**19:01** · setup. And now this will take just a

**19:03** · couple minutes to actually spin up your

**19:05** · VPS. So, while we're waiting for that,

**19:06** · let me talk about the difference between

**19:08** · setting it up kind of with the one-click

**19:10** · or setting it up directly at the root of

**19:13** · your VPS. Okay, so a VPS is basically

**19:15** · just a computer in the cloud that you

**19:17** · will be renting from Hostinger.

**19:19** · You will get an IP address and you will

**19:21** · get a password in order to basically SSH

**19:24** · in, which means you were just like

**19:25** · getting into that virtual private

**19:27** · computer so that you can manage the

**19:28** · files and install things, stuff like

**19:30** · that. So if you install Hermes directly

**19:32** · on the VPS, it will be at the root

**19:33** · level. And if you install it using the

**19:35** · one-click Docker image, it will be in a

**19:37** · containerized Docker environment within

**19:40** · your VPS. So I know that might make like

**19:42** · no sense at all, but here's a quick

**19:43** · visual. Your VPS has data, it has like

**19:46** · services, it has other files, and then

**19:48** · you could also put the Hermes agent

**19:49** · right there. Or you could have all of

**19:51** · your files and stuff, you know, locked

**19:53** · into the root of your VPS and then you

**19:56** · can spin up an individual container for

**19:57** · all of your different Hermes agents or

**19:59** · Open Cloud agents within the actual

**20:01** · different Docker containers. So for the

**20:02** · sake of the video, I'm going to be doing

**20:04** · the Docker container approach because

**20:05** · it's just a one-click install and it's

**20:07** · much simpler, but even the root VPS is

**20:09** · very, very simple. Now, here is

**20:11** · something that I am very, very strong on

**20:13** · that some people might disagree with me

**20:15** · and think that it's over-engineering,

**20:16** · but I think it's like why would you not

**20:18** · do this?

**20:19** · For all of my VPS agents, I have created

**20:21** · a my own Cloud Code project to help me

**20:23** · manage them. So right here you can see

**20:25** · this is called UpIt agents. If I click

**20:27** · on VPS agents, you can see that I have

**20:28** · my bull, which is my trading bot, I have

**20:30** · my main Hermes, I have my UpIt OS, and I

**20:32** · have Klaus, which was like my main

**20:33** · personal assistant. And so for each of

**20:35** · these, I can see my passwords and my

**20:37** · environment variables and I can see, you

**20:38** · know, like what's the IP address of this

**20:40** · VPS and how do we have this set up in

**20:42** · the Docker or at the root and it has an

**20:43** · information about security and

**20:45** · integrations. And basically now, I have

**20:47** · one clean place to manage all of my

**20:49** · different agents because I've got a lot

**20:50** · of different VPSs running and I don't

**20:51** · want to forget my passwords and I don't

**20:53** · want to forget like which agent is on

**20:54** · which server. So I just have this

**20:56** · project set up. So I would definitely

**20:57** · recommend you guys do this. And I'm

**20:59** · actually going to do this live with you

**21:00** · guys here to show you what I mean. So,

**21:03** · all right, we are going to go ahead and

**21:04** · set up a new VPS and we're going to do a

**21:06** · new Hermes agent. So, in the VPS_agents

**21:09** · folder, create a new subfolder called

**21:11** · YouTube Hermes. And then we're going to

**21:13** · go ahead and set up like, you know, like

**21:14** · the passwords and the configuration

**21:16** · stuff, just so that you can help me make

**21:18** · sure we maintain this project well. Now,

**21:20** · the reason I like to do this is because

**21:22** · do you think that I like understanding

**21:24** · VPSs and terminal commands and CLIs? Not

**21:26** · at all. And I'm not very good at it. So,

**21:28** · who's better at that than me? Hermes

**21:30** · agent and Cloud Code.

**21:32** · And sometimes if you're running random

**21:33** · commands and you don't know what you're

**21:34** · doing, your Hermes agent might like shut

**21:36** · down. And now I have Cloud Code to help

**21:38** · me boot it back up if I need to. And

**21:40** · this may sound scary and overwhelming,

**21:41** · but trust me, it is so, so simple. This

**21:44** · is just a good best practice to keep

**21:46** · yourself organized. Okay, so switching

**21:48** · back over to our Hostinger dashboard,

**21:50** · you can now see that we have our VPS

**21:53** · ready. So, if I click on manage VPS,

**21:55** · this opens up our main dashboard. Couple

**21:57** · things to look at. So, first of all, we

**21:59** · have our root access. This is what we

**22:01** · can actually give to Cloud Code. So, if

**22:03** · it needs to root into our

**22:05** · VPS and like look at our passwords or

**22:08** · help us fix things, it can do so. It

**22:10** · would just need the password as well.

**22:12** · So, here's where you can change that

**22:13** · root password. Down here you can see

**22:14** · your current plan. You can see when it

**22:16** · expires. You can see your, you know,

**22:17** · your analytics and server data will pop

**22:19** · up and it will show you if you need to

**22:21** · like upgrade to a higher plan. And also,

**22:23** · you can see on this left-hand side,

**22:24** · these are all the different servers that

**22:26** · I've got running, which is why I want a

**22:27** · Cloud Code project to help me keep that

**22:28** · organized. So, the other thing you can

**22:30** · do is you can change the host name. If

**22:31** · you come into here,

**22:33** · you just have to have it end in a dot

**22:34** · something. So, if I just do YouTube

**22:37** · Hermes and then I do dot VPS, I should

**22:40** · be able to get that to go through. And

**22:42** · now this host name in my dashboard will

**22:44** · change to that. So, I can just keep

**22:46** · myself a little bit more organized.

**22:47** · Okay, so the two methods, right? If you

**22:49** · want to do this at the root, you would

**22:51** · basically just open up a terminal or

**22:53** · Hostinger gives you a terminal right

**22:54** · here, which means I click on this

**22:55** · button. This opens up a terminal that

**22:57** · it's already SSH'd into our project. You

**22:59** · can see it's root at youtube-hermes. And

**23:02** · this is where you would just go ahead

**23:03** · and go to Hermes and you would just run

**23:05** · the install command. So, you would come

**23:07** · down here and you would install with

**23:08** · this one-line command and then you'd go

**23:10** · ahead and do Hermes setup and start

**23:11** · configuring your Hermes agent. But like

**23:13** · I told you guys today, what we're going

**23:14** · to do is the one-click install. So, we

**23:16** · would go over to our Docker manager and

**23:18** · this is where we'd go ahead and click

**23:19** · install. And remember how we have our

**23:21** · main server, but if we wanted to spin up

**23:23** · a bunch of different Docker containers

**23:24** · inside of this server, we could do so.

**23:26** · And that's how you could keep like

**23:27** · different Hermes agents in here and kind

**23:29** · of keep them separate. Okay, well this

**23:30** · says it's going to take 10 minutes. I

**23:32** · doubt it. Okay, yeah, it just finished

**23:33** · up. So, I'm going to click compose. I'm

**23:36** · going to go to one-click deploy and then

**23:38** · when this loads up, this is where I will

**23:39** · search for Hermes and I will click on

**23:41** · select.

**23:43** · Now, here is where you have to set an

**23:44** · admin username and an admin password for

**23:46** · your Hermes agent. I'm just going to

**23:48** · leave this as default. I'm going to copy

**23:49** · this password and what I'm going to do

**23:51** · is I'm going to go to my Cloud Code

**23:52** · project and I'm going to save the admin

**23:54** · password and username into this new one.

**23:57** · So, right here you can see it made this

**23:58** · one called youtube-hermes.

**24:01** · And what I want to do is I'm going to

**24:02** · add a new file in here, call this one

**24:04** · the dot env.

**24:05** · And then in this dot env, I'm basically

**24:07** · just going to do admin_

**24:09** · username

**24:11** · equals and then admin

**24:14** · _password

**24:16** · equals and then I'm going to paste those

**24:17** · two things in here. So, this is where I

**24:19** · can keep myself organized with that. All

**24:21** · right, so I've saved that to my dot env

**24:23** · file and now I can click deploy. And

**24:25** · this is going to spin up that container.

**24:26** · And now if we want to access this, all

**24:29** · we're going to have to do is click on

**24:30** · this little button right here that it

**24:30** · will give us, which will basically like

**24:33** · put us into that container and we can

**24:35** · chat with Hermes, we can do the

**24:36** · onboarding, we can do everything in

**24:37** · there. But this main terminal button,

**24:39** · that is going to take us to the root of

**24:41** · our VPS, not inside of this Docker

**24:43** · container. I hope I'm not losing you

**24:44** · guys. I know that it may seem like I'm

**24:46** · an expert at this stuff, but truly I'm

**24:48** · all self-taught. I ask Hermes, "Hey,

**24:50** · explain this to me." I ask Cloud Code,

**24:52** · "Hey, explain this to me." And that is

**24:54** · how I've learned all this stuff. So, So

**24:55** · really not too bad. Okay, so while

**24:56** · that's getting set up, let me go back

**24:58** · into our project that we manage our VPS

**25:00** · agents on. Let's answer some questions.

**25:02** · So, has the VPS already been provisioned

**25:04** · on Hostinger? I'm going to say yes, it's

**25:06** · already been provisioned.

**25:08** · Um

**25:09** · What's the primary scope for this

**25:10** · YouTube Hermes? I'm just going to say

**25:12** · other for now. You don't really need to

**25:13** · know that yet. Right now we're just

**25:14** · setting this up as a demo. All right,

**25:16** · Telegram bot. Um we will do a new bot

**25:18** · via Bot Father, yep. And for the LLM

**25:21** · provider, we will be using Codex GPT

**25:23** · OAuth. So,

**25:25** · I will show you guys all of that as we

**25:26** · get onboarded. By the way, the

**25:27** · speech-to-text tool that I'm using right

**25:28** · here is called Glydo. It is our

**25:30** · speech-to-text startup. I fully

**25:32** · transitioned over from Whisper to Glydo

**25:34** · and I am now official member of the

**25:35** · Glydo team. It's faster, it's completely

**25:38** · private, and it's way more gentle. So,

**25:40** · check it out. Link in the description.

**25:41** · Okay, so now you can see that this

**25:42** · Hermes agent thing is set up. All I have

**25:44** · to do now is click on open. And this is

**25:46** · where you have to go get the admin

**25:48** · username and password that you just

**25:49** · saved. So, go grab that and put it in.

**25:51** · And once you put that in, you basically

**25:52** · just start the onboarding right away.

**25:54** · So, we're going to do our quick setup.

**25:55** · So, I'm just going to go ahead and hit

**25:56** · enter. We then have to choose an

**25:57** · inference provider. So, as you can see

**25:59** · there's tons of different options, like

**26:00** · a ton of different options. But what I

**26:02** · want to do is I want to use OpenAI

**26:03** · Codex. This actually lets you take your

**26:05** · ChatGPT subscription, so 20 bucks, 100

**26:08** · bucks, 200 bucks a month, and use that

**26:10** · inside of Hermes agent instead of API

**26:12** · keys. So, it's going to be the cheapest

**26:13** · option by far besides using like

**26:16** · um you know, an open-source model. So,

**26:17** · I'm going to choose OpenAI Codex. Now,

**26:21** · what happens is it makes you go to this

**26:22** · URL, so I'm going to click on that. It

**26:23** · has you sign in to your ChatGPT account,

**26:25** · and then you have to give it access, and

**26:27** · then you have to go back into the

**26:28** · terminal. You're going to grab this

**26:30** · uh what is that? A nine-digit code and

**26:32** · copy that, and then paste that into

**26:33** · there, hit continue, and when you go

**26:35** · back to your VPS, you should be fully

**26:37** · signed in and it should authenticate.

**26:39** · There you go. Login successful. We get

**26:41** · to choose a model now, so I'm obviously

**26:42** · going to choose GPT 5.5.

**26:45** · And now we're going to set up our

**26:46** · channel. So, set up messaging now. I'm

**26:48** · going to choose that. We're going to go

**26:49** · ahead and hit space to hit Telegram.

**26:52** · This is where you could also choose some

**26:53** · other things if you want, but for now,

**26:55** · I'm just going to go Telegram and hit

**26:56** · enter.

**26:57** · And now it asks us for a Telegram bot

**26:59** · token. So, what we have to do in our

**27:01** · Telegram is we have to start a new

**27:02** · conversation with the BotFather to

**27:04** · create a new bot. So, here I am in the

**27:06** · BotFather. I'm going to do {slash} new

**27:08** · bot. It asks us for a name. This is

**27:10** · going to be YouTube

**27:12** · Hermes. And then it asks us for a bot

**27:14** · username. So, I'm going to try YouTube

**27:15** · Hermes. Oops, YouTube Hermes bot. Does

**27:17** · that work? Username is taken. Okay, an

**27:19** · absolutely

**27:20** · super ugly name, haha,

**27:22** · but that works. And now this is the

**27:24** · token right here that you're going to

**27:25** · need to copy and you're going to give to

**27:28** · um your VPS down here. So, I'm going to

**27:30** · go ahead and paste that in. It might not

**27:31** · actually appear. Sometimes it just does

**27:33** · that in the terminal, but I'm going to

**27:34** · go ahead and hit enter anyways. So, now

**27:35** · that token has been saved. And the next

**27:37** · thing you have to do is allow a certain

**27:39** · user ID. So, right now, I only want my

**27:42** · Telegram account to be able to talk to

**27:44** · our Hermes. So, we have to go get our

**27:45** · own user ID. It gives you the steps

**27:47** · right here. You have to message the user

**27:49** · info bot and it will give you your

**27:50** · number. So, once again, if you go back

**27:52** · into Telegram and just search for user

**27:53** · info bot, it will look like this. This

**27:55** · is where it gives you your ID. So,

**27:57** · you're going to go ahead and copy that

**27:58** · and paste that into VPS tele terminal

**28:01** · thingy. So, this is the home channel.

**28:02** · I'm going to say yes, this is the user

**28:04** · ID I want to use for the home channel.

**28:05** · Hit yes. And now we're basically

**28:07** · completely set up with Hermes. What do

**28:10** · we have available? So, to start off tool

**28:11** · availability, we have vision, we have

**28:14** · browser automation, we have image gen,

**28:15** · we have text to speech, we have terminal

**28:17** · commands, task planning, and skills.

**28:20** · We also have different files. So, here's

**28:21** · our settings, here's our API keys,

**28:23** · here's our data, here is how we can edit

**28:25** · configuration. So, what I'm going to do

**28:27** · is I'm just going to copy all of this,

**28:28** · right? I'm going to take all of this and

**28:30** · I'm going to go ahead and hit copy and

**28:31** · I'm going to go back into our Cloud Code

**28:32** · project, paste that in, and then just

**28:34** · say,

**28:35** · All right, so we just set up this Hermes

**28:37** · agent and here is all the information

**28:39** · that it gave us. So, make sure you save

**28:41** · this. So, later if I need help with

**28:42** · tools or skills or files, you know

**28:45** · exactly how to help us do that. So,

**28:47** · hopefully now you guys are starting to

**28:48** · understand the value. If you're ever

**28:49** · getting confused on something with your

**28:51** · Hermes or your VPS, you just open this

**28:53** · up and say, "I'm working on this agent.

**28:54** · I need help with X, Y, and Z." I've

**28:56** · actually saved myself a ton of times

**28:57** · doing this. And also, when you want to

**28:58** · start thinking about security and maybe

**29:00** · getting a firewall on your VPS and

**29:02** · locking it down a little bit, which I

**29:03** · definitely recommend you should look

**29:04** · into, that is something that Cloud Code

**29:06** · is going to help you out with big time.

**29:08** · But, Hermes can also help you out with

**29:09** · that, too. Um I have my Hermes agents

**29:11** · doing like a nightly sweep of just

**29:13** · making sure that things are kind of

**29:14** · locked down in the right spots. But,

**29:15** · anyways, now you can see it says, "Do

**29:16** · you want to launch Hermes chat now?" I'm

**29:18** · going to say, "Yes." And this pulls up

**29:21** · the command line interface for Hermes.

**29:23** · You can see it's going to load up. It's

**29:24** · going to let us chat with it right here.

**29:26** · And it's going to look kind of similar

**29:27** · to if you use Cloud Code in the

**29:29** · terminal. There we go. So, we have our

**29:31** · Hermes agent. I love this text up here.

**29:33** · We can see available tools. We can see

**29:34** · available skills. You can see there's

**29:36** · already a ton of them. There's 85

**29:37** · already installed. And we're able to see

**29:40** · our model, our context window, and how

**29:42** · long we've been in this session. So, let

**29:43** · me just make sure that our connection to

**29:44** · ChatGPT is working. I'm just going to

**29:46** · say "Hello." And awesome, it has given

**29:47** · us a response. Now, let's go ahead and

**29:49** · start our Telegram and see if we can get

**29:51** · this connected. So, this is the bot that

**29:53** · I just made. I'm going to hit start. And

**29:55** · I'm going to say "Hello." And if it's

**29:57** · working, then we'll see a typing in the

**29:58** · top left up here. But, what you'll

**30:00** · notice right now is that it's not

**30:01** · working. There's no typing. So, what I'm

**30:03** · going to do is go back into our Hermes

**30:04** · right here and say,

**30:06** · "Hey, for some reason the Telegram

**30:08** · connection doesn't seem to be working. I

**30:09** · just shot the message off and said

**30:11** · hello, and I'm not getting anything

**30:12** · back." And look at that, it's already

**30:13** · invoking a Hermes agent skill to

**30:15** · understand what's going on. It's doing a

**30:16** · plan. It's running some commands right

**30:18** · here. So, it's basically going to

**30:19** · investigate how we make sure to get this

**30:21** · Telegram connection all set up. Okay.

**30:23** · So, it actually just sent me a message.

**30:25** · It says, "Hermes gateway is back online.

**30:27** · If you sent hello, try it again." So,

**30:29** · we'll go ahead and try that again.

**30:30** · Hello.

**30:31** · And now we can see in the top left it is

**30:33** · typing. And it's actually able to

**30:35** · respond. So, it said that it found the

**30:36** · issue, the gateway was stopped, and it

**30:38** · started it again. So, that is perfect.

**30:40** · Okay. So, we are up and running. We can

**30:42** · see we now have Hermes right here. So,

**30:44** · let's just go ahead and get on board a

**30:46** · little bit with it. I'm going to say,

**30:48** · "Hey, Mr. Hermes. My name is Nate.

**30:50** · Um I want you to be my ultimate personal

**30:53** · AI assistant. So, let me know what you

**30:55** · need from me and what, you know,

**30:57** · features and stuff that you can actually

**30:59** · do for me and how you can make my life

**31:01** · easier." And once again, that is

**31:02** · actually going to be able to transcribe

**31:04** · that audio and understand it and then

**31:06** · respond to us. And what I love about

**31:07** · using Hermes, especially even if you're

**31:09** · in Telegram, you still get to see the

**31:11** · visibility of what it's doing. So, you

**31:12** · can see skill view, you can see it's

**31:14** · adding some user memory. So, it's saying

**31:16** · user's name is Nate Herk. So, as I'm

**31:18** · editing this video, I was like, "Wait a

**31:20** · minute. How did this thing know my last

**31:21** · name was Herkelman? All I said in the

**31:23** · voice message was, 'Hey, my name's

**31:24** · Nate.'" And I was like, "Oh, that's

**31:26** · scary." And then I realized

**31:29** · Telegram has my full name. So,

**31:32** · yeah. And then it goes ahead and

**31:33** · responds with a bunch of stuff. So,

**31:35** · "Great to meet you. I've saved your name

**31:36** · and that you want me to operate as a

**31:37** · serious personal AI assistant. Here's

**31:39** · what I can do. I can do admin stuff. I

**31:41** · can do research. I can do coding,

**31:43** · automation, files and documents, voice.

**31:46** · Here's some stuff I need from you." So,

**31:47** · this is where you'll probably just want

**31:48** · to yap to this thing for 5 to 10

**31:50** · minutes. Tell it about your goals, tell

**31:52** · it about what you're working on, tell it

**31:53** · about your team, tell it about skills

**31:55** · that already exist that you have, and

**31:56** · just giving it some more information so

**31:58** · it knows you a little bit better. Now,

**31:59** · what this is going to start to do is

**32:00** · it's going to start to build its own

**32:02** · environment, right? It's going to build

**32:03** · those files that we mentioned and it's

**32:04** · going to potentially start to build out

**32:05** · the whole infrastructure for skills and

**32:07** · other stuff. So, the first thing that I

**32:09** · think that everyone needs to do when

**32:10** · they set up a Hermes agent is they need

**32:12** · to connect it to a GitHub repo. The

**32:13** · reason being, if Hermes goes down for

**32:15** · some reason and the VPS is corrupted,

**32:17** · you still have all of that saved so you

**32:19** · could take that repo and just wake up a

**32:21** · new Hermes agent and sync it to that and

**32:23** · then it's like you didn't lose anything.

**32:24** · So, that's exactly what we're going to

**32:25** · do. Before I start to give you all of

**32:27** · this information about me, I really want

**32:29** · to just make sure that we sync this

**32:31** · project to a GitHub repo. So, can you

**32:33** · just do some research and figure out how

**32:35** · how works? I can go ahead and give you

**32:37** · whatever you need as far as an API key

**32:39** · or um information about my GitHub

**32:41** · account so that you can create this, but

**32:43** · I want you to set this up as a private

**32:44** · repo for me. And so, what this is going

**32:46** · to do, it's going to do research. I'm

**32:47** · going to show you guys how we give it

**32:49** · that API key in a safe way, and it's

**32:51** · also going to help us figure out, you

**32:53** · know, it's going to probably build a

**32:54** · skill around this. And then, what we're

**32:55** · going to do is we're going to turn it

**32:56** · into a cron so that every single day at

**32:58** · midnight or something, it automatically

**33:00** · backs up everything that we did. So,

**33:01** · every day, if we ever make changes, our

**33:03** · repo is committing every single day

**33:05** · automatically. You can see it's viewing

**33:07** · different skills. It already has two

**33:08** · skills for GitHub repo management and

**33:10** · GitHub off, which is awesome. It's

**33:11** · running some terminal stuff. It's

**33:12** · searching through some files. I'll check

**33:14** · in with you guys once we have an action

**33:16** · to take. And while it's doing that, let

**33:17** · me just show you guys. So, if you've

**33:18** · never used GitHub before, don't be

**33:20** · intimidated. It is basically just think

**33:22** · about it like a like a shared drive,

**33:24** · like a one drive. It's a place for you

**33:26** · to store your projects and your code

**33:27** · bases. And that way, if you wanted to

**33:30** · pick up on your laptop or on a different

**33:32** · device, you could still access all of

**33:33** · those files. So, it's really important

**33:35** · that we're going to set up this

**33:36** · automated backup. It's completely free

**33:38** · to set up. Go to GitHub and get an

**33:39** · account set up. And now, we got a

**33:41** · response here that says, "Okay, I

**33:43** · checked the environment and I researched

**33:45** · the clean setup path. Git is installed,

**33:47** · but the CLI is not installed." But, it

**33:49** · actually said, "Okay, we're going to do

**33:50** · the API with a personal access token.

**33:52** · So, create a private repo, initialize

**33:54** · Git locally, and add a safe.gitignore

**33:57** · to make sure that our API keys and our

**33:59** · secrets don't get pushed to this repo,

**34:00** · even though we're going to keep it

**34:01** · private, still best practice."

**34:03** · It says, "I need you to send me these

**34:04** · four things: your GitHub username, your

**34:07** · private repo name, your Git commit

**34:09** · identity, and your GitHub token. Before

**34:11** · pushing, I'll make sure we do not upload

**34:13** · secrets that are in these files, and I

**34:15** · will also create a .gitignore so it

**34:17** · knows GitHub way better than I do,

**34:19** · probably better than you do, unless

**34:20** · you're coming from a GitHub background.

**34:22** · So, if you're curious about it, just ask

**34:24** · it, and it has these skills to manage

**34:25** · GitHub repos." And now, what's

**34:27** · interesting is if I actually go and give

**34:29** · it my personal access token, it should

**34:31** · be able to set up the repo. So, I don't

**34:32** · want to manually click around and do

**34:33** · that. Let's see if it can do it for us.

**34:35** · But, what I do need to do is get our

**34:37** · token. So, I'm going to click on this

**34:38** · link it gave us. That opens up my

**34:39** · GitHub. I'm going to go ahead and

**34:40** · generate a new token. So, I'm going to

**34:42** · do a fine-grained new token. I'm going

**34:45** · to real quick authenticate. Token name,

**34:47** · we're going to call this the YouTube

**34:49** · Hermes. I'm going to just have this one

**34:51** · Probably you want this to never expire,

**34:53** · but because I'm going to delete this

**34:54** · right after the video, I'll just keep it

**34:55** · at 30 days. You can do public, you can

**34:57** · do all, or you can do select. And so,

**34:59** · this is I guess the point where you

**35:00** · would probably want to make the repo if

**35:02** · you want it to only sync to that one.

**35:03** · So, I'm just going to go ahead and say

**35:04** · all repos. And then for permissions,

**35:06** · what we need to do is we want to do

**35:08** · contents, and we want to make sure that

**35:10** · this is read and write. So, it can pull

**35:12** · in stuff, but also push updates every

**35:14** · night. We're going to go ahead and

**35:15** · generate that token, and I am going to

**35:18** · now just have to copy this and show you

**35:20** · guys how we give it to Hermes. Because

**35:22** · what you might be tempted to do is just

**35:24** · drop it in the chat. And honestly, like

**35:26** · depending on the model you're using, it

**35:27** · might not be a huge deal, but it's just

**35:28** · not best practice. And if you do

**35:30** · accidentally do it, and it's going to,

**35:31** · you know, OpenAI servers, then you can

**35:33** · just rotate it. So, it's not a big deal.

**35:35** · If you're using an open-source model and

**35:37** · it's completely local and private, then

**35:38** · you could just drop it in because Hermes

**35:40** · obviously will take it, put it into the

**35:42** · .env, and put it where it needs to go,

**35:44** · which is which is nice, but then it's in

**35:45** · the conversation history. So, the way

**35:47** · that we're going to do this is we're

**35:48** · actually going to go back to the VPS,

**35:50** · and then you're going to go ahead right

**35:51** · here and click on open.

**35:52** · And what this is going to do is

**35:53** · obviously open up that chat, but we're

**35:55** · going to try to get out of the Hermes

**35:56** · chat and just get into like this Docker

**35:57** · container. So, I'll hit Ctrl C.

**35:59** · Now, what I can do is Hermes config set

**36:03** · all caps GitHub_token.

**36:06** · Hit space, and now I can paste in that

**36:08** · GitHub token. And when I hit enter, that

**36:11** · basically sets that in the

**36:12** · /opt/data/.env.

**36:15** · So, now we have put this token into that

**36:18** · .env file inside of our VPS without

**36:21** · putting it into the AI conversation

**36:23** · window. And this is the way that you

**36:24** · should be setting up all of your API

**36:25** · keys in here. So, now if I say, all

**36:28** · right, so I just dropped in my API key

**36:31** · for GitHub

**36:32** · in the .env file. It is called

**36:35** · GitHub_token.

**36:37** · So, see if that works. And then what I

**36:39** · want you to do is actually just create

**36:40** · the repo for me. My GitHub username is

**36:42** · NateHarkAI. My commit identity can just

**36:45** · be NateHark. And you can call this repo

**36:47** · whatever you want. And make sure it's

**36:49** · private. Okay. So, hopefully that works

**36:51** · and hopefully it's able to find that API

**36:53** · key. Let's go ahead and just see what it

**36:55** · does. Now, once again, if this stuff

**36:57** · down here is confusing you or if you

**36:58** · want to delete a key or whatever it is,

**37:00** · then you will go to your Claude code

**37:03** · project. You will give it the info it

**37:04** · needs and say, "Hey, by the way, my

**37:06** · agent is set up in a Docker container

**37:08** · and this is the name of the container

**37:10** · and here is the SSH and help me just

**37:12** · figure out where my files are or where

**37:14** · my API keys are." Okay, so that worked.

**37:16** · It found the API key, but what happened

**37:18** · is

**37:19** · we didn't give it permission to actually

**37:20** · create repos. Okay, cool. So, I'm

**37:22** · actually going to just go ahead and

**37:23** · create a new classic token. But,

**37:25** · remember, we can't have two tokens in

**37:26** · there called GitHub_token or they're

**37:28** · going to clash. So, I'm actually glad

**37:30** · this happened because what this will do

**37:32** · is it will have me have to show you guys

**37:34** · how we can delete an API key. So, I'm

**37:36** · just going to say to our Hermes,

**37:38** · "Okay, can you give me the command to

**37:40** · run inside of the terminal that we can

**37:42** · actually open up that .env file that you

**37:44** · just accessed because I need to delete

**37:46** · that GitHub token so I can give you a

**37:48** · new one."

**37:49** · All right, so we have this command which

**37:51** · is the file path for that .env. And if I

**37:54** · go to the terminal now, the one up here,

**37:56** · which is our root level VPS terminal,

**37:58** · not the Docker one, and we paste that

**38:00** · in, that should basically open up that

**38:02** · file for us. Although, it looks like

**38:04** · that we haven't actually installed nano

**38:05** · yet. So, I'm going to say,

**38:07** · when I paste it in that first one, it

**38:08** · said nano colon command not found.

**38:12** · And I know that I had this like pasted

**38:13** · in a little bit weird, but I think that

**38:14** · we still would have got this either way.

**38:16** · So, now we can just use this instead,

**38:17** · apparently. So, let's copy that and

**38:19** · let's get this pasted in here.

**38:21** · Hit enter. and now we see

**38:24** · Can you just show me how we could get

**38:25** · the nano command to work instead? And

**38:27** · just want to confirm that we should be

**38:28** · doing this on the root of the VPS, not

**38:31** · inside of the docker container image

**38:33** · that you run on. Okay, so that V1

**38:35** · command was weird, and I normally I use

**38:38** · the nano, so I just asked that question.

**38:40** · Okay, so I figured it out. What happened

**38:43** · was the agent's running inside of a

**38:45** · container, right? And then we were doing

**38:48** · looking at the root file for the .env,

**38:52** · but actually we needed to be looking at

**38:53** · the .env inside of that docker

**38:55** · container. So this is the nano command

**38:56** · that we actually need to use that gets

**38:58** · us into the docker container .env file.

**39:01** · So now you guys understand that you

**39:03** · don't have to understand like exactly

**39:05** · how all the stuff works. You just have

**39:07** · to be able to communicate clearly what's

**39:09** · wrong and what you're seeing. So I'm

**39:11** · going to go ahead and delete this GitHub

**39:12** · token,

**39:13** · and then we're going to go ahead and

**39:13** · generate the new one, and you guys are

**39:15** · going to see me put it in the same way

**39:16** · that we did earlier. What you do in here

**39:18** · is you do control O, and then you hit

**39:20** · enter, and then you do control X, and

**39:22** · that's how you save it. But now I can go

**39:24** · ahead and create a classic token instead

**39:26** · of a fine-grained. We're going to do a

**39:27** · new classic, and now we can select the

**39:29** · scopes. And this is where you would

**39:30** · choose exactly what actions you want. We

**39:33** · definitely want the repo actions to be

**39:34** · able to access public repos and

**39:37** · invitations. And this is where you might

**39:39** · want to just go through and give it like

**39:40** · read access to things, but not write

**39:41** · access to everything. But as you guys

**39:43** · can see, it's not a huge deal if you

**39:44** · need to come back in later and increase

**39:46** · or decrease the scope. So I'm just going

**39:48** · to go ahead and generate this token.

**39:49** · We're going to copy this, and we're

**39:50** · going to do that exact same thing in

**39:51** · here where we do our Hermes config set

**39:55** · GitHub_token,

**39:58** · and then

**39:59** · we paste that puppy in. And now that

**40:01** · should be set. I'm going to go back into

**40:02** · Hermes and say,

**40:04** · "Awesome. The new GitHub token that you

**40:06** · see in that .env file should be the

**40:08** · updated one. So go ahead and create that

**40:10** · private repo for us now." And what you

**40:12** · see here is even in Telegram it can ask

**40:14** · you for access to things or permissions.

**40:16** · So you can allow once, you can allow it

**40:18** · for the session, or you can always allow

**40:20** · something. So, in this case, when it is

**40:22** · creating a repo or it's going to be like

**40:23** · committing to a repo, I'm just going to

**40:25** · go ahead and do always allow so that in

**40:27** · our skill we're about to set up where it

**40:28** · does a daily sync, it just does it with

**40:30** · no problem. Okay, so that has been

**40:32** · created. It gave us a link. If I click

**40:33** · on this, it should pull up a private

**40:35** · repo right here. You can see this is

**40:37** · Hermes personal AI assistant. It's

**40:38** · private. And here are all the files that

**40:40** · it already pushed into what we're doing

**40:42** · in this project. So, if you wanted to

**40:44** · dig in, you could take a look at what is

**40:46** · here. Now that that's created, let's go

**40:47** · ahead and make a skill.

**40:49** · Awesome. So, I'm going to be using you a

**40:51** · lot and you're going to be creating

**40:52** · different skills and different memories

**40:53** · about me and stuff like that. So, what

**40:55** · we need to do is set up our first cron

**40:57** · job. And I want you to build a skill

**40:58** · around this. Basically, every single

**41:00** · night at 12:00 a.m., so midnight Central

**41:02** · Time, I want you to push changes to this

**41:06** · GitHub repo. This is going to be kind of

**41:08** · our, you know, our source of truth. So,

**41:10** · if you have any questions about that,

**41:11** · please ask. But otherwise, just go ahead

**41:13** · and set up the skill and set up the

**41:15** · cron.

**41:17** · And it's really just as simple as that.

**41:18** · In natural language, you say, "Hey,

**41:19** · every night at 12:00 a.m." Or you can

**41:21** · even do things like what I do for my

**41:23** · YouTube videos is I I drop a video and

**41:25** · then

**41:27** · I give it the link to that YouTube video

**41:28** · and I say, "Hey, for the next 12 hours,

**41:30** · run a cron every 10 minutes to go check

**41:33** · on comments and respond to them."

**41:35** · So, you can set up basically the same

**41:36** · way that like the slash loop works in

**41:38** · Cloud Code. You can say, "Hey, for the

**41:39** · next 24 hours, just do this every 5

**41:42** · minutes." And then once 24 hours has

**41:43** · passed, go ahead and kill that cron. And

**41:45** · it can do things like that as well. You

**41:47** · can see it's viewing a bunch of

**41:48** · different skills. It's going to run some

**41:49** · terminal stuff and then hopefully we're

**41:50** · going to see it create a skill and maybe

**41:52** · update some stuff in its memory. Now,

**41:54** · while this is running, there's one thing

**41:55** · that I wanted to hit on real quick,

**41:56** · which is basically like what's the

**41:57** · difference between using

**42:00** · Hermes in the terminal or using it in

**42:02** · Telegram. So, functionally, it's really

**42:04** · not all that different. It's the same

**42:07** · agent in both interfaces. Telegram does

**42:08** · not run a weaker version of it, but you

**42:11** · have a little bit less control when

**42:12** · you're using it in Telegram.

**42:15** · The CLI is kind of like the cockpit, and

**42:17** · Telegram is more like your remote

**42:18** · control. You can also set up things like

**42:20** · your dashboard, and Hermes has its own

**42:21** · Kanban board, so you can monitor like

**42:23** · tasks, which is in my opinion, I don't

**42:25** · use it at all. I think if I was doing

**42:27** · like hardcore coding and I had different

**42:28** · agents working on different things, and

**42:30** · I could view, you know, like the project

**42:32** · in a visual way, it would be super

**42:33** · helpful. But, the way that I'm using

**42:36** · Hermes Agent, like I talked about in the

**42:37** · beginning of the video, where it's kind

**42:38** · of like my on-the-go wherever AI agent,

**42:41** · I don't really need that Kanban board.

**42:42** · It's not too useful for me. But anyways,

**42:44** · that's like the mental model. The CLI,

**42:46** · which I hardly ever use, is best for

**42:49** · like deep work. You're building

**42:50** · something, you're coding, you're um you

**42:52** · know, you're living in there as kind of

**42:54** · like your operating system. And it just

**42:56** · has more like commands. You you have the

**42:59** · ability, obviously as we saw in here,

**43:00** · you can see your contacts better, you

**43:02** · can manage that better. You have all of

**43:03** · the slash commands available to you,

**43:05** · whereas in Telegram, it's not exactly

**43:06** · the same. And the session, or the

**43:08** · context window, feels a little bit more

**43:10** · ambiguous, and ultimately it is. It's

**43:12** · still doing like auto compaction and

**43:13** · stuff under the hood, but that's why I'm

**43:16** · saying like in Telegram, I'm not going

**43:17** · to be vibe coding apps and projects,

**43:19** · because I might be in context route

**43:21** · territory, and I don't have really the

**43:23** · best ability to manage that. So, for me,

**43:25** · being able to say, "Hey, check on

**43:26** · ClickUp and check in with the team and

**43:27** · do this, and you know, do this cron."

**43:29** · It's not like a super super high-risk

**43:32** · operation, which is why I'm fine having

**43:34** · less visibility into context window

**43:36** · session management, things like that.

**43:38** · So, that's what Telegram is best for,

**43:39** · schedule things, quick tasks, you know,

**43:41** · kind of your general knowledge work

**43:43** · that's not super super high-risk. Once

**43:45** · again, though, same agent, same brain,

**43:47** · same window, same skills, same memory,

**43:49** · but you lose a lot of the visibility

**43:50** · there, you lose a lot of those slash

**43:51** · commands. And

**43:54** · context, right? It's token-based. It's

**43:56** · not message-based. So, the model, no

**43:58** · matter what, is going to see your system

**43:59** · prompt, you know, your user.md, your

**44:03** · soul, all that kind of stuff. And that

**44:05** · has to fit inside the context window,

**44:07** · and it's going to be running those auto

**44:09** · compactions as you get near that. So, in

**44:11** · Telegram, it's a little bit tougher to

**44:13** · understand like, okay, where did the

**44:14** · session actually reset? And how much

**44:16** · information does it see in this current

**44:18** · working sort of memory? So, hopefully

**44:20** · that makes sense the difference between

**44:22** · CLI and Telegram, and that's why if you

**44:24** · were trying to vibe code like a hardcore

**44:27** · app or game out of Telegram, it might

**44:29** · just not feel as good as if you were

**44:31** · doing it in the CLI. But anyways, let's

**44:33** · see what's going on here. So, it set up

**44:34** · the first cron job. You can see if we

**44:36** · look at this stuff, it was able to write

**44:38** · some files, it was able to use a cron

**44:39** · job create tool. It used the cron job

**44:41** · list to see if it's there, and it also

**44:43** · updated memory at the bottom. So, that's

**44:45** · super awesome.

**44:47** · The skill is called nightly GitHub sync,

**44:49** · and it's syncing to this repo. So,

**44:52** · the container is running in UTC, so

**44:53** · instead of using a fixed UTC time that

**44:55** · would break during daylight savings, I

**44:57** · made it run hourly and self-check

**44:59** · central time.

**45:00** · So, this actually syncs to midnight my

**45:02** · time in Chicago, and it's going to

**45:06** · mirror save assistant state into the

**45:07** · repo under this branch.

**45:10** · And now what else you could do is you

**45:11** · could copy this and give this to your

**45:13** · Cloud Code project if you wanted it to

**45:14** · have this visibility. Or of course, you

**45:16** · could have your Cloud Code project look

**45:17** · at the repo you're building. However you

**45:19** · want to keep things a little bit synced

**45:20** · up, whatever makes you feel more

**45:21** · comfortable. Cuz like you don't have to

**45:22** · remember all this. Cloud Code can.

**45:24** · Hermes obviously does. Just give

**45:26** · yourself a little bit of like insurance

**45:27** · there. Anyways, that nightly sync is now

**45:29** · active, so that's great. But all right,

**45:32** · I think at this point you guys really

**45:33** · have everything that you need. You

**45:34** · understand the pillars, you understand

**45:35** · how to do API keys, and you know,

**45:37** · navigate your VPS environment. At this

**45:40** · point, it's really just a matter of

**45:42** · figuring out what workflows make sense

**45:44** · to put into your Hermes agent. So, if

**45:47** · you want to start talking about that a

**45:47** · little bit, you have two main paths to

**45:49** · have your first skill. The first one is

**45:51** · where you describe an outcome. You just

**45:52** · saw that what I did with the GitHub sync

**45:55** · cron. That was super super simple. The

**45:57** · other path is you could write your own

**46:00** · or you could install one from your cloud

**46:02** · code projects or obviously from the

**46:04** · skills library where you would click on

**46:05** · a skill and you would just run this

**46:07** · command or tell your Hermes agent to go

**46:09** · install that. So for example, if I went

**46:10** · ahead and just copied this URL, put it

**46:13** · into here and said, "I want you to go

**46:15** · ahead and real quick install the

**46:17** · hyperframes official skill from here and

**46:19** · then generate me a 5-second video which

**46:22** · is just like you introducing yourself

**46:24** · and showing me a little bit of your

**46:25** · personality. If there's anything in your

**46:26** · soul. md already. So while that's

**46:28** · running, we'll continue talking about

**46:29** · it. So and then basically as you're

**46:32** · asking it to do more things and as

**46:33** · you're asking it to work on those

**46:35** · repeatable processes, watch what

**46:37** · happens. Like I think that's what's

**46:38** · really important is to watch what it's

**46:39** · doing. You know, watch if it's viewing a

**46:40** · skill. Watch if it's running something

**46:42** · in the terminal. Because if you want it

**46:44** · to invoke a skill and it's not, then

**46:46** · that's basically an indicator for you to

**46:48** · say, "Hey, whenever I say, you know,

**46:50** · something along the lines of this, you

**46:52** · should probably be invoking that skill.

**46:53** · So go ahead and update the YAML front

**46:55** · matter so that you more accurately

**46:56** · actually call on the correct skill." And

**46:59** · from there, you just use it more and you

**47:01** · give it as much feedback as possible.

**47:02** · Give it more information about you. Now

**47:04** · a few things I wanted to touch on about

**47:06** · like the mindset of having a personal

**47:07** · assistant like this, I typically always

**47:10** · set up my Hermes agents with their own

**47:12** · accounts. So if I'm going to give this

**47:13** · thing an email address, I'm going to

**47:15** · give it its own Gmail or its own agent

**47:16** · mail account. I'm not going to give it

**47:18** · mine. Or if I am, I'm going to give it

**47:19** · an API key with very strict scopes.

**47:22** · I'm also giving all of my different

**47:23** · agents different API keys if they're

**47:25** · going to spend. So open router or

**47:27** · Perplexity, I'm going to give each one a

**47:29** · named API key so I can see which agents

**47:31** · are using how much of my money. And I

**47:33** · think best practices is like

**47:35** · pretend this is an actual intern or a

**47:37** · new employee. What access would you give

**47:39** · them? You wouldn't just give them your

**47:40** · credit card. You wouldn't just give them

**47:41** · all the stuff. So why would you do that

**47:43** · with an autonomous agent? I'm going to

**47:44** · go ahead and approve this command real

**47:45** · quick. So I think it's really important

**47:47** · to be thinking about it in that way.

**47:49** · Obviously to protect yourself and to

**47:50** · protect your business. And speaking of

**47:52** · protection, another thing that you want

**47:54** · to look at probably doing is when you

**47:55** · come into your VPS, think about how you

**47:58** · can lock this down a little bit more.

**47:59** · So, you can come over here to security

**48:01** · and you can set up a firewall. And right

**48:03** · here you can see I've got one on this

**48:05** · VPS and I think it's overall my VPS

**48:07** · called Uppet Guard, but you can set one

**48:09** · up to lock it down for like your IP and

**48:11** · to block out certain ports and stuff

**48:13** · like that. And I don't really know

**48:14** · anything about firewalls as far as like

**48:17** · formal education. I had to do my own

**48:18** · research, but guess how I set up my

**48:20** · firewall. I asked

**48:22** · Hermes and I asked Cloud Code to do

**48:24** · research, look at our environment, look

**48:26** · at our VPS, and help me figure out how

**48:28** · to lock it down. And then what you could

**48:29** · do is build skills around it where every

**48:31** · night or once a week they're doing an

**48:32** · audit on the security, they're maybe

**48:34** · trying to attack it, trying to get in,

**48:35** · and they're helping you optimize just to

**48:37** · make sure that your VPS is staying safe

**48:39** · and secure. But anyways, we're starting

**48:40** · to reach the end of this video here, so

**48:42** · I wanted to wrap up with maintaining

**48:44** · your Hermes agent. Definitely let me

**48:45** · know in the comments what else you want

**48:46** · to see with Hermes, if I can expand on

**48:48** · some stuff deeper for you guys, or

**48:49** · specific use cases. But anyways,

**48:52** · when the agent gets something wrong

**48:53** · twice, correct it on the spot and tell

**48:54** · it to update the relevant skill and or

**48:56** · memory. So, same thing, if you give the

**48:58** · same instruction twice, ask Hermes to

**48:59** · write a skill for it. When the agent is

**49:01** · too verbose or off tone, you have it

**49:03** · edit the soul.

**49:04** · When you want a new scheduled task, you

**49:05** · build a skill and then you just ask it

**49:07** · to schedule that cron. When something

**49:09** · breaks, check the memory.md. Stale

**49:11** · memory is the number one cause of weird

**49:12** · agent behavior. And this isn't a tool

**49:14** · you finish setting up, it's a teammate

**49:15** · that you keep using and you keep

**49:17** · training. And of course, you can always

**49:19** · at any time say, "Hey, read me your

**49:21** · memory file. Read me your soul file. Let

**49:23** · me see what's actually in there." And

**49:25** · it's funny, right here, remember how I

**49:26** · asked this agent to make a video about

**49:29** · itself to show me its personality? It

**49:31** · had to obviously read its own soul file

**49:34** · to know what to put inside of that

**49:36** · video. And it's only going to be a

**49:37** · 5-second video, so we'll see what it

**49:39** · really comes out as, but this is just

**49:41** · showing you how I dropped in a skill,

**49:43** · it's installing it, it's doing all the

**49:45** · hard work, and we should get an output

**49:46** · very soon. All right, fingers crossed

**49:48** · that this is good. It installed the

**49:50** · Hyperframe skill and then generated a

**49:52** · 5-second video based on its soul. I

**49:53** · don't even know what was in its soul.

**49:55** · So, let's take a look at what we got

**49:56** · here. We have Hermes, helpful,

**49:58** · knowledgeable, direct, think, build,

**50:00** · research, automate, Nate, I'm your

**50:02** · action engine. So, for a 5-second video,

**50:05** · not too bad. I turn messy goals into

**50:07** · finished actions. Yes, you absolutely

**50:09** · do, Hermes. And I didn't even give this

**50:11** · poor thing a name yet. So, from here,

**50:13** · I'm going to start building up the soul.

**50:14** · I'm going to start giving it way more

**50:15** · information about me and my business,

**50:17** · and I'm going to keep it letting it

**50:18** · build up skills and just learn more over

**50:19** · time. And that's exactly what you guys

**50:21** · should be doing now. Also, one more

**50:23** · quick thing is I obviously did this for

**50:25** · a demo, so I told it to pause that cron

**50:27** · for now, and I wanted to show you we

**50:28** · finally hit that threshold where it does

**50:30** · a compaction. So, we were at almost

**50:31** · 170,000 tokens, which is over the

**50:34** · threshold of about 136K. So, it decided

**50:37** · to go ahead and try to compress. For

**50:39** · some reason, that failed, so it inserted

**50:41** · a fallback context marker. And then we

**50:43** · can see it can use the other cron tools

**50:45** · to list and pause, and then it did a

**50:47** · memory update as well. But let's say you

**50:48** · didn't understand what these two lines

**50:50** · mean. Once again, just paste that in and

**50:51** · say, "Okay, so you just sent me these

**50:54** · messages and I don't understand what

**50:55** · that means. Explain it to me."

**50:57** · So, I'm not going to read this out right

**50:58** · now cuz I feel like I've been talking to

**50:59** · you guys for a long time. If you give

**51:02** · that a quick read,

**51:03** · go ahead and pause the video and

**51:04** · understand what that means in case you

**51:07** · get that message from your Hermes agent

**51:08** · at some point. Now, as you start to make

**51:10** · more and more of these Hermes agents, it

**51:12** · does get interesting. You have some

**51:13** · decisions to make, which is basically

**51:15** · like, "Where do they live? And when do I

**51:17** · do that? And how do they have separation

**51:20** · but still be able to talk to each

**51:21** · other?" Questions like that start to

**51:22** · come up. So, I wanted to talk a little

**51:24** · bit more about how you kind of scale

**51:26** · this up. So, if you're doing it on one

**51:28** · VPS, I think the best way to do it is to

**51:30** · have them each in their own container,

**51:32** · which is why in this setup, I decided to

**51:35** · do the one-click install, besides the

**51:36** · fact that it's very, very easy.

**51:38** · So, for example, if you guys remember,

**51:40** · we have our kind of like personal main

**51:41** · one that we set up. And remember when we

**51:43** · were trying to figure out the API keys

**51:45** · and deleting them and stuff, we figured

**51:47** · out that those API keys were stored

**51:49** · inside of that Docker container. So,

**51:51** · this agent has its own memory, its own

**51:53** · tools, and its own private keys. So,

**51:55** · then as we started to add on more, if we

**51:56** · put them in their own container as well,

**51:58** · they will all have their own keys, and

**51:59** · then they don't clash. And that's where

**52:01** · you can get more visibility as far as

**52:03** · like how often they're using their tools

**52:04** · and how much money they're costing you

**52:06** · and things like that. And that's the

**52:07** · value of having, you know, your VPS

**52:09** · being like the office building, and then

**52:10** · each agent being their own container

**52:12** · with their own passwords, you know,

**52:14** · keyboard, whatever you, you know, if

**52:16** · you're thinking like an office analogy,

**52:18** · coffee mug, whatever it is. So, that ENV

**52:20** · file, the .env, first of all, that

**52:22** · doesn't get committed to GitHub. So,

**52:24** · you're not pushing your secrets out

**52:25** · there, even though it's staying private.

**52:27** · But then, each agent's basically having

**52:29** · their own, as you can see. If you have a

**52:30** · marketing Hermes and you have a finance

**52:32** · Hermes, they will not be sharing keys.

**52:34** · They will not see each other's keys. And

**52:36** · you can use the least privilege rule,

**52:38** · which is basically give each agent only

**52:39** · the credentials and the tools needed for

**52:41** · its job. So, for example, your marketing

**52:44** · agent doesn't really need maybe read

**52:45** · access into your QuickBooks, but your

**52:47** · finance Hermes probably does. And then a

**52:49** · quick little decision tree for you guys

**52:51** · on when you should create a new Hermes,

**52:53** · because really for a while, you're

**52:55** · probably going to be all set with just

**52:56** · the one. And even if you have one main

**52:59** · one that starts doing a little bit of

**53:00** · finance stuff, some finance skills, a

**53:01** · little bit of marketing skills, what

**53:03** · happens is, okay, when you want to scale

**53:04** · up and create a dedicated finance

**53:06** · Hermes,

**53:07** · you can migrate those tools and those

**53:09** · crons and those skills super, super

**53:11** · easy. And that's the cool part about all

**53:13** · of that just living as a markdown file.

**53:15** · So, then you take those and you move

**53:16** · them over. But anyways, start with the

**53:18** · task or the role that you're thinking

**53:19** · about making an agent for. Does it need

**53:21** · different permissions, secrets, or

**53:23** · tools? If yes, go ahead and start a new

**53:25** · agent. If no, keep on moving. Does it

**53:28** · need separate longer-term memory, or

**53:30** · separate long-term memory? If yes,

**53:31** · create a new agent. If no, ask the next

**53:33** · question, which is, is it ongoing

**53:34** · repeated work? If yes, create a new

**53:36** · agent. If no, keep it in your main

**53:38** · personal, because if it's a one-off

**53:39** · task, you don't need a full new

**53:41** · container and a full new Hermes setup.

**53:43** · So, simple rule, if it needs its own

**53:45** · memory, its own tools, its own

**53:46** · credentials, its own schedule, or

**53:48** · audience, then feel free to split it up

**53:50** · into its own Hermes agent. So, I would

**53:52** · recommend that you maybe look at like a

**53:54** · road map of okay, these are maybe the

**53:55** · next one or two or three agents that I'd

**53:57** · want, but once again, I would say try to

**54:00** · get as much use out of your main

**54:02** · personal one to start just because you

**54:05** · are still learning how the skills work

**54:07** · and how to work with your Hermes and how

**54:08** · to set up everything. So,

**54:10** · limiting the amount of like distractions

**54:13** · really and just keeping one, working on

**54:15** · that one really well, you'll be able to

**54:16** · get pretty far. That's how I would

**54:18** · recommend starting out. And obviously,

**54:19** · as you start to get more, you might get

**54:21** · confused about like okay, how do I have

**54:23** · this hierarchy between them and how do I

**54:24** · make them, you know, talk and assign

**54:26** · work to each other? That is something

**54:27** · that your main Hermes agent, the one

**54:29** · that you're building right now, whether

**54:30** · you want to call that like your COO or

**54:32** · your executive assistant or whatever,

**54:34** · that main one is going to be able to

**54:36** · help you figure out all that delegation

**54:38** · and stuff like that. You just have to

**54:39** · have some conversations with it and have

**54:41** · it help you plan. But ultimately, there

**54:43** · is a point where you probably get to

**54:45** · certain scale and you need to, you know,

**54:48** · start to segment some stuff off. So, a

**54:49** · bad pattern would be one mega agent with

**54:52** · all the API keys, with all the skills,

**54:54** · with so much bloat of different tools

**54:56** · and different crons running, which could

**54:58** · cause high confusion and also high risk

**55:00** · if something happens to that one agent

**55:01** · for some reason. But as you start to

**55:03** · scale up, you can adopt a better pattern

**55:05** · where you're starting to split up

**55:06** · things, whether that's via vertical or

**55:08** · whether that's via you know, social

**55:10** · media platform or whether that's

**55:12** · whatever your separation that makes

**55:13** · sense in your business and in your

**55:14** · workflows and in your SOPs and in your

**55:16** · job descriptions, that is where you want

**55:19** · to get a little bit more separation. You

**55:21** · lower the risk, you you know, you aren't

**55:22** · putting all your eggs in one basket as

**55:24** · they say, cleaner memory and probably

**55:26** · easier debugging and better visibility.

**55:28** · So, wanted to hit on that real quick,

**55:29** · but once again, just because you can

**55:31** · spin up a bunch of agents in one VPS

**55:33** · doesn't mean you need to. So, don't

**55:35** · force it. Just let that phase happen

**55:36** · naturally once you've really felt good

**55:38** · about Hermes and once you feel like you,

**55:40** · you know, have gone through this this

**55:42** · decision tree and you hit some of these

**55:44** · criteria where you need a new one. And

**55:46** · then, of course, you can keep your Cloud

**55:47** · Code project updated and you're going to

**55:49** · be really happy that I told you to set

**55:51** · all this stuff up so you can understand

**55:52** · the different containers and the

**55:53** · different where the files are and all

**55:55** · that stuff. This is going to come in

**55:57** · handy big time for you. Now, Hermes also

**55:59** · does come with like its own dashboard

**56:01** · where you can look at the recent

**56:02** · sessions. You can see your different

**56:03** · connected platforms. And it is pretty

**56:05** · helpful, but honestly, I don't ever find

**56:07** · myself going in here because one of the

**56:10** · things that I talked about earlier is

**56:11** · the fact that I mainly like to use my

**56:13** · Hermes agents when I'm out and about and

**56:15** · I'm kind of on the go. But if I'm

**56:16** · sitting down on my computer, I'm usually

**56:18** · just working inside of Cloud Code. And

**56:20** · this dashboard, it's usually just easier

**56:22** · to open up on a local device because you

**56:24** · have to open up the tunnel and there's a

**56:25** · gateway. And you guys will understand

**56:27** · once you start setting it up. But if you

**56:28** · want to check it out, this is where you

**56:30** · can also have your Kanban board and you

**56:32** · can also look at things like, you know,

**56:33** · different keys and different configs and

**56:36** · skills and plugins. And it's just

**56:37** · basically a nice little visual dashboard

**56:39** · to see what's going on here. You can

**56:41** · also look at your crons and you can

**56:42** · create new ones from here. So, what

**56:44** · you'd do is you'd go to your Hermes

**56:45** · agent and you'd say, "Hey, I want to

**56:46** · open up the Hermes dashboard. Can you

**56:48** · help me figure it out?" What you're

**56:49** · going to need to do is you're going to

**56:50** · need to say, "Okay, here is like my VPS

**56:52** · root and here is my um Docker container

**56:55** · setup if you have that set up like

**56:57** · that." Because you have to kind of like

**56:58** · open up the gateway and make sure

**57:00** · there's a tunnel open so that you can

**57:01** · open up this local

**57:02** · um dashboard. And that's where you can

**57:04** · start to play around with this. So, the

**57:06** · first time you do it,

**57:08** · you might feel a little bit like this

**57:09** · sucks because the first time you might

**57:11** · be pasting different things around and

**57:12** · it might not feel like it's going to

**57:14** · work, but it will work. Just keep giving

**57:17** · your Hermes agent the info. Keep giving

**57:19** · it what you're doing and it will get you

**57:21** · there. And once you get there, then say,

**57:22** · "Okay, save this to your memory. Turn

**57:24** · this into a skill so that every time I

**57:25** · ask for the dashboard, you give me the,

**57:27** · you know, three commands I need to run

**57:29** · and then I just boom, boom, boom run

**57:30** · them and I'm good." So, I just wanted to

**57:31** · warn you guys about that and um you know

**57:34** · if you want to get in here and play

**57:35** · around the camera board is pretty cool

**57:36** · if you got multiple agents running you

**57:38** · can sort of like assign them to

**57:39** · different agents and they'll pick up

**57:40** · tasks and you can see them move around

**57:42** · but like I said I didn't really spend

**57:44** · too much time on this in this video

**57:45** · because I

**57:46** · don't ever find myself in this dashboard

**57:48** · but it is a nice built-in feature. So

**57:50** · anyways don't forget I'm going to put

**57:51** · all of this information that we talked

**57:52** · about today and the full setup guide and

**57:54** · all that stuff into a free resource

**57:56** · guide that you can access in my free

**57:57** · school community the link is in the

**57:58** · description. Don't forget to use the

**58:00** · link to go to Hostinger and use code

**58:01** · Nate Herc to get 10% off your annual

**58:03** · plan when you set up that VPS and yeah

**58:05** · let me know what else you guys want to

**58:06** · see with Hermes and where I can expand

**58:08** · on some stuff I'd love to bring you guys

**58:09** · some more content around what you want

**58:11** · to see. So that's going to do it for

**58:13** · today if you enjoyed the video or you

**58:14** · learned something new please give it a

**58:15** · like it helps me out a ton and as always

**58:17** · I appreciate you guys making it to the

**58:18** · end of the video and I will see you in

**58:20** · the next one. Thanks everyone.
