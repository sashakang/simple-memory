---
title: "The 4 Levels of Loop Engineering Clearly Explained"
source: "https://www.youtube.com/watch?v=5WB5bcGNib8"
author:
  - "[[The AI Automators]]"
published: 2026-07-13
created: 2026-07-14
description: "Loop-engineering explainer centered on checkers, /goal blind spots, computational vs inferential feedback, worktrees, caps, cost, and human oversight."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=5WB5bcGNib8)

Access our AI Architects course & community: https://www.theaiautomators.com/?utm_source=youtube&utm_medium=video&utm_campaign=tutorial&utm_content=loop-engineering

Loop engineering explainer focused on Claude Code's four levels of loops, /goal, feedback taxonomies, worktrees, loop caps, cost control, and human review.

Timestamps:
00:00 Loop engineering
01:03 Every coding agent is already a loop
01:54 The 4 levels of loops
04:20 Is any of this actually new?
06:01 How /goal works (and its blind spot)
08:25 Better feedback: computational vs inferential
11:14 Worktrees, caps & the cost of loops
12:49 Delete your scaffolding as agents improve
13:22 Human in the loop
13:50 The verdict: it's the checker

## Transcript

**0:00** · There's been a lot of talk online about the topic of loop engineering and to

**0:03** · the topic of loop engineering and to confuse matters, everyone seems to have

**0:05** · confuse matters, everyone seems to have their own definition of exactly what it

**0:07** · their own definition of exactly what it is. This all started a few weeks ago

**0:09** · is. This all started a few weeks ago when the creator of open claw posted on

**0:11** · when the creator of open claw posted on X, here's your monthly reminder that you

**0:13** · X, here's your monthly reminder that you shouldn't be prompting coding agents

**0:15** · shouldn't be prompting coding agents anymore. You should be designing loops

**0:17** · anymore. You should be designing loops that prompt your agents. Then Boris

**0:19** · that prompt your agents. Then Boris Cherny, the creator of Claude code,

**0:21** · Cherny, the creator of Claude code, said, I don't prompt Claude anymore. I

**0:23** · said, I don't prompt Claude anymore. I have loops running that prompt Claude.

**0:25** · have loops running that prompt Claude. My job is to write loops. So what does

**0:28** · My job is to write loops. So what does this all mean and how much of it is just

**0:30** · this all mean and how much of it is just hype? Because on one side of the

**0:31** · hype? Because on one side of the spectrum you have people claiming that

**0:32** · spectrum you have people claiming that this is a game changer and it's changing

**0:34** · this is a game changer and it's changing how they work and on the other side,

**0:36** · how they work and on the other side, plenty of developers are rolling their

**0:38** · plenty of developers are rolling their eyes saying that these are just wild

**0:40** · eyes saying that these are just wild loops and crown jobs and that loop

**0:42** · loops and crown jobs and that loop engineering is just another push towards

**0:44** · engineering is just another push towards token maxing and trying to make AI

**0:46** · token maxing and trying to make AI companies as much money as possible. So

**0:48** · companies as much money as possible. So let's get into it and see which one is

**0:49** · let's get into it and see which one is right. Anthropic recently published a

**0:52** · right. Anthropic recently published a good post on this where the Claude code

**0:54** · good post on this where the Claude code team defines loops as agents repeating

**0:56** · team defines loops as agents repeating cycles of work until a stop condition is

**0:59** · cycles of work until a stop condition is met and this stop condition is something

**1:01** · met and this stop condition is something we're going to keep coming back to.

**1:02** · we're going to keep coming back to. First off, when you prompt a coding

**1:04** · First off, when you prompt a coding agent, you might think of it as one

**1:06** · agent, you might think of it as one instruction in, one result or one answer

**1:08** · instruction in, one result or one answer out, but that's not what's actually

**1:10** · out, but that's not what's actually happening under the hood. The agent is

**1:12** · happening under the hood. The agent is already running multiple loops by

**1:14** · already running multiple loops by itself. It reads the context, calls

**1:16** · itself. It reads the context, calls tools such as editing a file, runs a

**1:18** · tools such as editing a file, runs a test, it reads the result of that and

**1:20** · test, it reads the result of that and then it loops around again and again and

**1:22** · then it loops around again and again and it keeps going around in that cycle

**1:24** · it keeps going around in that cycle until it decides on its own that the

