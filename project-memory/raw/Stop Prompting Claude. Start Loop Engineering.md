---
title: "Stop Prompting Claude. Start Loop Engineering."
source: "https://www.youtube.com/watch?v=YAS4ojuhbW4"
author:
  - "[[Austin Marchese]]"
published: 2026-06-19
created: 2026-06-28
description: "Get my free 5-day AI playbook (what I used to build a $25M+ startup): https://the-ai-playbook.com/loop  In this video, I break down Loop Engineering (Claude Loops), the shift Boris..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=YAS4ojuhbW4)

Get my free 5-day AI playbook (what I used to build a $25M+ startup): https://the-ai-playbook.com/loop

In this video, I break down Loop Engineering (Claude Loops), the shift Boris Cherny and Peter Steinberger both made when they stopped prompting their AI and started loop engineering instead. You'll learn what a loop actually is, when to use one, the 5 building blocks every successful loop needs, and how to build your first loop today even if you have zero technical experience.

Timestamps:
(0:00) - Stop Prompting Claude, Start Writing Loops
(0:46) - Part 1: What a Loop Actually Is
(2:34) - Part 2: The 5 Building Blocks
(2:38) - Block 1: The Trigger
(4:01) - Block 2: Execution Skills
(5:15) - Block 3: Goal and Verification
(7:53) - Block 4: Output and Memory
(9:16) - Part 3: Build Your First Loop Today

What to watch next ⤵️
- The only skills you need to 10x: https://www.youtube.com/watch?v=AfKoqFwC7Ew
- Stop prompting, start agentic engineering: https://www.youtube.com/watch?v=7zZy1QTvokM
- Karpathy's 10x Claude Code method: https://www.youtube.com/watch?v=yfeHoOkn2TI

--------
FOR INDIVIDUALS:
- Free 5-day AI playbook (what I used to build a $25M+ startup): https://the-ai-playbook.com/loop
- Use BuildPartner to build 10x faster with Claude Code (try free): https://buildpartner.ai/loop

FOR BUSINESSES, Ways to work with me:
- Apply for my Executive AI Coaching Program: https://www.theincubator.xyz/apply/loop
- Want to build a SaaS product without hiring a CTO? https://www.theincubator.xyz/eng/loop
--------

If you're new here, I'm Austin Marchese. How I got here...
16: First business (SAT Math Tutor)
22: Graduated Stevens Tech, 4.0, College Basketball, software engineering job at JPM
23: Bitcoin ATM company + building algorithms for a professional gambler (fun story)
24: Started creating content, grew 100k+ followers, built first agency, The Incubator
25: Scaled agency to 15+ team members, $75K/M while working full time
26: Quit my job, joined a startup called IYK
27: Became COO of a $25M+ tech startup, worked with Ed Sheeran, Chance the Rapper and more
28: Built a $20M+ real estate portfolio in the background
29: Transitioned from IYK, re-launched The Incubator, grew it to a 6-figure biz in 30 days. Now building BuildPartner.ai

To everyone who's spending time learning and putting the work in, cheers. Anyone can make comments from the sidelines but not everyone can build...

- Austin

Follow/Subscribe

- Instagram: https://www.instagram.com/austin.marchese/
- Youtube: https://www.youtube.com/@austin.marchese

## Transcript

_Caption track: English auto-generated or provided._

**0:00** · Boris Cherny, the creator of Claude

**0:01** · code, just said something that should

**0:03** · change how you use AI forever. He said,

**0:05** · "I don't prompt Claude anymore. My job

**0:06** · is to write loops." Then I found a tweet

**0:08** · from Peter Steinberg, the creator of

**0:09** · Open Claude, saying the exact same

**0:11** · thing. You shouldn't be prompting coding

**0:13** · agents anymore. You should be designing

**0:15** · loops that prompt your agents. There's

**0:16** · endless AI hype out there, but when two

**0:18** · people who literally build the tools

**0:19** · that we're using tell you to stop

**0:21** · prompting and start building loops, I

**0:23** · listen. So, I went deep on loop

**0:25** · engineering and realized something. It's

**0:26** · actually really simple. Most

**0:28** · people just overcomplicate it. So, in

**0:30** · this video, I'm breaking loop

**0:31** · engineering down into three parts. Part

**0:33** · one, what a loop actually is and when to

**0:35** · use them. Part two, the four things

