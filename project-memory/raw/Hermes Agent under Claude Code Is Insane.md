---
title: "Hermes Agent under Claude Code Is Insane"
source: "https://www.youtube.com/watch?v=Sb96po6S67k"
author:
  - "[[AI LABS]]"
published: 2026-06-06
created: 2026-06-28
description: "Hermes use cases get serious once you connect the Hermes agent to Claude Code.  Want to go deeper into AI Agents, MCP, and LLMs?   Check out these Educative courses:   📘 Essentials..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=Sb96po6S67k)

Hermes use cases get serious once you connect the Hermes agent to Claude Code. 
Want to go deeper into AI Agents, MCP, and LLMs?  
Check out these Educative courses:  
📘 Essentials of Large Language Models: A Beginner's Journey https://www.educative.io/courses/essentials-of-large-language-models-a-beginners-journey?aff=VAbo  
🔌 MCP Fundamentals for Building AI Agents https://www.educative.io/courses/model-context-protocol?aff=VAbo  
🤖 Agentic System Design https://www.educative.io/courses/agentic-ai-systems?aff=VAbo  
🎯 LLM Bootcamp https://www.educative.io/courses/llm-bootcamp?aff=VAbo  

This is the full Hermes agent setup, how to install Hermes agent step by step, and why this Hermes AI agent unlocks AI automation other tools simply can't.

Community with All Resources: http://ailabspro.io

The Roundup: Our daily newsletter covering the AI stories.
Join now: https://www.theroundup.so/

What is the Hermes agent? It's an always-running personal agent built by Nous Research, and in this Hermes agent guide we pair it with Claude Code to automate things most people assume can't be automated.

If you've only ever leaned on assistants like ChatGPT, the gap is the self-evolving skill system. Whenever Hermes spots a reusable workflow in your chats, it saves it as a skill, and it trims its own memory files so the model stays focused instead of losing attention in a noisy context window.

We also settle the Hermes agent vs OpenClaw question. Hermes was actually built before OpenClaw, runs sandboxed by default, and handles persistent memory with token limits OpenClaw never bothered with. Its 90 bundled skills are maintained and security-scanned through the Skill Hub, which is a real difference from the unsafe OpenClaw skills we covered before.

From there it's a complete walkthrough: importing or skipping your old OpenClaw config, choosing your model, and getting the Hermes AI agent running locally or on a VPS. We also cover running Hermes as its own MCP server so Claude Code can reach everything Hermes can do.

Then we get into the real use cases. The Hermes best skills and use cases here go beyond a personal agent. There's a Slack workflow where Hermes monitors a project channel and turns the discussion into a living PRD skill, and a coding use case where Hermes runs health checks on a deployed Claude Code app and syncs its self-evolving skills back into your project. These Hermes agent real use cases are exactly the use cases for Hermes agent that make it worth setting up, and they're the same use cases Hermes owners ask about most.

One heads-up from the video: after June 15th, using your Claude subscription with third-party apps like Hermes will draw from a monthly Agent SDK credit, so now is the best time to set this up.

If AI automation and real Hermes use cases are what you're after, this is the setup to copy. The full guides live in AI Labs Pro.

Hashtags
#ai #claudecode #hermesagent #openclaw #chatgpt #seo #aiautomation #hermesusecases

## Transcript

_Caption track: English auto-generated or provided._

**0:00** · You've probably already heard by now

**0:01** · that the Hermes agent is the most

**0:03** · powerful personal agent around and

**0:05** · that's not wrong. It actually has

**0:06** · numerous features that make it so much

**0:08** · better than Open Claw. But what happens

**0:10** · when you connect it to one of the most

**0:12** · powerful coding agents out there, Claude

**0:13** · Code? On its own, Claude Code is great,

**0:16** · but it's missing one crucial part from

**0:17** · the Hermes agent, the self-evolving

**0:19** · skill system. Paired with that, you can

**0:21** · create workflows that are so much more

**0:23** · autonomous, even for things that we

**0:25** · didn't think could be automated. But

**0:27** · other than as a personal agent, you can

**0:29** · set it for any business that wants to

**0:31** · automate their processes and it's really

**0:33** · simple. But since a lot of you might be

**0:34** · new to the Hermes agent, you don't need

**0:36** · to worry as we're going to guide you

**0:38** · through it. But before we get into the

**0:39** · setup, let's start with why the

**0:41** · self-evolving skill system matters in

**0:43** · the first place. When we came across it,

**0:46** · we figured it might actually be better

**0:47** · than Open Claw. It wasn't just some

