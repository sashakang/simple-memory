---
title: "How Anthropic Teams ACTUALLY use Claude Code day to day (for non-engineers)"
source: "https://www.youtube.com/watch?v=l4mSSN6exGg"
author:
  - "[[Simon Scrapes]]"
published: 2026-06-05
created: 2026-06-28
description: "🚀 Build agentic systems that run your business: https://skool.com/scrapes  Don't miss the next build - https://www.youtube.com/@simonscrapes?sub_confirmation=1 Anthropic’s guide on..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=l4mSSN6exGg)

🚀 Build agentic systems that run your business: https://skool.com/scrapes 
Don't miss the next build - https://www.youtube.com/@simonscrapes?sub_confirmation=1
Anthropic’s guide on how teams use Claude Code: https://www-cdn.anthropic.com/58284b19e702b49db9302d5b6f135ad8871e7658.pdf 

Anthropic recently revealed how their own non-engineering teams use Claude Code, and it's not what you'd expect. In this tutorial, we break down the four key patterns used by their legal, marketing, and finance teams to get real work done without writing complex code. Learn the mindset and strategies that will change how you approach building with Claude Code. 

00:00 - How Anthropic Teams ACTUALLY Use Claude Code
00:47 - #1: It's Not About Prompting
02:30 - #2: Building Repeatable and Modular "Skills"
04:27 - #3: Automate the Grind, Not Yourself
07:23 - #4: The "Slot Machine" Mindset
#claudecode #anthropic #claudecodetutorial

## Transcript

**0:00** · Claude Code is as powerful as it is

**0:01** · daunting to start using. But recently

**0:03** · Anthropic published a guide showing how

**0:05** · their non-engineering teams actually use

**0:06** · it to get real work done. And the way

**0:08** · they use Claude Code is very different

**0:10** · from most of the advice you've seen

**0:11** · online. So in this video I want to break

**0:12** · down the four patterns that kept showing

**0:14** · up across every team and why I think

**0:16** · they change how any business owner

**0:17** · should be using Claude Code. Now the

**0:19** · guide talks through 10 internal teams

**0:20** · and the ones I cared about weren't the

**0:22** · engineers. They were legal, marketing,

**0:24** · design, and finance. People with no

**0:26** · coding background getting real usage out

**0:28** · of Claude Code. And four patterns showed

**0:30** · up again and again. How they prompt it

**0:31** · to get better results, how they turned

**0:33** · repeated work into skills, the clear and

**0:35** · narrow use cases they actually use it

**0:37** · for, and how they actually run a session

**0:39** · across their team. So let's start

**0:40** · [music] with how they prompt it.

**0:42** · Now most people think getting good at

**0:44** · Claude Code is about writing the perfect

**0:46** · prompt. And this was bred into us from

**0:47** · earlier models and ChatGPT where the

**0:50** · right prompt had an outsized effect on

**0:52** · the quality of what you got back. You'd

**0:54** · sit there crafting this huge clever

**0:55** · instruction set, you'd hit enter, and it

**0:57** · would sometimes do well and other times

**0:59** · not. But Claude Code isn't that and none

**1:01** · of these teams prompt it that way at

**1:03** · all. So here's what they actually do.

**1:04** · The legal team plans the whole task or

**1:07** · session in claude.ai first in the

**1:09** · browser, then they move over to Claude

**1:11** · Code only once they know what they're

**1:12** · building. And importantly, they tell it

**1:15** · to slow down and go one step at a time.

**1:17** · So they're not expecting everything to

**1:18** · work out of the box from a single

**1:20** · instruction. The product design team

**1:22** · keeps a custom memory file that

**1:23** · practically says, "I'm a designer with

**1:25** · little coding experience. Give me

**1:27** · smaller, incremental changes." Then

**1:29** · growth marketing brainstorms the entire

**1:31** · workflow up front before writing even a

**1:34** · single prompt. And the data team has

**1:35** · their finance people write a plain text

**1:37** · file describing their workflow. Then

**1:39** · they just drop it into Claude Code to

**1:41** · run it. So if you take the common

**1:42** · threads here, nobody's actually writing

**1:44** · clever prompts. They're doing three

**1:45** · things. They're creating a context

**1:46** · memory file that tells Claude who they

**1:48** · are and how they work. And then finally

**1:50** · they're going after a task step-by-step,

**1:52** · not expecting one giant ask to return an

**1:55** · exact result. And that contextual or

**1:57** · file is the bit that most people skip.

**1:59** · The stuff Claude knows about you before

**2:01** · you've typed anything is absolutely

**2:02** · critical to getting good results. So, if

**2:04** · we translate it back to your setup, it's

**2:06** · all about being specific in your

**2:07** · Claude.md file and any other shared

**2:09** · context field that you load in, like how

**2:11** · you sound in your brand voice files or

**2:12** · who you target in your positioning file.

**2:14** · So, this all feels closer to organizing

**2:16** · something like a Notion page rather than

**2:17** · actually coding or prompt engineering.

**2:19** · So, it goes back to highlight the

**2:20** · importance of getting the context right

**2:22** · and then prompting becomes actually the