**1:26** · until it decides on its own that the task is done and it stops. Each agent

**1:29** · task is done and it stops. Each agent has its own internal loop and coding

**1:31** · has its own internal loop and coding harnesses can layer additional loops on

**1:32** · harnesses can layer additional loops on top of that. So for our purposes, what

**1:34** · top of that. So for our purposes, what exactly is loop engineering? Well, it's

**1:36** · exactly is loop engineering? Well, it's effectively the outer loop. It's any

**1:39** · effectively the outer loop. It's any additional loop or loops wrapped around

**1:41** · additional loop or loops wrapped around the outside of the whole process. One

**1:43** · the outside of the whole process. One that decides when the job is finished or

**1:45** · that decides when the job is finished or sets it going again. And the lines here

**1:47** · sets it going again. And the lines here can get quite blurred as the creator of

**1:49** · can get quite blurred as the creator of the coding agents include more looping

**1:51** · the coding agents include more looping features directly out of the box and

**1:53** · features directly out of the box and we'll talk about that later. The Claude

**1:54** · we'll talk about that later. The Claude team has laid out loop engineering in

**1:56** · team has laid out loop engineering in four different levels. First off, we

**1:58** · four different levels. First off, we have turn-based loops, and this is using

**2:00** · have turn-based loops, and this is using those built-in features of practically

**2:02** · those built-in features of practically any coding agent. You have your prompt,

**2:04** · any coding agent. You have your prompt, the agent runs its inner loops, and it

**2:06** · the agent runs its inner loops, and it judges for itself when it's finished. At

**2:08** · judges for itself when it's finished. At this level, you've handed off the check,

**2:09** · this level, you've handed off the check, the is it done decision. You've got your

**2:11** · the is it done decision. You've got your prompt, it gathers context, takes

**2:13** · prompt, it gathers context, takes action, verifies the work, keeps going

**2:15** · action, verifies the work, keeps going around in that loop as necessary, and

**2:17** · around in that loop as necessary, and then returns with a response. The stop

**2:19** · then returns with a response. The stop criteria here is where the main Claude

**2:21** · criteria here is where the main Claude agent judges it has completed the task

**2:23** · agent judges it has completed the task or needs additional context. Level two

**2:25** · or needs additional context. Level two is goal-based, and this is where things

**2:27** · is goal-based, and this is where things get interesting. The goal command in

**2:29** · get interesting. The goal command in Claude code is a pretty simple

**2:31** · Claude code is a pretty simple implementation of a goal-based loop.

**2:34** · implementation of a goal-based loop. Here, you type {forward slash} goal,

**2:35** · Here, you type {forward slash} goal, give it some success criteria, and then

**2:37** · give it some success criteria, and then a separate evaluator model for each

**2:40** · a separate evaluator model for each check that criteria has been met on

**2:41** · check that criteria has been met on every turn of the main agent, and then

**2:43** · every turn of the main agent, and then sends it back until it's actually been

**2:45** · sends it back until it's actually been met. At the end of the process, ideally

**2:47** · met. At the end of the process, ideally the goal has been met or the max turn

**2:49** · the goal has been met or the max turn limit has been reached. There are many

**2:51** · limit has been reached. There are many different implementations of this type

**2:53** · different implementations of this type of goal-based loop, and the goal feature

**2:55** · of goal-based loop, and the goal feature in Claude code is essentially a type of

**2:57** · in Claude code is essentially a type of Ralph Wiggum loop, although with not as

**2:59** · Ralph Wiggum loop, although with not as much control and not as efficient as one

**3:02** · much control and not as efficient as one that clears the context every time. So,

**3:04** · that clears the context every time. So, the goal feature in Claude code is very

**3:05** · the goal feature in Claude code is very useful and easy to use, but it does have

**3:08** · useful and easy to use, but it does have certain limitations. Level three is

**3:10** · certain limitations. Level three is time-based, such as using {forward

**3:12** · time-based, such as using {forward slash} loop or {forward slash} schedule

**3:14** · slash} loop or {forward slash} schedule within Claude code. Now, the agent will

**3:16** · within Claude code. Now, the agent will be prompted at a specific time. {Forward

**3:18** · be prompted at a specific time. {Forward slash} loop runs on your own computer,

**3:20** · slash} loop runs on your own computer, or you can move to the cloud by creating