**0:49** · random project. It's actually built by

**0:51** · Nous Research, one of the leading labs

**0:53** · in open-source AI and it has become one

**0:55** · of their most popular projects. Also,

**0:57** · here's something interesting. The Hermes

**0:59** · agent was actually built before Open

**1:01** · Claw. It just didn't get much hype at

**1:03** · first. The people over at Nous Research

**1:05** · also tried Open Claw, but they ran into

**1:07** · issues with it, so they switched to

**1:09** · their own setup. They saw its problems

**1:11** · firsthand and open-sourced their

**1:13** · solution. Most of the features Hermes

**1:14** · has are the same as Open Claws. Just

**1:16** · like Open Claw, you can connect it to

**1:18** · multiple platforms, but there are two

**1:20** · things that make it so much better. The

**1:22** · first is persistent memory and the

**1:23** · second is self-improving skills. Open

**1:26** · Claw already has persistent memory,

**1:28** · which lets it remember information about

**1:30** · you and shape its to what you like, but

**1:32** · that has its limits, too. Hermes goes

**1:34** · further. It saves those memories and

**1:36** · whenever it finds a reusable workflow in

**1:38** · your chats, it turns it into a skill.

**1:40** · Hermes' persistent memory is built on a

**1:42** · really smart setup. Hermes puts a limit

**1:44** · on how large the user.md and memory.md

**1:48** · files can be. As you're chatting with

**1:50** · the Hermes agent, it keeps updating

**1:51** · those files after each run. Now, why

**1:54** · does that limit matter? It's because of

**1:55** · how models work. Just like you, a model

**1:57** · also has a really bad attention span. It

**1:59** · can only focus on a limited amount of

**2:01** · information at a time, and it gets

**2:03** · confused when it's given a lot of

**2:05** · information. And all that information,

**2:07** · from the prompts and tools to the system

**2:09** · instructions, and on top of that your

**2:11** · own files, is fighting for the model's

**2:13** · attention in the context window. So, the

**2:15** · more you fit into that context, the more

**2:17** · the model loses focus on the actual task

**2:20** · because all the extra information

**2:21** · becomes noise to the agent. So, that

**2:23** · token limit is there to prevent this

**2:25** · from happening. Once Hermes hits the

**2:27** · token limit on the files, the model goes

**2:29** · through them and cuts out anything that

**2:31** · isn't useful. It holds the newest

**2:33** · information in memory, so the agent

**2:35** · isn't distracted by old details you

**2:37** · don't need anymore. Open Claw doesn't do

**2:39** · any of this. It just lets the memory

**2:41** · keep growing. There's another issue we

**2:43** · faced with Open Claw. To secure it, we

**2:45** · had to sandbox the agent ourselves.

**2:47** · Hermes runs in a sandbox on its own.

**2:49** · That means it runs in an isolated

**2:51** · environment where it can't reach things

**2:53** · it shouldn't or accidentally do

**2:55** · something it isn't supposed to. So, it

**2:56** · gets rid of most of the security

**2:58** · problems Open Claw had. And if you want

**3:00** · to run Hermes with a Claude code setup,

**3:02** · now's the best time to do it because

**3:04** · greedy little Dario discovered another

**3:06** · way to make money off Claude by starting

**3:08** · to charge for using your Claude

**3:09** · subscription with third-party

**3:11** · applications. After June 15th, you won't

**3:13** · be able to use your Claude code

**3:15** · subscription to run agents like Hermes

**3:17** · for free. You'll have to pay Anthropic

**3:19** · extra. Your plan will include a monthly

**3:21** · agent SDK credit, and that credit gets

**3:23** · spent whenever you connect a third-party

**3:25** · app through your subscription. The same

**3:27** · limit applies to running Claude in

**3:29** · non-interactive mode, which is the mode

**3:31** · a lot of agents use to run Claude code

**3:33** · in the background without needing any

**3:35** · permission prompts. So, until June 15th,

**3:37** · you can keep running the Hermes agent

**3:39** · without the ridiculous API costs. Now,

**3:42** · setting up the Hermes agent is actually

**3:43** · pretty simple. You just copy the install

**3:45** · command and run it in your terminal. It

**3:48** · first installs all the dependencies it

**3:50** · needs, then runs the installer in

**3:51** · interactive mode. If you want to set the

**3:53** · agent up on the News Plan where you get

**3:55** · their models and built-in tools, you can

**3:57** · go for it. But, we wanted our own setup,

**3:59** · so we went with the manual option. You

**4:01** · can also reconfigure the agent later on

