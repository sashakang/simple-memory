---
title: "Claude Code Works Better With Loops, Not Prompts"
source: "https://www.youtube.com/watch?v=D7TIvqtSZQE"
author:
  - "[[Eric Tech]]"
published: 2026-06-24
created: 2026-06-28
description: "Loop engineering is the shift the creators of Claude Code and OpenClaw made when they stopped prompting their agents — and I was running it in real workflows before it had a name. ..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=D7TIvqtSZQE)

Loop engineering is the shift the creators of Claude Code and OpenClaw made when they stopped prompting their agents — and I was running it in real workflows before it had a name. Here's what loop engineering is, how it works, and how I build self-correcting agentic loops in Claude Code.

Key takeaways:
- What loop engineering is: a self-correcting orchestrator → executioner → reviewer loop that iterates until your goal is met
- The 6 building blocks of a reliable agentic loop: trigger, worktree, skills, connectors, memory, sub-agents
- Using GitHub Issues as the memory/state layer so every iteration is logged and resumable
- Loopmaker: the portable Claude skill I built to scaffold a verified self-running loop with a human gate

🔗 Join our Skool community: skool.com/erictech

🔗 Get Loopmaker (free): https://free.erictech.ca/loopmaker?src=yt-loop-engineering

🔗 Check out bookzero.ai — AI-powered bookkeeping built entirely with Claude Code

📌 Mentioned videos:

- How I Make Claude Code Build Apps Autonomously: https://youtu.be/nX_bGyIOFM4

Timestamps:
0:00 Intro
1:42 How Loops Work
4:06 Why Multiple Agents
4:50 Trigger
5:03 Worktree
5:21 Skills
5:34 Connectors
7:08 Memory
7:47 Sub-Agents
8:07 Recap
10:06 Loopmaker Skill
11:04 Outro

#claudecode #aitools #loopengineering

## Transcript

_Caption track: English auto-generated or provided._

**0:00** · Boris journey, the creator Claude code,

**0:01** · said that he doesn't use prompt anymore.

**0:03** · He used loops to prompting Claude and

**0:05** · figure out what to do. And even Peter

**0:07** · Steinberger, the creator of open Claude,

**0:09** · has said the same thing, that we

**0:10** · shouldn't be prompting our coding agents

**0:12** · anymore. We should be designing loops

**0:14** · that prompting our AI agents. And that

**0:16** · was said on June 7th. And later on June

**0:18** · 8th, people on X claimed that this is

**0:20** · something called loop engineering. And

**0:21** · the truth is, way before they were

**0:23** · talking about this, I was the one on

**0:24** · YouTube already created a video on how

**0:26** · you can be able to apply loop

**0:28** · engineering in a practical day-to-day

**0:29** · workflow. For example, the video is

**0:31** · called how I make Claude code here

**0:33** · building apps completely autonomously.

**0:35** · And furthermore, I also have a version

**0:36** · two of that video. And if you're

**0:37** · interested, you can check out this video

**0:39** · as well. But with all being said, in

**0:40** · this video, I'm going to show exactly

**0:42** · what is loop engineering, how does it

**0:43** · work behind the scene, and why we should

**0:45** · use it. And most important part is, I'm

**0:47** · going to show exactly how I use it in my

**0:49** · personal experience on building loops.

**0:51** · And if you stick to the end of this

**0:52** · video, I'm going to show you the skills

**0:53** · that I built on how you can be designing

**0:55** · loops with the best practice. So with

**0:57** · that being said, if that sounds

**0:58** · interesting, let's get into the video.

**1:00** · Now, before we continue, I recently

**1:02** · launched our school community where I

**1:03** · help you to master AI agents,

**1:05** · automations, and so much more. And

**1:07** · that's all coming from someone who used

**1:08** · to work as a senior AI software engineer

**1:10** · at companies like Amazon and Microsoft.

**1:13** · And in this community, you're going to

**1:14** · get over 100 plus video materials like

**1:16** · templates and workflows that I

**1:18** · personally built and sold over 100 plus

**1:20** · times. On top of that, you're also going

**1:22** · to get access to our weekly live calls.

**1:24** · And just give an idea, this week, we're

**1:26** · actually running a Claude code

**1:27** · masterclass where we're going to dive

**1:28** · into how to improve Claude code's

**1:30** · accuracy. Or we're going to use it to

**1:32** · build the applications. Plus, you're

**1:33** · also going to get full community

**1:34** · supports where you're going to get a

**1:35** · chance to ask questions and get direct

**1:37** · answers back. So if you're ready to

**1:38** · level up, make sure you jump right in

**1:40** · and I'll see you in a community. Okay,

**1:42** · so first of all, what is loop

**1:43** · engineering? Well, here you can see that