**3:22** · or you can move to the cloud by creating a routine with {forward slash} schedule.

**3:24** · a routine with {forward slash} schedule. A simple example, {forward slash} loop 5

**3:27** · A simple example, {forward slash} loop 5 minutes, check my PR address review

**3:28** · minutes, check my PR address review comments, and fix failing CI. You might

**3:31** · comments, and fix failing CI. You might be looking at this saying, "Wait,

**3:32** · be looking at this saying, "Wait, schedule loops are basically just cron

**3:34** · schedule loops are basically just cron jobs." And yes, you will be very much

**3:36** · jobs." And yes, you will be very much correct. And finally, level four is

**3:38** · correct. And finally, level four is proactive loops, which stitches the

**3:40** · proactive loops, which stitches the others together. A schedule might fire

**3:42** · others together. A schedule might fire it or an event fire a webhook, a goal to

**3:44** · it or an event fire a webhook, a goal to stop it, a workflow to do the work. And

**3:47** · stop it, a workflow to do the work. And these could potentially run categories

**3:48** · these could potentially run categories of jobs on their own, triaging bugs,

**3:50** · of jobs on their own, triaging bugs, running migrations, etc. And within

**3:52** · running migrations, etc. And within Claude's example here, they have a

**3:53** · Claude's example here, they have a schedule, they have a goal, they have

**3:55** · schedule, they have a goal, they have their very powerful dynamic workflows,

**3:57** · their very powerful dynamic workflows, and they suggest using auto mode so that

**4:00** · and they suggest using auto mode so that the routine runs without stopping to ask

**4:01** · the routine runs without stopping to ask for permission. And because we're using

**4:03** · for permission. And because we're using built-in features of Claude here, you

**4:05** · built-in features of Claude here, you don't need to build any elaborate

**4:07** · don't need to build any elaborate external harnesses. You have /schedule,

**4:10** · external harnesses. You have /schedule, /goal, and then ask it to use a workflow

**4:13** · /goal, and then ask it to use a workflow to explore solutions in parallel work

**4:15** · to explore solutions in parallel work trees. So, there really is a lot going

**4:17** · trees. So, there really is a lot going on here, all using the built-in features

**4:19** · on here, all using the built-in features of Claude code. So, is loop engineering

**4:21** · of Claude code. So, is loop engineering really a new concept? Well, the most

**4:23** · really a new concept? Well, the most cynical take on this is that loops have

**4:25** · cynical take on this is that loops have been a key part of computer programs for

**4:26** · been a key part of computer programs for nearly 80 years. In fact, the world's

**4:28** · nearly 80 years. In fact, the world's very first computer programmer published

**4:30** · very first computer programmer published an algorithm which included the concept

**4:32** · an algorithm which included the concept of loops in 1843. So, she was pretty far

**4:35** · of loops in 1843. So, she was pretty far ahead of these guys. So, a more specific

**4:37** · ahead of these guys. So, a more specific question, are agentic loops a new

**4:39** · question, are agentic loops a new concept? Well, it depends on how you

**4:41** · concept? Well, it depends on how you define it. The idea of a react loop, as

**4:43** · define it. The idea of a react loop, as we know it within AI architectures, was

**4:46** · we know it within AI architectures, was published in 2022. This is the

**4:48** · published in 2022. This is the thought-action-observation

**4:50** · thought-action-observation loop that is now the standard design

**4:52** · loop that is now the standard design pattern for AI agents. But really, when

**4:54** · pattern for AI agents. But really, when people are talking about loop

**4:55** · people are talking about loop engineering now, it's much more of a

**4:57** · engineering now, it's much more of a broad umbrella term about repeating

**4:59** · broad umbrella term about repeating cycles of work for your agents. It's a

**5:01** · cycles of work for your agents. It's a bit of a mindset shift to make agents

**5:03** · bit of a mindset shift to make agents work more autonomously on a schedule or

**5:06** · work more autonomously on a schedule or towards a goal. And for the most part,

**5:08** · towards a goal. And for the most part, yes, it's basically just loops and cron

**5:11** · yes, it's basically just loops and cron jobs. But when you dig into it, there

**5:13** · jobs. But when you dig into it, there are a lot of considerations, and there's

**5:14** · are a lot of considerations, and there's a big difference between a well-designed