**4:03** · using the Hermes setup command. This

**4:05** · step is where you set up everything the

**4:07** · agent needs. Hermes can import from your

**4:09** · previous OpenClaw settings, so it first

**4:12** · asks whether you want to bring those

**4:13** · over. You can check for yourself exactly

**4:15** · what gets brought over, which covers

**4:17** · your user profile and credentials along

**4:19** · with your skills and your soul file,

**4:21** · which is basically the agent's

**4:22** · personality and instructions. But, just

**4:24** · like how your bloodline's been passing

**4:26** · down that amazing height for

**4:27** · generations, inheriting from one agent

**4:30** · to another comes with its own issues.

**4:31** · The login details you bring over still

**4:33** · point to the same channels your OpenClaw

**4:35** · agent used, and the files OpenClaw

**4:37** · relied on don't carry over cleanly

**4:40** · because those instructions were written

**4:41** · specifically for OpenClaw. So, importing

**4:44** · them just causes problems, and that's

**4:45** · why we chose not to import ours. After

**4:48** · that, you choose which model Hermes

**4:50** · uses. We wanted it on Claude models

**4:52** · through the Anthropic subscription, but

**4:54** · when we tried it, we couldn't actually

**4:55** · use the Claude models and got an error.

**4:57** · Turns out Dario was already asking us to

**5:00** · set up that extra usage even though it's

**5:02** · not June 15th yet. So, that policy might

**5:04** · already be rolling out gradually, but it

**5:06** · might still work for you. Either way, we

**5:08** · could still use Claude code in

**5:10** · non-interactive mode right now, which is

**5:12** · what we'll be using for most of our

**5:14** · tasks anyway, and you can change your

**5:15** · model provider anytime later on. Once

**5:17** · the model is set, it asks where the

**5:20** · agent will actually run, whether that's

**5:22** · on hosting or a VPS you've set up. And

**5:24** · for those of you who don't know, a VPS

**5:26** · is basically a server you rent and run

**5:28** · yourself. But, since we have Mac minis

**5:30** · running entirely for this, we went with

**5:32** · the local option. And no, we weren't the

**5:34** · ones who caused the Mac mini shortage

**5:36** · because unfortunately, just like you,

**5:37** · our AI B2B SaaS business actually ran

**5:40** · out of funding. After that, it asks you

**5:41** · to connect whichever messaging platform

**5:43** · you want. We chose Discord, but you can

**5:45** · connect any of them. We won't walk

**5:47** · through the Discord bot setup here, but

**5:49** · you'll find the full instructions in our

**5:51** · community AI Labs Pro. Once that's done,

**5:53** · it asks a few more questions, and your

**5:55** · agent is ready. You just type Hermes,

**5:57** · and once the UI loads, you can start

**5:59** · chatting with the agent right there. In

**6:01** · order to tailor itself to what you

**6:03** · actually need, it needs information

**6:05** · about you. So, you can either keep using

**6:07** · it for a month and let it figure you out

**6:09** · on its own, or just tell it who you are

**6:10** · up front before it touches any other

**6:12** · task. If you want to set it up as a

**6:14** · personal agent, you can either give all

**6:16** · the information about yourself in the

**6:18** · chat, or if you'd rather not type it all

**6:20** · out, link it to your second brain vault

**6:22** · instead. Just give it the path to your

**6:24** · second brain, and tell it to onboard

**6:25** · itself from there. And it learns

**6:27** · everything about you that way. If you

**6:29** · want to set it up for a specific

**6:30** · automation use case, just provide the

**6:32** · docs of the use case, or the general

**6:34** · info about the company that it's being

**6:36** · set up for. But before we move forward,

**6:38** · let's have a word by our sponsor. So, if

**6:40** · you're building with AI tools every day,

**6:42** · but don't fully understand how LLMs,

**6:44** · agents, or protocols like MCP actually

**6:46** · work under the hood, that gap catches up

**6:48** · fast. That's where Educative comes in as

**6:51** · an interactive platform used by over 3

**6:53** · million developers with 2,300 plus

**6:56** · courses where you code in the browser

**6:57** · with no setup, and get AI-powered

**6:59** · feedback on every submission. I'd start

**7:01** · with their Essentials of Large Language

**7:03** · Models course. In 2 hours, it breaks

**7:05** · down how LLMs work from tokenization to

**7:07** · attention mechanisms to RAG. You'll

**7:09** · finish with a real mental model of

**7:11** · what's happening under the hood. From

**7:13** · there, MCP Fundamentals teaches you to