**1:45** · it is a practice for designing a

**1:47** · self-correcting AI agent system that can

**1:49** · recursively iterate until a certain goal

**1:51** · is met. So what does it really mean?

**1:54** · Well, before what we have here is where

**1:55** · we have our user here just give it a

**1:57** · prompt to our AI agents and our AI agent

**1:59** · here is going to perform the task. But

**2:01** · sometimes AI agent here might not give

**2:03** · you what you want. So, what do we do? We

**2:04** · have to manually check it and re-prompt

**2:06** · it again. And that entire re-prompting

**2:08** · process is exactly what Loop Engineer

**2:10** · here is trying to solve. So, originally

**2:12** · we have our user here, give it a prompt

**2:13** · like building an app to our AI agent,

**2:16** · and instead of just have our AI agent

**2:17** · here to dispatch that and try to do the

**2:19** · work, it's going to spin up another

**2:21** · agent here, right? So, this is the

**2:22** · orchestrator and it's going to spin up

**2:24** · another agent here to do the execution.

**2:26** · And this execution here is going to

**2:27** · trigger MCP, skills that we have, and

**2:30** · also different sub-agents, and try to

**2:31** · process that work. Once the executioner

**2:34** · is done, then it's going to send the

**2:35** · results back to the orchestrator, and

**2:38** · the orchestrator here is going to check

**2:39** · the work based on the conditions or the

**2:41** · prompts that we provided initially. And

**2:43** · as a result, once we have our

**2:44** · orchestrator here process the request

**2:46** · and found that, "Okay, well, this is not

**2:47** · exactly what we want. Here's the

**2:49** · feedback." Then it's going to spin up a

**2:50** · new sub-agent here for execution, pass

**2:53** · that feedback and the initial goal, and

**2:55** · try to have the agent here to process

**2:57** · that. So, you can see that this is going

**2:58** · to be the loop that we're going to run

**2:59** · until our orchestrator here has reviewed

**3:01** · this and said, "Yes, the result." Then

**3:03** · it's going to go ahead and send it back

**3:04** · to the user. And the most important part

**3:06** · for Loop Engineer here is that it's not

**3:08** · really just limited to just two agents,

**3:10** · right? You have your orchestrator and

**3:11** · you have your executioner. You can also

**3:13** · have other agents here in the chain to

**3:14** · actually make this process here a lot

**3:16** · more better. For example, you can have

**3:17** · an orchestrator here that will dispatch

**3:19** · a execution agent here to work on a

**3:21** · task. And then you can also have another

**3:23** · agent here once the agent here has done

**3:25** · the work, for example, the builder,

**3:27** · right? Has built the application and now

**3:29** · is going to the QA process, then we have

**3:32** · our QA agent here that's specialized in

**3:34** · QA that will basically review, or in

**3:36** · this case, test the work that the

**3:38** · previous agent has done. And if this

**3:40** · work here is not approved, then it's

**3:41** · going to send it back to the agent here

**3:43** · and try to re-process that again. But if

**3:46** · it does pass, then it's going to send it

**3:47** · to the reviewer.

**3:49** · And if the reviewer reviews this, and if

**3:51** · there's any feedback, it can still send

**3:53** · it back to the QA or to the executioner

**3:56** · and try to reprocess that again. You can

**3:58** · see that this is basically the power of

**3:59** · Loop Engineer here is that you can be

**4:00** · able to adding a lot more things into

**4:02** · your Loop Chain and try to have the

**4:04** · workflow here to be executed in a

**4:05** · systematic way. Now, at this point you

**4:07** · may be wondering, okay, why do we need

**4:08** · so many agents here in the loop, right?

**4:10** · Why can't we just have one agent here

**4:12** · does a review and also does the bill?

**4:14** · Well, here's the thing. It's like if you

**4:16** · were to do this way, it's kind of like

**4:17** · the same as like having a student here

**4:19** · finishing exam, but also marking his own

**4:22** · exam as well, right? You're not going to

**4:23** · get the highest accuracy here. And

**4:25** · that's why we need to have multiple

**4:26** · agents here. One agent does the review

**4:28** · and one agent does the executions. And

**4:30** · most important part is let's say down

**4:32** · the line you want to have QA, reviewer,

**4:34** · or a UX agent, then you need to have a

**4:36** · separate agent for that, right? A

**4:38** · specialized agent with set of skills

**4:41** · that it has in its own tool belt to

**4:42** · basically trigger this process. Okay, so

**4:44** · now you know exactly how this works

**4:46** · behind the scene. Let me show you

**4:47** · exactly what are the six steps to create

**4:49** · a perfect Agentic Loops. So, the first

**4:51** · thing we need to hear is we need to know

**4:52** · exactly what the trigger is, right? How