**5:16** · a big difference between a well-designed loop for your agent and a badly designed

**5:19** · loop for your agent and a badly designed one. So, while I've been eye-rolling a

**5:20** · one. So, while I've been eye-rolling a little bit about the loop engineering

**5:22** · little bit about the loop engineering topic as a whole, I think it is an

**5:24** · topic as a whole, I think it is an interesting one once you look at it

**5:25** · interesting one once you look at it through the right lens. There's huge

**5:27** · through the right lens. There's huge demand for AI to run autonomously and

**5:29** · demand for AI to run autonomously and produce real results without us having

**5:31** · produce real results without us having to continuously prompt them. And the one

**5:33** · to continuously prompt them. And the one interesting question is, how do you

**5:35** · interesting question is, how do you design an effective loop for your coding

**5:37** · design an effective loop for your coding agent? Pretty much everything is riding

**5:39** · agent? Pretty much everything is riding on this level two moment here, the

**5:40** · on this level two moment here, the moment a machine decides when the work

**5:42** · moment a machine decides when the work is finished. Because remember, the

**5:44** · is finished. Because remember, the Claude code team defined loops as agents

**5:46** · Claude code team defined loops as agents repeating cycles of work until a stop

**5:48** · repeating cycles of work until a stop condition is met. So, it all stands or

**5:51** · condition is met. So, it all stands or falls on the question of how effective

**5:53** · falls on the question of how effective our system is at really knowing when

**5:55** · our system is at really knowing when work has been completed, knowing when

**5:57** · work has been completed, knowing when that stop condition has been met. And

**5:59** · that stop condition has been met. And that's where the real engineering kicks

**6:00** · that's where the real engineering kicks in. Let's start off simply by examining

**6:03** · in. Let's start off simply by examining how these goal-based loops actually

**6:05** · how these goal-based loops actually work. In this simple example, {forward

**6:07** · work. In this simple example, {forward slash} goal, get the home page

**6:09** · slash} goal, get the home page lighthouse score to 90 or above, stop

**6:12** · lighthouse score to 90 or above, stop after five tries. So, let's say that

**6:13** · after five tries. So, let's say that you're running a website and you want to

**6:15** · you're running a website and you want to optimize its speed, Cloud Code will

**6:17** · optimize its speed, Cloud Code will continually update the code on the page,

**6:19** · continually update the code on the page, and then retest the score until it

**6:21** · and then retest the score until it reaches the desired result. So, here we

**6:23** · reaches the desired result. So, here we have the main agent doing the actual

**6:24** · have the main agent doing the actual work, and then sitting just behind it,

**6:27** · work, and then sitting just behind it, there's a second, much smaller model.

**6:29** · there's a second, much smaller model. Under the hood, that's really all

**6:31** · Under the hood, that's really all {forward slash} goal actually is within

**6:32** · {forward slash} goal actually is within Cloud Code. A little hook that fires

**6:35** · Cloud Code. A little hook that fires every time the agent tries to stop, and

**6:37** · every time the agent tries to stop, and then runs your success condition past

**6:39** · then runs your success condition past that small model. Its one job is to

**6:41** · that small model. Its one job is to decide over and over whether you've

**6:43** · decide over and over whether you've actually hit the goal yet. So, this

**6:45** · actually hit the goal yet. So, this evaluator model will decide whether it

**6:47** · evaluator model will decide whether it needs to provide feedback to the main

**6:48** · needs to provide feedback to the main agent that will keep going around in a

**6:50** · agent that will keep going around in a loop as necessary, and then eventually

**6:53** · loop as necessary, and then eventually it stops. So, that little gatekeeper is

**6:55** · it stops. So, that little gatekeeper is deliberately tiny, a small, fast model

**6:57** · deliberately tiny, a small, fast model running after every single turn. And it

**6:59** · running after every single turn. And it actually can't go and do anything

**7:01** · actually can't go and do anything itself. It can't run your tests, it

**7:03** · itself. It can't run your tests, it can't open your files, and it can't

**7:05** · can't open your files, and it can't reload the page to check the real score.

**7:07** · reload the page to check the real score. It can only actually read the

**7:08** · It can only actually read the transcript, the conversation history.

**7:11** · transcript, the conversation history. But, if the main agent actually runs

**7:12** · But, if the main agent actually runs tests, the results still land there in