**7:15** · build AI agents using the Model Context

**7:18** · Protocol. Agentic System Design goes

**7:20** · further, multi-agent systems that

**7:21** · reason, plan, and act autonomously. Then

**7:23** · the 16-hour LLM Bootcamp adds hands-on

**7:26** · AWS labs in Bedrock, Sagemaker, and

**7:29** · LangGraph. You'll fine-tune a model,

**7:31** · build multi-agent systems, and ship a

**7:33** · RAG chatbot. You're writing real code

**7:35** · from the very first lesson, not sitting

**7:36** · through tutorials watching someone else

**7:38** · build. Educative has helped more than

**7:40** · 10,000 developers land jobs at top tech

**7:43** · companies. Try it free, link in the

**7:44** · description. You can build a collection

**7:46** · of skills for your Hermes agent from the

**7:48** · skill hub. That's their official

**7:50** · marketplace for skills and it has skills

**7:52** · for all kinds of use cases. Hermes also

**7:55** · comes with 90 skills installed by

**7:57** · default. Those pre-installed skills are

**7:59** · actually secure because they are

**8:01** · maintained by the organization itself.

**8:03** · That's a real difference from open claw

**8:04** · skills, which we covered in our previous

**8:06** · video. A huge number of those weren't

**8:08** · safe at all with security issues like

**8:11** · dangerous prompts and scripts that can

**8:12** · literally transfer your data off to some

**8:14** · server. And the skill hub actually runs

**8:17** · a security scan on each skill and

**8:19** · watches for these issues. That way you

**8:20** · can add the skills you want without the

**8:22** · same risk. Just like any other agent,

**8:24** · you can connect any MCP you want to

**8:26** · Hermes. But here's what separates Hermes

**8:29** · from the rest. You can run your own

**8:30** · Hermes setup as an MCP server itself and

**8:33** · connect it to your other agents, letting

**8:35** · them reach Hermes through tools so the

**8:36** · communication goes both ways. Connecting

**8:39** · Hermes to other agents this way fills in

**8:41** · what those agents are missing. An agent

**8:43** · like Claude code on its own doesn't

**8:45** · remember anything about you and its

**8:46** · skills don't fix or improve themselves.

**8:49** · But through this MCP connection, you can

**8:51** · give it access to everything Hermes can

**8:53** · do. It also means you reach every app

**8:55** · you've already connected to Hermes

**8:56** · without wiring each agent up to each app

**8:59** · separately. They just use those apps

**9:01** · through your Hermes setup instead. To

**9:03** · run Hermes as an MCP, you run the Hermes

**9:05** · MCP serve command. There's no output on

**9:07** · the terminal saying the server is up,

**9:09** · but it's actually started running as the

**9:11** · MCP server. To connect it to your agent,

**9:13** · you add the Hermes MCP to the .mcp.json

**9:17** · file and then it's usable. You can set

**9:19** · it at project scope, which means only

**9:20** · the project you're working on gets

**9:22** · access. Or you can add the config to the

**9:24** · root.cloud folder and then the Hermes

**9:26** · MCP is available across all your

**9:28** · projects. And speaking of skills, Hermes

**9:30** · comes bundled with a Claude code skill

**9:32** · which has guidance on how to use Claude

**9:34** · code through the agent. So combined with

**9:37** · the Hermes setup running as an MCP, this

**9:39** · unlocks a lot for us. The Hermes agent

**9:42** · and Claude code together open up a lot

**9:44** · of use cases, especially in businesses

**9:46** · where multiple automations can be set up

**9:48** · to handle repeatable processes. One of

**9:50** · those is connecting Claude code to your

**9:51** · team's Slack workspace. This works

**9:53** · really well because Hermes is basically

**9:55** · an always running agent, while Claude

**9:57** · code is where the actual development

**9:59** · happens. So, we use the Hermes agent to

**10:01** · access the team workspace. Just like

**10:03** · with the Discord setup, we won't walk

**10:04** · through the Slack connection here,

**10:06** · either. But, you'll find the full guide

**10:07** · in our community. In most workspaces,

**10:09** · you could have a dedicated channel for a

**10:11** · project where the whole team discusses

**10:13** · different points about it. What you can

**10:15** · do with the Hermes agent is ask it to

**10:17** · create a cron job that monitors that

**10:19** · specific channel. From the requirements

**10:21** · being discussed there, it builds a PRD

**10:23** · skill that evolves as those requirements

**10:25** · change. Having the PRD as a skill is

**10:28** · really helpful, especially during the