**0:38** · every successful loop needs. And part

**0:40** · three, the most important part, how you

**0:42** · will build your first loop today, even

**0:44** · if you have no technical experience. So,

**0:46** · part one, what actually is a loop and

**0:48** · how does it compare to a normal prompt?

**0:49** · Unlike a normal prompt, which runs once

**0:51** · and then stops, a loop is a prompt that

**0:54** · runs over and over again until a

**0:56** · specific task or goal is complete.

**0:58** · Listen to how Boris thinks about his

**0:59** · day-to-day now.

**1:00** · >> Now, what's actually leveled up, I think

**1:02** · again, to the next level of abstraction,

**1:03** · where I don't prompt Claude anymore. I

**1:06** · have loops that are running. They're the

**1:07** · ones that are prompting Claude and kind

**1:09** · of figuring out what to do. My job is to

**1:11** · write loops.

**1:11** · >> So, it's clear. Instead of prompting

**1:13** · Claude 100 times to complete a task, you

**1:15** · should now be thinking about how to

**1:16** · create loops to accomplish clear goals.

**1:18** · This sounds great, but when should you

**1:19** · actually use it? Well, there's a

**1:20** · four-condition test that I run when

**1:22** · determining if I should create a loop or

**1:24** · not. The first condition is, does the

**1:26** · task repeat? For any one-time task, just

**1:28** · use a prompt. Second is, is there a

**1:29** · clear definition of done? When I was the

**1:31** · COO of a $25 million tech startup,

**1:33** · whatever task we were doing, we wanted

**1:35** · to have a clear definition of how we

**1:37** · would quantify if the task was done. And

**1:39** · a lot like humans doing tasks, the most

**1:41** · successful loops have a clear definition

**1:43** · of done and a way to verify the results.

**1:46** · Now, this is an art and not necessarily

**1:47** · a science, and we'll cover that in a

**1:49** · bit. Three is, can you afford to be

**1:51** · wasteful? So, loops will automatically

**1:53** · prompt itself until a task is complete.

**1:55** · So, it can use a lot of tokens. Now,

**1:57** · there's ways to limit this, which we

**1:58** · will cover, but if you're always running

**2:00** · into token limit issues, you want to be

**2:02** · a bit more strategic using this. And

**2:04** · four is, does the loop have all the

**2:05** · necessary tools to complete a task? For

**2:08** · example, if you're making a website,

**2:09** · does it have the ability to check that

**2:11** · the website is live and accessible to

**2:13** · anyone? These tools will be used in the

**2:14** · verification and the implementation

**2:16** · process. If the answer is yes to all

**2:18** · four of these conditions, you now have a

**2:20** · candidate for building a loop. Here is a

**2:21** · prompt to audit your workspace and rank

**2:24** · your loop candidates using this four

**2:26** · condition test. The prompt's on screen,

**2:28** · and you know what loops are, and you

**2:29** · conceptually understand when to use

**2:31** · them. But, how do you build a loop that

**2:33** · actually works? Part two is the four

**2:35** · building blocks for successful loops.

**2:37** · The first block is the trigger. This is

**2:39** · what starts your loop. Every loop needs

**2:41** · a trigger. This is the thing that kicks

**2:43** · it off. And there are a lot of ways to

**2:44** · set this up, but these are the three

**2:45** · simplest ways. The first is actually

**2:47** · {slash} loop. If you type {slash} loop

**2:49** · into Claude, it will let you

**2:50** · automatically run something at a set

**2:52** · interval. For example, {slash} loop

**2:54** · every six hours, check today's weather

**2:56** · and notify me if I need to change my

**2:58** · plans based on my calendar. This is nice

**3:00** · because it's very simple, but it's

**3:01** · running on your local machine. So, if

**3:02** · you close your laptop, it'll just stop.

**3:04** · The second is {slash} schedule. This

**3:05** · lets you run something automatically in

**3:07** · the cloud at any time or day in whatever

**3:10** · cadence you want. So, you can run the

**3:11** · prompt that I had just mentioned for the

**3:13** · loops, but instead have it run at 8:00

**3:14** · a.m. every day, and it'll run remotely

**3:16** · instead of on your machine. And the

**3:17** · third is custom loop orchestration

**3:19** · skills. It's a mouthful, but this is

**3:21** · actually how I run all of my loops. I