**7:14** · tests, the results still land there in the transcript, so the evaluator can

**7:16** · the transcript, so the evaluator can still read and examine those. But, this

**7:18** · still read and examine those. But, this evaluator model can only ever trust

**7:21** · evaluator model can only ever trust what's in the transcript. It can't check

**7:23** · what's in the transcript. It can't check whether it's still true. What if the

**7:24** · whether it's still true. What if the agent never actually ran the tests and

**7:26** · agent never actually ran the tests and just said it did? What if it ran a

**7:27** · just said it did? What if it ran a handful, not all of them? Or if it just

**7:29** · handful, not all of them? Or if it just ran five turns ago and then broke the

**7:31** · ran five turns ago and then broke the build? So, regardless of those

**7:33** · build? So, regardless of those limitations, it's very, very useful to

**7:35** · limitations, it's very, very useful to have a separate agent grading the work

**7:37** · have a separate agent grading the work in some shape or form, because the main

**7:39** · in some shape or form, because the main agent is likely to just declare success

**7:41** · agent is likely to just declare success early if you just leave it up to that

**7:43** · early if you just leave it up to that agent. If you're working on casual or

**7:45** · agent. If you're working on casual or relatively simple or contained projects,

**7:48** · relatively simple or contained projects, and particularly if you're a solo

**7:49** · and particularly if you're a solo developer, these features might be

**7:51** · developer, these features might be enough for your use case, especially

**7:53** · enough for your use case, especially because what you get out of the box with

**7:55** · because what you get out of the box with coding agents like Cloud Code and Codex

**7:57** · coding agents like Cloud Code and Codex can be incredibly effective. So, you

**7:59** · can be incredibly effective. So, you don't necessarily need to go engineering

**8:02** · don't necessarily need to go engineering more convoluted external loops in order

**8:04** · more convoluted external loops in order to get the job done. But, software

**8:06** · to get the job done. But, software projects will often require much more

**8:08** · projects will often require much more effective feedback loops than you get

**8:10** · effective feedback loops than you get out of the box with these coding agents.

**8:12** · out of the box with these coding agents. And they're often very project dependent

**8:15** · And they're often very project dependent and use case specific. And this can get

**8:17** · and use case specific. And this can get quite important in enterprise or for

**8:19** · quite important in enterprise or for projects that are already deployed with

**8:20** · projects that are already deployed with large code bases or projects where

**8:22** · large code bases or projects where multiple developers are working

**8:24** · multiple developers are working together. So, a loop is only ever as

**8:26** · together. So, a loop is only ever as good as the thing that decides when it's

**8:28** · good as the thing that decides when it's done. But, for coding agents, there are

**8:30** · done. But, for coding agents, there are many different types of feedback that we

**8:32** · many different types of feedback that we can feed into the loop. And you can

**8:34** · can feed into the loop. And you can build additional feedback into the

**8:35** · build additional feedback into the process, such as using hooks within your

**8:38** · process, such as using hooks within your coding agent to keep things on track. In

**8:40** · coding agent to keep things on track. In a previous video, I covered this article

**8:41** · a previous video, I covered this article on Harness Engineering for coding users.

**8:44** · on Harness Engineering for coding users. And in it, it distinguishes between the

**8:46** · And in it, it distinguishes between the inner harness, which is the coding agent

**8:48** · inner harness, which is the coding agent features you get out of the box, as well

**8:50** · features you get out of the box, as well as your outer harness, the user harness.

**8:53** · as your outer harness, the user harness. And these are feedforward and feedback

**8:55** · And these are feedforward and feedback controls that you can put in place as a

**8:57** · controls that you can put in place as a user of the coding agent. And the author

**8:59** · user of the coding agent. And the author of that article defined two broad types

**9:01** · of that article defined two broad types of feedback mechanisms that we can pass

**9:03** · of feedback mechanisms that we can pass back into the main agent and therefore

**9:06** · back into the main agent and therefore improve the quality of the development

**9:07** · improve the quality of the development feedback loop. That is computational

**9:09** · feedback loop. That is computational checks and inferential checks.

**9:12** · checks and inferential checks. Computational checks are deterministic

**9:14** · Computational checks are deterministic and fast. They're run by the CPU. So, we

**9:16** · and fast. They're run by the CPU. So, we have things like test suites, linters,