**4:54** · do we trigger the loop? Is it a slash

**4:56** · skill? Is it on a schedule? How does it

**4:58** · actually get triggered? And then what we

**4:59** · need here is we also need to have the

**5:01** · workflow here to be triggered in a

**5:03** · separate environment. And that usually

**5:05** · be using a work tree. Because for our

**5:07** · Agentic OS that I built, you can have

**5:09** · the workflow here to be dispatched with

**5:11** · multiple agents running at the same

**5:12** · time. And each and agent here is going

**5:14** · to be running using its own work tree,

**5:16** · its own environment, so that there's no

**5:18** · code conflicts or change conflicts

**5:19** · between different agents. And then the

**5:21** · third thing we need to do here is we

**5:22** · need to know exactly what skills the

**5:24** · execution and the review here is going

**5:26** · to be triggered. And literally that's

**5:27** · going to be your agent hardness, which

**5:29** · will guide the AI on exactly how to do

**5:31** · things. And number four is going to be

**5:33** · your connectors, right? Connectors, you

**5:35** · can think of that as your like MCPs.

**5:37** · What are some tools that is actually

**5:39** · going to connect to, right? Is it

**5:40** · actually going to communicate to? Is it

**5:41** · like Slack, Jira, or is it like

**5:44** · Supabase, Stripe? What are some other

**5:46** · MCPs that it's going to interact with?

**5:48** · For me myself was the Agentic OS that I

**5:50** · built. I usually have it to connect it

**5:51** · to Century to look at the logs, and I

**5:53** · also have it to connect to GitHub so

**5:55** · they can be able to commit the changes,

**5:57** · push the issues, and everything are

**5:58** · viewable inside of a GitHub issue. For

**6:00** · example, take a look at one of the issue

**6:02** · that I have in my GitHub issue, you can

**6:03** · see that everything's are all logged in

**6:05** · here, and that's the actual another

**6:07** · thing that I'm going to talk about,

**6:07** · which is the memory. So, you can see

**6:09** · that everything from the task

**6:11** · descriptions all the way to what each

**6:13** · agent here has done. So, the first is

**6:16** · the building process, and then it moved

**6:18** · into the loop, and then here the build

**6:20** · is done. Then you can see there's like

**6:22** · 30 items in there, but if you were to

**6:24** · keep it short, you can see the build

**6:25** · process here is done. Maybe this process

**6:28** · here you can see it actually sent it

**6:29** · back in between like maybe the review

**6:31** · take a look at it or the QA runs the

**6:33** · test and it didn't pass, it's going to

**6:34** · send it back to the builder here to

**6:36** · rebuild it. But eventually you can see

**6:38** · that the build here is fully complete,

**6:40** · QA now is passing, and then the reviewer

**6:42** · here is fully approved based on the

**6:44** · description of the task, and also the

**6:46** · changes that the builder has complete

**6:48** · and the QA has passed. Then it's going

**6:51** · to review and the review now is

**6:52** · approved, so then it's going to merge

**6:54** · that pull request. And eventually here

**6:56** · you can see the ticket here is finally

**6:58** · closed, and we can do it now mark that

**7:00** · ticket as done. Okay? So, you can see

**7:02** · that each every issue here is basically

**7:04** · using a MCP here GitHub to keep track of

**7:07** · all the issue status. And that's

**7:09** · literally the next thing we have here is

**7:10** · memory, which is basically having the

**7:12** · Nest agent here having context of what

**7:14** · has happened so far, right? Maybe this

**7:17** · has gone over for like 10 iterations

**7:19** · already where we have a reviewer, agent

**7:21** · here has done the executions back and

**7:23** · forth. Each iteration here we spin up a

**7:25** · new sub agent, right? So, it has a fresh

**7:26** · context window, and it needs to know

**7:28** · exactly what has happened in the past.

**7:30** · What have we tried so far, right? So, we

**7:32** · need to record that in the memory to log

**7:34** · that so that the agent here when it

**7:36** · start work on it, it look through the

**7:38** · past log to see what has been tried and

**7:41** · what's not working. And here is what we

**7:43** · need what we need to try, right? So,

**7:45** · this is exactly what we need here is a

**7:46** · memory. And the last thing we need to do

**7:48** · here is we need to have a sub agents.

**7:50** · Now, sub agent part, like I said, you

**7:52** · need to have multiple agent here to do

**7:53** · different things. And by having sub

**7:55** · agent, you can have multiple agent here

**7:57** · running in parallel along with each

**7:59** · agent here has his own work tree to

**8:01** · process this simultaneously. So, now you

**8:03** · know exactly what are the things we need

**8:04** · to building our perfect agentic loops,

**8:07** · let me show you the skills that are

**8:08** · created for you so that you can use it

**8:10** · your perfect agentic loop following the