**3:23** · create a single loop orchestration skill

**3:25** · that I run that kicks off the entire

**3:27** · loop. It has all of the settings

**3:28** · configured about what the goal is, how

**3:30** · to complete the loop, how to verify it.

**3:32** · In that same weather example I

**3:33** · mentioned, I would have a single skill

**3:35** · that would be {slash} check weather

**3:37** · loop, and I would just type that into my

**3:39** · terminal, and I would hit enter. Here's

**3:40** · a prompt to help you create that custom

**3:42** · loop orchestration skill. Block one is a

**3:44** · trigger, and the next block is about

**3:46** · actually doing the work. And I know

**3:47** · we're going through these concepts

**3:48** · pretty quickly, so I put together a free

**3:50** · 5-day email series where I walk through

**3:52** · a lot of the concepts we cover in this

**3:53** · video. That's linked below and based on

**3:55** · over 6,000 people that have gone through

**3:57** · it, I'm highly confident that you're

**3:58** · going to love it. But, if you don't, you

**4:00** · can unsubscribe at any time. Block two

**4:02** · is the execution skills. I have

**4:03** · extensive videos on my channel about

**4:05** · Claude skills, but in short, it is a

**4:07** · save set of instructions that allows

**4:09** · Claude to run the same thing every

**4:11** · single time. Simply put, it's like a

**4:12** · prompt that you have saved that you can

**4:14** · easily rerun instead of having to type

**4:16** · it. In the first block, we created a

**4:17** · {slash} check weather loop and

**4:19** · orchestration skill that runs the whole

**4:21** · loop. Execution skills are different.

**4:23** · These are the things that actually do

**4:24** · the task. Each one is a single

**4:26** · specialized job the orchestration calls.

**4:29** · Of the four building blocks I'm going to

**4:30** · cover, this is the most important. In my

**4:32** · eyes, the rule is simple. You don't

**4:34** · build a loop without battle-tested

**4:36** · skills behind it. The reason for this is

**4:38** · these skills know exactly how you want

**4:40** · to get a task done. Back to the check

**4:42** · weather loop. Say you didn't have a

**4:44** · {slash} analyze workout skill, AI would

**4:46** · just say, "It's raining, cancel your

**4:48** · run." But, if I had a {slash} analyze

**4:50** · workout skill that documented that I

**4:51** · actually love running in the rain, the

**4:53** · response would be entirely different.

**4:55** · And this is why I use skill-driven loop

**4:57** · development. Any loop I create has to

**4:59** · have existing skills that I've already

**5:01** · battle-tested. Here's a prompt to

**5:03** · identify which skills make sense for

**5:05** · your workspace. This will look at the

**5:06** · current skills that you've already

**5:08** · established and suggest loops based on

**5:10** · those skills. This strategy is so

**5:12** · important and it comes into play in the

**5:14** · next block. Block number three is the

**5:15** · goal and the verification. Every loop

**5:17** · needs two things tied together. A goal,

**5:20** · what you want done, and a verification,

**5:22** · the rule that confirms you completed the

**5:24** · goal. These go together, right? You

**5:25** · can't have a goal unless you're able to

**5:27** · verify the goal was complete. So, here's

**5:28** · how you can do this for both technical

**5:30** · and non-technical tasks. The technical

**5:32** · example is a lot more straightforward.

**5:34** · The goal could be launch a website to

**5:36** · this domain and make sure it loads in

**5:37** · under 2 seconds. To verify, AI could hit

**5:39** · that specific domain, make sure it can

**5:41** · see the content that it expects,

**5:43** · calculate the load time, and then make

**5:45** · sure that the {slash} engineer review

**5:47** · skill approves all the changes. AI will

**5:50** · then know exactly what's needed and then

**5:52** · can verify the results and repeat in a

**5:54** · loop until it's complete. So that's for

**5:56** · technical tasks, but what about for

**5:57** · non-technical things? Well, this is

**5:59** · where it becomes a bit of an art, not a

**6:00** · science. You need to bridge the abstract

**6:03** · to verifiable. Look at the end of the

**6:05** · technical example that I just mentioned.

**6:07** · The slash engineer review skill has to

**6:09** · approve the changes. How does a loop

**6:11** · actually know if code is good or not?

**6:13** · Well, AI is very good at writing code,

**6:15** · so it could just say approved or not