**2:24** · trivial part.

**2:25** · Now, once they've nailed how to inject

**2:28** · the right context, they also worked out

**2:30** · how to do that on a repeatable,

**2:31** · consistent basis by creating skills for

**2:34** · anything they do more than once. But,

**2:35** · how they built them was very intentional

**2:37** · and specific. And that's to get the most

**2:38** · out of them. And at its core, a skill is

**2:40** · just your good prompt with a set of

**2:42** · step-by-step instructions saved in a

**2:44** · folder so that Claude can reach for it

**2:46** · whenever it's needed. And then add in

**2:47** · the additional context for each step,

**2:49** · like the planning stages we mentioned

**2:50** · before. So, there's a right way to build

**2:52** · a skill. And if you're doing these three

**2:53** · things, you'll absolutely nail it. So,

**2:55** · number one is starting with the name and

**2:57** · the description. This is the part that

**2:58** · Claude reads every single time into its

**3:00** · memory and it's how Claude decides

**3:01** · whether to load that skill at all. So,

**3:03** · it sits in memory permanently. So, if

**3:05** · the description's vague, Claude won't

**3:07** · know when to use it. And if it's

**3:08** · specific, it will grab it exactly the

**3:10** · right moment without you even having to

**3:11** · ask it to. So, there's a couple of

**3:13** · things that you need to make sure you do

**3:14** · in that description. Firstly, you tell

**3:15** · it when it should be called, like use

**3:17** · when a user wants marketing copy

**3:18** · reviewed. You should say when it

**3:20** · shouldn't be called, like does not

**3:21** · trigger for blog posts. And then of

**3:23** · course what it actually does. So, it

**3:24** · analyzes copy against proven frameworks

**3:27** · and rewrites to match brand voice and

**3:29** · ICP. So, a specific name and description

**3:31** · there. Now, number two, the skill.md is

**3:33** · just your step-by-step instructions. So,

**3:34** · these are the actual instructions, but

**3:36** · try not to bloat these. Keep them under

**3:38** · 200 lines because the biggest mistake is

**3:40** · cramming everything into one file. The

**3:42** · top tip here is to keep it short and

**3:44** · focus just on the steps, which brings us

**3:46** · to number three. Put your detailed

**3:47** · examples, the examples that you want to

**3:49** · show as good practice, in separate

**3:51** · reference files and point to them from

**3:53** · the skill.md. So, instead of stuffing

**3:55** · everything into memory at once, Claude

**3:57** · only loads the deeper details when a

**3:59** · task actually needs it. So, think a

**4:01** · short file at the top in the skill.md,

**4:03** · and the heavy detail tucked away in the

**4:05** · reference folder until it's called for.

**4:07** · So, now you know how they prompt it and

**4:09** · how they get consistent results with

**4:10** · skills. But, that still leaves the

**4:11** · bigger question. What are Anthropic's

**4:13** · non-engineering teams actually using it

**4:15** · for? Because this is where most advice

**4:16** · online gets it quite wrong, actually.

**4:18** · So, let me show you some real tasks

**4:20** · these teams are running day-to-day.

**4:22** · Now, most so-called experts online

**4:25** · consistently reference the holy grail,

**4:26** · replacing yourself with something like

**4:28** · low code. So, why are they still

**4:30** · involved in their own businesses if

**4:32** · these agents are just running their

**4:33** · business in the background? And as you'd

**4:35** · expect, Anthropic's own non-technical

**4:37** · teams don't do that at all and don't

**4:39** · advocate for doing that. Not one of them

**4:41** · talks about autonomous tasks as a huge

**4:43** · contributor to the value and results

**4:45** · they get from Claude Code. But, what

**4:46** · they actually do is much narrower. So,

**4:47** · growth marketing is literally just the

**4:49** · team of one person at Anthropic. That's

**4:52** · right, literally just one person. So,

**4:53** · they built a workflow that takes a

**4:55** · spreadsheet of hundreds of existing ads

**4:56** · and spins out hundreds of new variations

**4:58** · from those existing ads in minutes. But,

**5:00** · they, as the human in the loop, still

**5:02** · pick out which ones go live. They also

**5:04** · built a Figma plugin that turns one

**5:05** · mockup into a hundred ad variations for

**5:08** · them to review. Now, the legal team

**5:10** · built tools to route reviews to the

**5:12** · right lawyer. So, it's effectively

**5:13** · augmenting the admin work they'd usually

**5:15** · do. Now, product design shipped a copy

**5:17** · change across an entire code base in two

**5:19** · 30-minute calls. So, instead of a week

**5:20** · back and forth, they were able to

**5:22** · actually make those changes across what

**5:23** · I can imagine is a huge code base in

**5:26** · 30-minute calls. But, if you reflect

**5:28** · again on the shape of every one of those

**5:30** · tasks, Claude is doing the heavy,

**5:32** · repetitive lifting, the generating, the

**5:34** · finding, the drafting, and the human is

**5:36** · staying at the decision point. So, the

**5:38** · marketer doesn't ask Claude to run the

**5:39** · ad account, they ask it for the

**5:40** · time-consuming, repeatable steps, the