**10:30** · sessions where you're actually

**10:31** · developing the product. Whenever it's

**10:33** · needed, it pulls the relevant parts of

**10:35** · the PRD into the context. So, the

**10:37** · project stays aligned with the original

**10:39** · requirements. The PRD on its own might

**10:41** · work, too. But, for the same reason we

**10:43** · talked about earlier, the agent

**10:44** · sometimes gets confused about what it

**10:46** · needs to pay attention to. A skill gets

**10:48** · called whenever it's needed and stays in

**10:50** · the fresh part of the context window

**10:52** · where the model is actually paying

**10:54** · attention. So, Hermes creates the skill

**10:56** · the way you instructed and runs it every

**10:58** · 30 minutes as a cron job. This way,

**11:00** · whenever a requirement change gets

**11:01** · discussed in the channel, it updates the

**11:03** · PRD and the Hermes agent makes sure

**11:05** · those changes flow both ways. So, the

**11:07** · skill created inside your project stays

**11:09** · updated, too. At this point, you might

**11:11** · be thinking, "Since we already have an

**11:13** · MCP connected for the Hermes agent, why

**11:15** · not just use a tool to pull the

**11:17** · information from that Slack channel and

**11:19** · have the agent act on it?" The reason is

**11:21** · that the Slack MCP has a limitation. It

**11:24** · can't read the entire conversation

**11:25** · history by default. It only reads the

**11:27** · messages it's tagged in, and it won't

**11:29** · pull the full history unless the tagged

**11:31** · message specifically needs that context.

**11:33** · So, setting it up through the Hermes

**11:35** · agent is the better route because it can

**11:36** · sync the information directly from

**11:38** · there. From there, you can also ask it

**11:40** · to implement any feature using Cloud

**11:42** · Code in non-interactive mode directly

**11:44** · through the Hermes agent channels. It

**11:46** · loads that Cloud Code skill we talked

**11:48** · about earlier, then launches Cloud Code

**11:50** · and uses it to build the feature. Also,

**11:52** · if you are enjoying our content,

**11:54** · consider pressing the hype button

**11:56** · because it helps us create more content

**11:58** · like this and reach out to more people.

**12:00** · You can [snorts] also bolt Hermes onto a

**12:02** · deployed app, whether you're building it

**12:03** · for yourself or for a client. So, if you

**12:05** · have a deployed app built with Cloud

**12:07** · Code, you can create skills for

**12:09** · monitoring and health checks that guide

**12:11** · the agent on how to monitor the running

**12:13** · app because Cloud Code has the best

**12:15** · context on what the app actually needs.

**12:17** · Then, you import those skills into your

**12:19** · Hermes agent. You can set up a cron job

**12:21** · for that, basically a task that runs on

**12:23** · its own on a schedule, and let the agent

**12:25** · monitor both the hosted app and the

**12:27** · code. We also told it that if it finds

**12:29** · an issue by running the skill and

**12:31** · updates it, it should sync those skills

**12:32** · back to the local project. So, Cloud

**12:34** · Code has context on them, too. So, this

**12:36** · is how its self-evolving skills help in

**12:38** · setting up a continuous health check

**12:40** · that gets better every time it runs. So,

**12:42** · once you give Hermes the prompt, it sets

**12:44** · up the cron job for you. You can test

**12:46** · run it to see if it's configured

**12:48** · properly. It gives you a report in

**12:50** · whichever channel you set up, and in our

**12:51** · case, it reported in Discord. And with

**12:53** · the MCP configured, you can get those

**12:55** · reports right inside Cloud Code along

**12:58** · with all the suggested fixes from other

**13:00** · team members and implement them directly

**13:02** · in your project. Or, you can push those

**13:04** · fixes yourself or even set up the Hermes

**13:06** · agent to fix the issues it found using

**13:08** · Cloud Code. If you want to found the

**13:10** · next big AI B2B company and automate

**13:13** · everything like we did with Hermes, you

**13:15** · should be in AI Labs Pro. That's where

**13:17** · you'll find the setup guides from this

**13:18** · video along with all the other resources

**13:21** · and goodies we've put together. You'll

**13:22** · also get to meet a bunch of like-minded

**13:24** · nerds, including our team. The link's in

**13:26** · the description, and you can check that

**13:28** · out. That brings us to the end of this

**13:30** · video. If you'd like to support the

**13:31** · channel and help us keep making videos

**13:33** · like this, you can do so by using the

**13:35** · super thanks button below. As always,

**13:37** · thank you for watching and I'll see you

**13:39** · in the next one.