**9:19** · have things like test suites, linters, type checkers, and structural analysis.

**9:21** · type checkers, and structural analysis. These are run in milliseconds to

**9:22** · These are run in milliseconds to seconds. Results are highly reliable.

**9:25** · seconds. Results are highly reliable. And importantly, when you have these

**9:26** · And importantly, when you have these checks up and running, they can be run

**9:28** · checks up and running, they can be run automatically using hooks. So, you're

**9:30** · automatically using hooks. So, you're not relying on your coding agents to

**9:32** · not relying on your coding agents to just run the tests through prompting. A

**9:34** · just run the tests through prompting. A hook is a shell command that runs at a

**9:36** · hook is a shell command that runs at a specific stage, and your coding agent

**9:38** · specific stage, and your coding agent can use these such as a stop command

**9:41** · can use these such as a stop command when Cloud Code thinks it's finished.

**9:43** · when Cloud Code thinks it's finished. And these checks can run continuously as

**9:45** · And these checks can run continuously as the agent is working. So, these are

**9:46** · the agent is working. So, these are cheap, fast, reliable computational

**9:49** · cheap, fast, reliable computational checks that you can run throughout the

**9:51** · checks that you can run throughout the process without having to spend any

**9:52** · process without having to spend any money on AI tokens. For serious

**9:55** · money on AI tokens. For serious projects, especially in enterprise and

**9:57** · projects, especially in enterprise and ones with lots of developers involved,

**9:59** · ones with lots of developers involved, computational checks are incredibly

**10:01** · computational checks are incredibly useful and are very underused across the

**10:03** · useful and are very underused across the board amongst the users of AI coding

**10:06** · board amongst the users of AI coding agents. And then we have inferential

**10:08** · agents. And then we have inferential checks, semantic analysis, AI code

**10:10** · checks, semantic analysis, AI code review, LLM as a judge, and this can

**10:12** · review, LLM as a judge, and this can perform all the additional checks that

**10:14** · perform all the additional checks that can't be done computationally. These

**10:16** · can't be done computationally. These checks are far more expensive and slower

**10:18** · checks are far more expensive and slower as they use AI tokens. You can fit these

**10:20** · as they use AI tokens. You can fit these into the life cycle where it suits and

**10:22** · into the life cycle where it suits and you could have multiple different types

**10:23** · you could have multiple different types of AI checks before the AI model commits

**10:25** · of AI checks before the AI model commits code. You could have lightweight review

**10:27** · code. You could have lightweight review sub-agents before merging, you could

**10:29** · sub-agents before merging, you could trigger a heavier review process where

**10:31** · trigger a heavier review process where you can fan out many sub-agents to look

**10:33** · you can fan out many sub-agents to look at the whole change in context, and then

**10:35** · at the whole change in context, and then even later in the process, you could

**10:37** · even later in the process, you could have an LLM judge running in the loop on

**10:39** · have an LLM judge running in the loop on a schedule against your live system to

**10:42** · a schedule against your live system to ensure things are running correctly. So,

**10:43** · ensure things are running correctly. So, this can get pretty deep, but in

**10:45** · this can get pretty deep, but in reality, the richer the feedback, the

**10:47** · reality, the richer the feedback, the more effective your agentic loops will

**10:49** · more effective your agentic loops will actually be. And the potential richness

**10:51** · actually be. And the potential richness of feedback we can give our coding

**10:53** · of feedback we can give our coding agents is one of the main reasons why AI

**10:55** · agents is one of the main reasons why AI agents are so effective at writing code,

**10:58** · agents are so effective at writing code, but how they can often fail in so many

**11:00** · but how they can often fail in so many other spaces where it's a lot more

**11:02** · other spaces where it's a lot more difficult to judge and validate the

**11:03** · difficult to judge and validate the work. So, very importantly, autonomous

**11:06** · work. So, very importantly, autonomous loops will only really work when the AI

**11:08** · loops will only really work when the AI model can get real feedback to

**11:10** · model can get real feedback to self-correct. Otherwise, things can go

**11:12** · self-correct. Otherwise, things can go really off track. When you start running

**11:15** · really off track. When you start running parallel agents against your code base,

**11:17** · parallel agents against your code base, you really need to keep them apart.

**11:19** · you really need to keep them apart. Cloud Code does this using Git work

**11:21** · Cloud Code does this using Git work trees. Every parallel agent gets its own