**6:17** · approved. The skill engineer review is

**6:20** · set up to bridge the abstract if code is

**6:23** · good to something verifiable, approved

**6:25** · or not approved. And we used it in a

**6:27** · technical example, but this is actually

**6:28** · the key to creating loops for

**6:30** · non-technical tasks. You have to figure

**6:32** · out a way to verify the final result,

**6:34** · even if it's not quantifiable. So for

**6:36** · example, let's say you have a slash

**6:37** · draft emails loop. The goal could be for

**6:40** · any unread email draft response. The

**6:42** · verification could be make sure all

**6:44** · emails that don't have a response have a

**6:46** · draft, and that draft has been verified

**6:48** · by the slash email review skill, the

**6:50** · slash writing voice skill, and the slash

**6:53** · fact checker skill. You've now

**6:54** · established key things you want to

**6:56** · verify that are inherently abstract, but

**6:58** · you've created a bridge to make them

**7:00** · verifiable. And yes, quantifiable tasks

**7:02** · are easier, no question. But if you

**7:03** · choose the right non-technical task that

**7:05** · you already have skills for, those can

**7:08** · easily become quantifiable. And this is

**7:10** · exactly why skill-driven loop

**7:11** · development matters so much because once

**7:13** · you have a skill, you can actually

**7:15** · convert it to include a verification

**7:18** · element. And this verification element

**7:19** · could be at the end of the output from

**7:21** · that skill, you could say approved or

**7:23** · not approved, or a score from 1 to 10,

**7:26** · etc. Here is a prompt that I've run in

**7:28** · the past to help me convert a normal

**7:30** · skill to a skill that can help with

**7:31** · verification. And one pro tip here with

**7:33** · the goals and the verification and all

**7:35** · of this, if you can have different AI

**7:37** · analyze the output, you'll be able to

**7:38** · get a less biased opinion. One easy way

**7:41** · you can do this in Claude is you could

**7:43** · use the Codex plugin or you can have

**7:44** · Claude spin up sub agents to analyze the

**7:46** · work. Here's a prompt to enforce

**7:48** · separate agent verification within your

**7:50** · loop orchestration skills. Block four,

**7:52** · the output and the memory. The output is

**7:54** · obvious, right? A loop produces

**7:55** · something, a document, updates code

**7:57** · base, live site, Telegram messages,

**8:00** · whatever you want the loop to produce.

**8:01** · The non-obvious thing here that most

**8:03** · people miss is the memory. Every loop

**8:05** · starts from scratch unless you record

**8:06** · what happened. And no memory means that

**8:08** · there's no improvement and you'll end up

**8:10** · wasting tokens because you keep hitting

**8:11** · the same issues over and over again.

**8:13** · Adadi Asmani has one line that sticks

**8:15** · with me. The agent forgets, the repo

**8:17** · doesn't. And from Anthropic docs, they

**8:19** · say, "Provide a place to write notes, as

**8:21** · simple as a markdown file." And so you

**8:23** · really don't need to overthink this

**8:24** · thing, but you need to document what the

**8:26** · results of the loop are. Just use this

**8:28** · prompt, which will update any of your

**8:30** · loop orchestration skills, to write any

**8:32** · lessons learned and run history in a

**8:34** · specific document. Here you can see the

**8:36** · prompt. It'll create an output and

**8:37** · memory files. Now we know the four key

**8:40** · building blocks, a trigger, execution

**8:41** · skills, goals and verification, and

**8:43** · output and memory. And before we apply

**8:45** · this to build our first loop end-to-end,

**8:47** · if this is your first video of mine,

**8:49** · welcome the channel. But if this is your

**8:50** · second or more, here is our anti-slop

**8:52** · agreement. The visuals, the testing, the

**8:54** · hours of research that went into this,

**8:55** · this is entirely built for humans like

**8:57** · you, not for AI robot scrapers. So all I

**9:00** · ask is you subscribe as part of this

**9:01** · agreement to help this content reach

**9:03** · more people so I can keep doing these

**9:05** · videos. Also, every video I give away a

**9:06** · Claude Max subscription. So comment

**9:08** · below with what you're building to

**9:09** · enter. This video's winner is the goat,

**9:12** · Bob Dobbs, who's working on a home

**9:14** · management app. All right, that's enough

**9:16** · of that. Let's go to part three, build