**5:42** · hundred variations of ads for an

**5:44** · existing ad. Then, they choose. That's

**5:46** · the difference between augmenting your

**5:48** · work and trying to go completely

**5:50** · autonomous. And there's a detail in the

**5:51** · marketing example there worth pulling

**5:53** · out. They didn't write one giant prompt

**5:55** · to make all those ads. They actually

**5:56** · split it into two specialized

**5:58** · sub-agents. So, one that only writes

**6:00** · headlines and is specialist at that, and

**6:01** · one that only writes descriptions. And

**6:03** · the reason that works so well is each

**6:04** · one runs with its own clean context

**6:06** · focused on a single job. So, it's the

**6:08** · same principle again as the skills,

**6:10** · small, focused, composable. We can use

**6:13** · them together with other skills or

**6:15** · agents too. But, you can see they all

**6:16** · use them as a narrow worker that does

**6:18** · one thing instead of a giant prompt that

**6:21** · tries to get it to do absolutely

**6:22** · everything. And this is what I mean when

**6:23** · I say humans in the loop used as a

**6:25** · design choice. So, every one of these

**6:26** · workflows we've seen is the same shape.

**6:28** · They have an input, they're doing some

**6:30** · sort of data transformation in the

**6:31** · middle, and they have an output with a

**6:32** · person sitting at that output checkpoint

**6:35** · to do the review. So, the system's doing

**6:36** · the grind on the repetitive work, and

**6:38** · then it stops and actually waits for

**6:39** · you. And that checkpoint is the thing

**6:41** · that makes the output good enough to

**6:42** · actually ship, preventing AI slop, so to

**6:45** · speak. So, pattern three then is don't

**6:47** · automate yourself out of it. Automate

**6:49** · the repetitive part and keep yourself at

**6:51** · the decision points, the bit where you

**6:52** · add value. Use human in the loops as a

**6:54** · design principle. And quickly, if you're

**6:56** · getting value from this, do me a favor

**6:58** · and hit the subscribe button below

**6:59** · because YouTube tells me the

**7:00** · overwhelming majority of you watching

**7:02** · this right now aren't subscribed, and it

**7:04** · genuinely helps me reach more people.

**7:05** · So, back to it. You know how to prompt,

**7:07** · how to create repeatable skills, and

**7:09** · what kind of things to use it for. But,

**7:11** · the next one is a mindset shift that

**7:13** · I've not seen before anywhere else. It

**7:15** · could change the way you think about

**7:16** · using Claude Code going forwards.

**7:18** · So, let's imagine a scenario. You start

**7:20** · a session, you've exchanged 10 messages

**7:23** · back and forth, and Claude starts to

**7:24** · drift off course. It's time to start

**7:26** · correcting it, re-explaining, getting it

**7:28** · to work back some of the mistakes it's

**7:30** · made. That's probably sounding quite

**7:31** · familiar. It's pretty much ChatGPT 101

**7:33** · right there. But, believe it or not,

**7:35** · Anthropic's team do the complete

**7:36** · opposite of this. They treat Claude Code

**7:38** · like a slot machine. And this This data

**7:40** · science team's actual phrase. "Save your

**7:42** · state, let Claude run for 30 minutes,

**7:45** · then either accept the result or start

**7:47** · completely fresh." And the engineering

**7:48** · team backs this up. They save

**7:49** · checkpoints constantly, so they can roll

**7:51** · back in seconds. And they're honest that

**7:53** · Claude nails it on the first go only

**7:55** · about a third of the time. The product

**7:57** · team starts every session from a clean

**7:59** · slate for the same reason. And across

**8:01** · all three of those examples, nobody

**8:03** · tries to correct the mistakes if they

**8:05** · get a bad output. They actually reset it

**8:07** · and rewind it. And you can literally do

**8:08** · this with a rewind flag in Cycle code.

**8:11** · And I know that I'm guilty, too, of

**8:13** · trying to get it to correct itself

**8:14** · because the instinct here is that

**8:15** · actually starting over wastes the work

**8:17** · and takes longer. But apparently,

**8:19** · restarting fresh actually has a higher

**8:20** · success rate than trying to rescue a

**8:22** · session that's actually starting to

**8:24** · drift off course. So, always pull the

**8:25** · lever on the slot machine again, so to

**8:27** · speak, if the result you're getting is

**8:30** · starting to drift off course, which is a

**8:31** · complete mindset shift not to try and

**8:34** · just rework it. So, across every

**8:35** · non-technical team in Anthropic's own

**8:37** · guide, legal, design, marketing,

**8:39** · finance, data, the unlock is the same

**8:42** · four plans. Get your context right, save

**8:44** · repeated work as skills, point it at

**8:46** · narrow jobs with you at the decision

**8:47** · points, and treat it like a slot

**8:49** · machine. And none of it, if you've

**8:50** · noticed, requires being technical. The

**8:52** · people getting the most out of Claude

**8:53** · code aren't the engineers. Now, if you

**8:54** · want to jump deeper into building out

**8:56** · repeatable processes through good

**8:57** · skills, then check out the next video.

**8:59** · Thanks for watching.