**11:23** · trees. Every parallel agent gets its own copy of the code. So, 10 of them editing

**11:26** · copy of the code. So, 10 of them editing at once never tread on each other. They

**11:28** · at once never tread on each other. They are a great option, but keep in mind

**11:29** · are a great option, but keep in mind that work trees can really

**11:31** · that work trees can really overcomplicate matters. It's also very

**11:33** · overcomplicate matters. It's also very important to make sure that your loops

**11:34** · important to make sure that your loops do not just run forever. So, you

**11:36** · do not just run forever. So, you generally should have a max iterations

**11:38** · generally should have a max iterations count to just stop it at a certain

**11:40** · count to just stop it at a certain point. With Claude Code's goal command,

**11:43** · point. With Claude Code's goal command, you have a soft cap. You can just ask it

**11:45** · you have a soft cap. You can just ask it to stop after five tries, but it's not

**11:47** · to stop after five tries, but it's not necessarily guaranteed. It generally

**11:49** · necessarily guaranteed. It generally works well, but it's not quite as

**11:50** · works well, but it's not quite as deterministic as a loop script, such as

**11:53** · deterministic as a loop script, such as a Ralph Wiggum script, which is just a

**11:55** · a Ralph Wiggum script, which is just a simple loop in code, which would

**11:56** · simple loop in code, which would deterministically stop after a certain

**11:58** · deterministically stop after a certain number of attempts. And your token bill

**12:01** · number of attempts. And your token bill is definitely worth thinking about here,

**12:02** · is definitely worth thinking about here, because the cost is the part that often

**12:04** · because the cost is the part that often is getting glossed over at the moment.

**12:06** · is getting glossed over at the moment. Agentic loops can be incredibly

**12:08** · Agentic loops can be incredibly expensive, and you really do need to

**12:09** · expensive, and you really do need to keep your usage in check. Any kind of

**12:12** · keep your usage in check. Any kind of workflow that's spinning up large

**12:13** · workflow that's spinning up large amounts of sub-agents can work through a

**12:15** · amounts of sub-agents can work through a huge amount of tokens quickly. We're

**12:17** · huge amount of tokens quickly. We're talking potentially millions of tokens.

**12:19** · talking potentially millions of tokens. Anyone who's run Claude Code's great

**12:21** · Anyone who's run Claude Code's great dynamic workflows feature would probably

**12:23** · dynamic workflows feature would probably know what I mean. It's not unusual for

**12:25** · know what I mean. It's not unusual for it to churn through millions of tokens

**12:27** · it to churn through millions of tokens just to reach a single end goal. A key

**12:29** · just to reach a single end goal. A key thing to keep in mind that concepts like

**12:32** · thing to keep in mind that concepts like loop engineering and token maxing are

**12:34** · loop engineering and token maxing are usually pushed by those that have a

**12:36** · usually pushed by those that have a pretty big incentive to do so, because

**12:38** · pretty big incentive to do so, because they're the ones profiting from it. The

**12:40** · they're the ones profiting from it. The more tokens you burn, the better it

**12:41** · more tokens you burn, the better it tends to be for them. So, I'd definitely

**12:43** · tends to be for them. So, I'd definitely take some of the louder claims with a

**12:45** · take some of the louder claims with a pinch of salt, and keep a close eye on

**12:47** · pinch of salt, and keep a close eye on what these loops are actually costing

**12:49** · what these loops are actually costing you. When you're building agentic loops,

**12:50** · you. When you're building agentic loops, you're often building additional

**12:52** · you're often building additional scaffolding around your main coding

**12:54** · scaffolding around your main coding agent, but as the coding agents get

**12:56** · agent, but as the coding agents get better, you need to delete unnecessary

**12:59** · better, you need to delete unnecessary and redundant parts of those scaffolds.

**13:01** · and redundant parts of those scaffolds. So, perhaps you've been using a specific

**13:03** · So, perhaps you've been using a specific outer coding harness for the last few

**13:04** · outer coding harness for the last few months, whereas now the out-of-the-box

**13:07** · months, whereas now the out-of-the-box functionality within the coding agents

**13:09** · functionality within the coding agents might just be good enough for your

**13:10** · might just be good enough for your particular tasks, and that older

**13:12** · particular tasks, and that older scaffolding might become dead weight.