**8:12** · best practice that we just mentioned.

**8:14** · Now, before I show you the skill, here

**8:15** · you can see this is the entire loop

**8:16** · layout on exactly what the skill help

**8:18** · you to generate. So, you can see that it

**8:20** · focuses on these seven things, right?

**8:22** · These six or seven things, like what I

**8:23** · just mentioned to you. And just to

**8:25** · quickly recap, we need to know exactly

**8:26** · what triggers the workflow, right? Is it

**8:28** · like a on-demand trigger or a schedule

**8:31** · or listening for like a third-party API

**8:33** · request? And in this case, do we need a

**8:36** · work tree? In this case, created a

**8:37** · separate branch for this. And also, what

**8:39** · is the agent harness skill, right? What

**8:41** · skill does the agent here is going to

**8:43** · follow and try to process the execution?

**8:45** · And each iteration here is going to

**8:47** · reload that skill and try to process

**8:49** · that. And then furthermore, we also have

**8:51** · our validator here, which will basically

**8:52** · validate work that the generator has

**8:54** · done. And then furthermore, you can see

**8:56** · we also have our connector here, which

**8:57** · will basically connect it to our

**8:58** · third-party MCPs or CLI tools. And then

**9:01** · lastly, we also have our states, which

**9:03** · will basically connect And lastly, we

**9:05** · also have our states, which will keep

**9:06** · track of each iteration summary. And

**9:08** · most important part is that if there's

**9:09** · any parts that are stuck, right? If the

**9:11** · generator here is unable to process,

**9:13** · then it's going to delegate that into

**9:14** · the human review, where we're going to

**9:16** · mark that issue here to be stuck. And

**9:18** · for the memory here, you can see, like I

**9:19** · said, I connected to using GitHub issues

**9:21** · because it's so much easier. You can be

**9:23** · able to link your pull requests,

**9:24** · repositories into GitHub issues, and you

**9:27** · can be able to have your ticket

**9:28** · descriptions, and also you can be able

**9:30** · to have all the logs, right? Keeping

**9:32** · track inside of the same issue. So, what

**9:34** · I usually do here for the state is I'll

**9:35** · just connect it to GitHub issues. Each

**9:37** · task is going to be one issue. Every

**9:39** · iteration here is just going to be

**9:41** · adding the log, right? These events here

**9:43** · you can see is going to be inside of

**9:45** · this same issue. So, everything's all

**9:46** · organized and compacted into a single

**9:49** · issue that you can see here, which is

**9:51** · easier for me to manage. And let's say

**9:53** · down the road, let's say if I want to

**9:54** · create a new loop, I'm simply just going

**9:55** · to creating a GitHub issue first,

**9:57** · creating the GitHub description on what

**9:59** · the task does, and what is the

**10:01** · acceptance criteria, and simply just

**10:03** · going to copy that link, paste that to

**10:05** · the loop, and start to iterate. And

**10:06** · finally, I have packaged everything that

**10:08** · I talked about in this video into the

**10:09** · skill called Loop Maker, which is a

**10:11** · portable agent skill that works in your

**10:13** · all your AI agents, and interview you to

**10:15** · scaffold a self-running agentic loop

**10:18** · that have a complete verifier, state

**10:20** · file, and also human gates. And it's

**10:22** · doing that by validating the loop it

**10:24** · creates, making sure that your loop here

**10:26** · following the seven best practice that

**10:27** · we talked about in this video. And

**10:29** · furthermore, this skill here also has a

**10:31** · very nice user interface, so you know

**10:33** · exactly which stage you are whenever

**10:35** · you're triggered a skill.

**10:37** · And then here you can see this is the

**10:37** · entire flow. It first asks you seven

**10:40** · questions that we mentioned, survey to

**10:42** · see if there's any gaps, confirm the

**10:43** · loop shape, and try to scaffold the

**10:45** · entire loop to make it ready to invoke.

**10:47** · So, pretty much that's the skill, and if

**10:49** · you want to give it a try, make sure to

**10:50** · check out in the link in the description

**10:51** · below, or you can join our school

**10:52** · community where you can go to check it

**10:54** · out inside of our video material

**10:55** · section. And of course, on this Friday

**10:56** · we actually have a live call, so if you

**10:58** · have any questions about agentic loops,

**10:59** · or anything that you're currently

**11:00** · building, make sure to prepare your

**11:02** · questions, join the call, and I will

**11:04** · make sure to see you there. Okay? So,

**11:05** · pretty much that's it for this video. If

**11:07** · you do find value in this video, please

**11:08** · make sure to like this video, consider

**11:10** · to subscribe, check out our school

**11:11** · community if you want more content like

**11:12** · this. With that being said, I'll see you

**11:14** · in the next video.