**9:18** · your first loop today. The key here is

**9:19** · you need to start small and follow

**9:21** · skill-driven loop development. Ask

**9:22** · yourself, what is the smallest thing

**9:24** · you've already done and proved works

**9:26** · that you can create a loop for. Once

**9:27** · you've identified that, use the four

**9:29** · condition test that I mentioned earlier,

**9:31** · which again, quickly you can see on

**9:32** · screen. And if it passes all that, it's

**9:34** · time to create a loop. So if you already

**9:36** · have an idea, here is a prompt to build

**9:38** · out a loop with all of the concepts that

**9:40** · I've mentioned in this video. Baked into

**9:42** · that is everything that I've covered.

**9:43** · Now, if you have no idea what to build,

**9:45** · here is a prompt that leans on

**9:47** · skill-driven loop development to

**9:49** · identify candidates from your past

**9:51** · session history. For either of these

**9:53** · prompts and for any prompt that I

**9:54** · covered in this or previous videos,

**9:56** · screenshot it and then just send it into

**9:58** · Claude and that's essentially the same

**9:59** · as writing the prompt. And the best part

**10:01** · of what this will create, which is a

**10:02** · skill, is you don't have to think about

**10:04** · using /loop or /goal to establish goals.

**10:07** · You just get the loop orchestration

**10:08** · skill that abstracts all of this

**10:10** · complexity away from you. You just type

**10:12** · that into Claude, hit enter, and then

**10:13** · monitor the results. When you do this,

**10:15** · one of my favorite features is that

**10:17** · you'll notice both of these prompts have

**10:19** · one important guardrail. I call it loop

**10:21** · training mode. So, the first couple

**10:22** · times you use a new loop, you want to

**10:24** · make sure the loop pauses at every step

**10:27** · until you approve the process. The

**10:28** · reason for this is you want to verify

**10:30** · that it's actually doing what you want

**10:32** · it to be doing and it's not just burning

**10:34** · through all of your tokens. When you

**10:36** · have this loop training mode set up, the

**10:38** · output could look something like this.

**10:39** · Quick check before I burn the tokens.

**10:41** · Then it waits for your approval and

**10:42** · continues on the process. After you've

**10:44** · done this and you know that the loop is

**10:46** · doing what you want it to do, you can

**10:48** · just turn testing mode off by running

**10:50** · this prompt. And this is really

**10:51** · important because you're going to get a

**10:52** · deeper understanding of the process and

**10:54** · ultimately these tokens aren't free, so

**10:56** · this will save you money and it will

**10:58** · save you time because you'll know the

**10:59** · output is what you want. Now, before you

**11:01** · go crazy with all these loops, I have

**11:03** · one rule of thumb. If a goal is less

**11:05** · quantifiable, then you need to break

**11:07** · down loops into much smaller goals where

**11:10** · the output is at key checkpoints in the

**11:12** · process. Think of AI like an intern. If

**11:14** · you just said, "Plan a corporate party,"

**11:16** · it could do anything, but you would

**11:18** · probably want to have key checkpoints at

**11:21** · what date to pick, where the venue is,

**11:23** · and the theme of the party. And as

**11:25** · somebody who throws an annual Christmas

**11:26** · party, that's the party of the year in

**11:28** · New York City, I I know how to throw a

**11:29** · party, it needs a theme. But anyway,

**11:31** · those decisions shape the entire party.

**11:33** · It's the same with loops. What are the

**11:35** · key moments where if the loop picks the

**11:37** · wrong direction, the rest of the loop is

**11:39** · entirely shot? Those are your human

**11:42** · verification checkpoints. Ultimately,

**11:44** · the more of these key verification

**11:46** · checkpoints that you don't actually

**11:48** · verify, the more the AI can go off

**11:50** · course. So, be very mindful of that,

**11:52** · specifically for non-measurable tasks.

**11:54** · With all that, my favorite thing about

**11:56** · loop engineering is the problem-solving

**11:58** · muscle it'll force you to flex. So, go

**12:00** · pick something small and build a loop

**12:02** · orchestration skill for it. Now, if you

**12:04** · like this video, you will love this

**12:05** · video where I do a deep dive on the only

**12:07** · Claude skills you need to 10x your

**12:09** · output. The topics I cover there will

**12:11** · help your loops go from good to great.

**12:13** · I'll see you in the next one. Peace.