**13:14** · scaffolding might become dead weight. This applies to outer harnesses that

**13:16** · This applies to outer harnesses that might be running loops, but it also

**13:18** · might be running loops, but it also applies to maybe older meta-prompting

**13:19** · applies to maybe older meta-prompting frameworks that are no longer required.

**13:22** · frameworks that are no longer required. There's a lot of sentiment online that

**13:23** · There's a lot of sentiment online that we should just be leaving autonomous

**13:25** · we should just be leaving autonomous loops run wild. In reality, human in the

**13:28** · loops run wild. In reality, human in the loop is absolutely vital at correct

**13:29** · loop is absolutely vital at correct stages of the process to make sure we're

**13:31** · stages of the process to make sure we're steering them in the correct direction.

**13:33** · steering them in the correct direction. So, back to this article again, even

**13:35** · So, back to this article again, even though there's potentially quite a lot

**13:37** · though there's potentially quite a lot going on in terms of guides and sensors

**13:39** · going on in terms of guides and sensors and feedback mechanisms, there's a human

**13:41** · and feedback mechanisms, there's a human steering the overall process, steering

**13:44** · steering the overall process, steering the feedback elements of the harness,

**13:46** · the feedback elements of the harness, and also reviewing and signing off on

**13:48** · and also reviewing and signing off on the results as necessary. So, where do

**13:50** · the results as necessary. So, where do we land on the concept of loop

**13:51** · we land on the concept of loop engineering? Overall, I think this has

**13:53** · engineering? Overall, I think this has been quite overblown. Loops are not new.

**13:56** · been quite overblown. Loops are not new. The react pattern for AI agents is also

**13:58** · The react pattern for AI agents is also not new. A lot of what's been sold as

**14:01** · not new. A lot of what's been sold as loop engineering is very much just while

**14:03** · loop engineering is very much just while loops and cron jobs. So, if you've been

**14:05** · loops and cron jobs. So, if you've been rolling your eyes at the hype, I do

**14:07** · rolling your eyes at the hype, I do certainly understand that. I think there

**14:09** · certainly understand that. I think there are some useful things to think about

**14:10** · are some useful things to think about once you really dig into what matters in

**14:12** · once you really dig into what matters in this whole process, which is the

**14:14** · this whole process, which is the checker. Then really the most important

**14:16** · checker. Then really the most important element is understanding stop condition,

**14:19** · element is understanding stop condition, understanding the checker, the

**14:20** · understanding the checker, the evaluator, and making sure that you

**14:22** · evaluator, and making sure that you provide all of the right feedback as

**14:24** · provide all of the right feedback as necessary to that evaluator, so it

**14:26** · necessary to that evaluator, so it actually knows when the work has been

**14:28** · actually knows when the work has been completed. Otherwise, you just have an

**14:30** · completed. Otherwise, you just have an agent that's just drifting in the wrong

**14:32** · agent that's just drifting in the wrong direction. A loop is only ever as good

**14:34** · direction. A loop is only ever as good as the thing that decides when it's

**14:35** · as the thing that decides when it's finished. If you get the checker right,

**14:38** · finished. If you get the checker right, the real feedback, the proper

**14:39** · the real feedback, the proper computational and inferential checks, a

**14:41** · computational and inferential checks, a human watching the things that actually

**14:43** · human watching the things that actually matter, then you can potentially set it

**14:44** · matter, then you can potentially set it running and walk away. If you get it

**14:47** · running and walk away. If you get it wrong, then you potentially just have

**14:48** · wrong, then you potentially just have loops that are burning through your

**14:49** · loops that are burning through your token budget. If you want to learn how

**14:51** · token budget. If you want to learn how to build expert level AI systems from

**14:53** · to build expert level AI systems from the ground up, then make sure to check

**14:55** · the ground up, then make sure to check out the AI Architect's course within our

**14:56** · out the AI Architect's course within our community, the AI Automators, where

**14:58** · community, the AI Automators, where there's over 50 lessons covering

**15:00** · there's over 50 lessons covering everything from agentic retrieval to

**15:02** · everything from agentic retrieval to harness engineering. You'll get access

**15:03** · harness engineering. You'll get access to starter apps, lots of other

**15:05** · to starter apps, lots of other resources, and a global network of AI

**15:07** · resources, and a global network of AI builders. Thanks for watching.
