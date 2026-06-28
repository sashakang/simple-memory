---
title: "Finally. Agent Loops Clearly Explained."
source: "https://www.youtube.com/watch?v=EuzYhzB0vbI"
author:
  - "[[Nate Herk | AI Automation]]"
published: 2026-06-19
created: 2026-06-28
description: "My FREE AI OS Course: https://www.skool.com/ai-automation-society/about?el=agent-loops-explained&hcategory=youtube-videos&utm_campaign=free-group Full courses + unlimited support: ..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=EuzYhzB0vbI)

My FREE AI OS Course: https://www.skool.com/ai-automation-society/about?el=agent-loops-explained&hcategory=youtube-videos&utm_campaign=free-group
Full courses + unlimited support: https://www.skool.com/ai-automation-society-plus/about?el=agent-loops-explained&hcategory=youtube-videos&utm_campaign=ais-plus
Apply for my YT podcast: https://podcast.nateherk.com/apply
Work with me: https://uppitai.com/

My Tools💻
FREE MONTH voice to text: https://get.glaido.com/nate
Code NATEHERK for 10% off VPS (annual plan): https://www.hostinger.com/vps/claude-code-hosting

Everyone is talking about agent loops and loop engineering right now, but most of the advice assumes you are a hardcore coder running fleets of agents around the clock. 

In this video I break down what an agent loop actually is (reason, act, observe, repeat), why the verification step matters more than the architecture, and how to think about a "done" criteria that your agent can actually check. 

I walk through a few real loops I ran, including thumbnail scoring, a three.js plane, and an Abbey Road recreation, and explain why loops are about getting you closer on the first try, not perfect output. If you have been feeling behind because you are not running five agents at once, this one is for you.

Sponsorship Inquiries:
📧 nate@smoothmedia.co

Connect with me:
https://www.linkedin.com/in/nateherkelman/
https://x.com/nateherk
https://www.instagram.com/nateherk/

TIMESTAMPS 
0:00 Intro
0:31 What Loop Engineering Means
2:23 How an Agent Loop Works
5:29 Three Ways to Build Loops
6:13 Demo: Thumbnail Scoring
8:12 Demo: Three.js Plane
9:08 Demo: Abbey Road Recreation
10:42 What Makes a Loop Work
12:40 Does This Apply to You?
14:06 Resources & Wrap-Up

## Transcript

_Caption track: English auto-generated or provided._

**0:00** · Right here, I've got four different

**0:01** · agents that are looping, calling other

**0:02** · sub agents, and writing all these

**0:04** · prompts for me, and designing systems

**0:05** · for me. But, is this actually

**0:06** · productive, or is that just a cool demo?

**0:08** · Here's your monthly reminder that you

**0:09** · shouldn't be prompting coding agents

**0:11** · anymore. You should be designing loops

**0:13** · that prompt your agents. Boris Cherny

**0:15** · and Peter Steinberg publicly said they

**0:17** · no longer prompt their coding agents.

**0:19** · They write loops. A loop is three

**0:20** · things: a trigger, an action, and a stop

**0:23** · condition. If you're still writing loops

**0:24** · that prompt coding agents, you're

**0:25** · falling behind. You need to build a meta

**0:27** · agent that infers what loops you would

**0:29** · have wanted based on your vibe, and then

**0:30** · write those loops. We're seeing a ton of

**0:32** · talk about agent loops, loop

**0:33** · engineering, whatever you want to call

**0:34** · it. So, I wanted to make a video to

**0:36** · clear up what that actually means.

**0:37** · Because I think that everyone kind of

**0:39** · has their own spin and a different

**0:40** · definition of what this is, and it

**0:42** · applies to everyone very, very

**0:44** · differently. I think that this

**0:45** · definition sums it up pretty well. Loop

**0:47** · engineering is replacing yourself as the

**0:48** · person who prompts the agent. You design

**0:50** · the system that does that instead. A

**0:52** · loop here can be thought of as a

**0:54** · recursive goal, where you define a

**0:55** · purpose, and the AI iterates until

**0:58** · complete. And there's really two most

**0:59** · important pillars of that in my mind,

**1:01** · which are the goal. What is the actual

**1:03** · objective? Something typically

**1:05** · that's objective, not subjective. And

**1:07** · then verification. How does the agent

**1:08** · know what that stop condition is? How

**1:10** · does it check and iterate? So, anyways,

**1:12** · if you take all that advice, and then

**1:13** · you start doing stuff like this, and

**1:15** · designing swarms and fleets of agents

**1:16** · that constantly run 24/7, then you need

**1:19** · to think about what are you actually

**1:21** · doing here? And is this actually moving

**1:22** · the needle? So, first of all, I thought

**1:24** · to myself, how do I actually use agent

**1:25** · loops? Because when you read some of

**1:27** · those tweets that I just showed earlier

**1:28** · in this video, you kind of think to

**1:30** · yourself, okay, if I'm not having five

**1:32** · agents that are continuously around the

**1:34** · clock orchestrating five of their own

**1:36** · agents, then I'm falling behind, or I'm

**1:37** · not using my cloud subscription in the

**1:39** · best way. And I think that that's very

**1:41** · false. Because if you don't understand

**1:43** · what you're doing, then you're probably

**1:45** · just going to scale problems, and you're

**1:46** · going to have a ton of bugs and a ton of

**1:48** · things that you're going to have to fix

**1:49** · later. And also, not all of us are in a

**1:51** · scenario where having agents work 24/7

**1:53** · around the clock actually benefits us.

**1:55** · For example, I don't. I have agents that

**1:57** · do things on a certain cadence and I

**1:58** · have agents that do things based on

**2:00** · certain event actions, but just having

**2:02** · them do 24/7 work for me isn't helpful.

**2:05** · I think if I was working with a team on

**2:06** · a codebase and we were building a

**2:08** · product and we were constantly iterating

**2:09** · and pulling in different things, then it

**2:11** · would maybe make more sense, but for me,

**2:12** · that doesn't apply. So, I just wanted to

**2:14** · come in here, explain this as simple as

**2:15** · I can, and hopefully shed some light on

**2:18** · where you guys can start applying loops

**2:20** · into your workflows and why and how. So,

**2:23** · I actually built an agent loop for this

**2:25** · HTML that we're going to look at today,

**2:27** · and it basically went through a ton of

**2:28** · different sources. It checked 45

**2:30** · sources, whether that was articles,

**2:32** · YouTube video transcripts, X posts. It

**2:33** · looked through a ton of stuff, and then

**2:35** · it kept looping on this until it had a

**2:36** · good idea of what to build. And then

**2:39** · once it built this HTML, this wasn't V1.

**2:41** · This was probably V7. It had to keep

**2:43** · checking, screenshotting, reviewing,

**2:44** · iterating, and then it finally said,

**2:46** · "Okay, we're done. This is what we got."

**2:48** · So, let me walk through this with you

**2:49** · guys. An agent loop is just an AI that

**2:51** · reasons on what to do, acts on what to

**2:53** · do, starts implementing, and then it

**2:54** · observes the result. And it will do that

**2:57** · over and over and over until some sort

**2:58** · of goal is met, until it knows we've hit

**3:01** · the stop criteria, this is good, I'm

**3:03** · going to stop now. And a really simple

**3:04** · visual that I like to think about is AI

**3:06** · is never perfect, right? It's never

**3:08** · going to one-shot something and you just

**3:09** · accept that final output. And so, if we

**3:11** · have attempts on the x-axis and we have

**3:13** · quality on the y-axis, let's think about

**3:15** · this. On attempt one, if you are just

**3:18** · giving your agent some sort of simple

**3:20** · task, maybe you get to like, let's just

**3:21** · say attempt one, you get to 50%, and

**3:23** · then you look at that and say, "Okay,

**3:24** · here are some changes to make." And then

**3:26** · by attempt two, maybe you bump up

**3:27** · another five or 10%. And every time that

**3:29** · you give more feedback and iterate, you

**3:31** · just kind of keep moving up on quality

**3:33** · until you hit somewhere where you're

**3:34** · okay with that, 90, 95%. And so, the

**3:37** · whole idea is why don't we outsource

**3:38** · this part, this feedback and iteration

**3:41** · loop, to an agent rather than having the

**3:42** · human do that? Cuz this is going to

**3:44** · happen either way. So, if we have an

**3:46** · agent do that instead of a human, then

**3:47** · what might happen is on attempt one, we

**3:50** · will go straight up to here. And then we

**3:52** · can give a little bit more feedback. And

**3:53** · then by attempt, you know, three or

**3:55** · four, we're already so much higher than

**3:56** · where we would have been without sort of

**3:58** · that agent verification loop right

**4:00** · there. And that's why a lot of people

**4:01** · are explaining this in a different way,

**4:03** · where some people have the think act

**4:05** · see, you know, we basically like reason

**4:07** · act observe reason act observe. Some

**4:09** · people have the model just going back

**4:10** · and forth with tools back and forth back

**4:11** · and forth. Some people have just, you

**4:13** · know, a goal that runs completely

**4:14** · unattended. And some people are using

**4:16** · these like fleets of agents with

**4:17** · managers prompting other agents

**4:18** · prompting other agents. And it's just

**4:20** · like, you know, those Russian nesting

**4:22** · dolls. So that's why I wanted to put

**4:23** · this into kind of the main pillars,

**4:25** · which I think are reason act observe.

**4:28** · Think of this like a smart intern that

**4:29** · you don't micromanage. You hand them a

**4:30** · goal, they figure out what to do next,

**4:32** · they check their own work, and they go

**4:34** · again, and then they only come back to

**4:35** · you and say, "Hey, I'm done." After they

**4:37** · probably checked it a few times and made

**4:39** · some changes. So you would say, "Okay,

**4:40** · Claude code, here's what I want you to

**4:42** · do." We as humans are really, really

**4:44** · good at defining what we want. We're

**4:46** · really good at defining an end goal. And

**4:48** · then on top of that, we have to say,

**4:49** · "Okay, how do you know when that is

**4:51** · done?" So when you're making a cake, you

**4:53** · stick the fork in it, and when it comes

**4:54** · out and it doesn't have batter all over

**4:56** · it, that means it's done. How do you

**4:57** · tell your agent something as objective

**5:00** · as possible, what is the stop criteria,

**5:02** · what is the definition of done? And so

**5:04** · what it will do is it will reason, it

**5:05** · will plan out, and then it will start to

**5:07** · implement. After it implemented, it will

**5:09** · observe. So maybe that's visual

**5:10** · verification, maybe that's running an

**5:12** · actual code test. Whatever it means to

**5:14** · verify, it has to verify. And then after

**5:16** · it looks at the results, it will say,

**5:17** · "Okay, did I meet this done criteria? If

**5:19** · no, I'm going to act again, then observe

**5:21** · again, and then reason. Otherwise, I'm

**5:22** · going to stop, and I'm going to say,

**5:24** · "Okay, Mr. or Mrs. Human, I am done."

**5:26** · And what's really interesting is that

**5:27** · the majority of tasks don't need loops.

**5:29** · What I've started doing is for the

**5:30** · majority of my tasks, I will build some

**5:32** · sort of loop, but it's just because of

**5:34** · the verification, right? This piece is

**5:36** · so important, the verification loop. But

**5:38** · a lot of times, you don't need some sort

**5:39** · of massive agent architecture in order

**5:42** · to run this sort of like dynamic looping

**5:44** · workflow. You You just get it done with

**5:45** · one simple terminal session and a good

**5:47** · prompt. You can have the speed just a

**5:49** · solo loop, which is what I'm typically

**5:50** · doing the most. One agent that's

**5:52** · reasoning, that's acting, observing, and

**5:53** · repeating. And I'll show you guys some

**5:54** · examples of what these loops might look

**5:56** · like in just a sec. You can have a maker

**5:58** · checker, where you have one agent that

**6:00** · does the thing and then one agent that

**6:01** · grades the thing and gives feedback. Or

**6:02** · you can have this sort of manager with a

**6:04** · bunch of helpers. And then as as long as

**6:06** · you've got one main agent that's

**6:07** · orchestrating the whole thing, then you

**6:09** · can build these loops in so many

**6:10** · different ways. So, let me just show you

**6:11** · guys a few examples that I pulled. These

**6:13** · first two that I'm going to show you

**6:15** · were actually from this loop library

**6:16** · that Matthew Berman published. He

**6:18** · created this loop library, which is a

**6:20** · list of agent loops that you can use,

**6:21** · and people can go submit their own. So,

**6:23** · kind of cool to just go in here and play

**6:24** · around with and see what's available.

**6:26** · And I grabbed two for these first two

**6:28** · demos. So, this was the first one right

**6:30** · here. It was a {slash} goal prompt in

**6:32** · Cloud Code to make me a thumbnail. So, I

**6:34** · told it basically what to use to make

**6:36** · them. It says, "Make 10 thumbnail

**6:37** · concepts and score each one against Mr.

**6:39** · Beast YouTube thumbnails using a rubric.

**6:41** · Clarity at small size, curiosity,

**6:42** · emotional pull, visual contrast." Stuff

**6:44** · like that. And after it makes those 10,

**6:46** · it selects the top three, it identifies

**6:48** · the weakest part of each concept, it

**6:49** · improves them, rescores them, and then

**6:51** · it continues iterating on on the

**6:53** · strongest concept until it's satisfied.

**6:55** · So, that's one of the issues with this

**6:56** · prompt here is that

**6:59** · the definition of done was "until you're

**7:01** · satisfied." And sometimes you have to

**7:03** · have these subjective sort of grading

**7:04** · criteria, but you want to get it

**7:06** · objective as objective as possible. The

**7:08** · best agent loops are where you literally

**7:10** · say, "Keep iterating until X metric

**7:13** · equals Y result." You can see right here

**7:15** · what it did is it created 10. We've got

**7:17** · number one, we've got number two, number

**7:18** · three, number four, number five. It

**7:20** · ended up choosing that number one was

**7:22** · one of the top contenders, number two,

**7:24** · and so was number eight. So, then it

**7:25** · iterated on these. You can see here's

**7:27** · number one original, here's number one

**7:29** · V2, here's number two original, here's

**7:31** · number two V2, and here's number eight

**7:33** · original, and here's number eight V2.

**7:35** · And what it did is after those version

**7:36** · twos of all of it, it said, "Okay,

**7:38** · number eight's the best. So, here is

**7:39** · number eight V3." And so, this is the

**7:41** · final thumbnail that we got after we ran

**7:43** · this goal, which took Claude Code 27

**7:46** · minutes right there. So that's one quick

**7:48** · example of the loop. You can see it was

**7:49** · it was scoring each of these, and that's

**7:51** · how it decided on the winner. But the

**7:53** · one thing here is that these scores were

**7:54** · subjective. So if we wanted to improve

**7:56** · this flow, we would try to figure out

**7:58** · how do we make this scoring more

**7:59** · objective? And maybe what we would want

**8:01** · to do is create a separate sub agent

**8:03** · that was a dedicated scorer, and we

**8:05** · would prompt that scoring agent and run

**8:06** · that through a bunch of evaluations so

**8:08** · that we could feel more confident about

**8:10** · its scoring ability. Anyways, let's take

**8:12** · a look at the next one. So the next one

**8:13** · was another slash goal, as you can see

**8:15** · right here. This one took 37 minutes.

**8:17** · And the prompt for this one was right

**8:18** · here, straight from Matthew Berman's

**8:20** · Loop Library. I'm not going to read this

**8:21** · whole thing. You guys can pause it right

**8:23** · there if you want to see. But it was

**8:24** · basically supposed to make a plane using

**8:26** · 3.js. So I'll open that up right here.

**8:28** · We can see this is the spinning plane

**8:29** · that it made. We can sort of zoom in. We

**8:31** · can move it around. And that is what we

**8:34** · got. Now from a looping perspective,

**8:36** · what it had to do was it had to build it

**8:38** · and then verify. Open up the browser,

**8:40** · spin it around, see if it works, see if

**8:41** · it's rendering properly, and then it

**8:43** · kept iterating until we finally got this

**8:44** · version. And as you can see still, like

**8:46** · it's not perfect. There's some things we

**8:47** · want to change. I think it was supposed

**8:48** · to be see-through like this so we could

**8:49** · like actually go look inside. But this

**8:52** · is so much better than it would have

**8:54** · been if I didn't give it that slash goal

**8:55** · with the criteria, and I just said build

**8:57** · me a 3D plane with, you know, 3.js. So

**9:00** · that's one of the key takeaways here.

**9:02** · Agent loops and goals are not supposed

**9:03** · to give you 100% perfect output. They're

**9:05** · supposed to help you get much closer on

**9:07** · the first try. And here's another great

**9:08** · example of that with the whole

**9:10** · subjectivity thing. Here's the last one

**9:12** · I did, which is a a prompt that I had

**9:13** · Claude Code make, a slash goal. It was

**9:15** · looking at this famous picture of the

**9:17** · Beatles Abbey Road. And then what I told

**9:19** · it to do was recreate this without using

**9:21** · image generation. So just recreating

**9:23** · this using like HTML or CSS or whatever

**9:25** · it wants to do. And then it goes through

**9:27** · and it creates, you know, version one,

**9:28** · version two, version three. And it ended

**9:30** · up stopping after version seven. You can

**9:32** · see the prompt here says, "If the

**9:33** · average is above nine or equal to nine,

**9:36** · then stop." And that's when you end. The

**9:38** · other thing it said is hard cap on eight

**9:39** · passes. So, it was getting near that cap

**9:41** · either way. But, these images are not

**9:43** · very good. What we can see though is

**9:45** · that it did its verification. So, each

**9:46** · time it went through and created the

**9:48** · HTML, it had to actually put it in a

**9:49** · browser and then it would take a

**9:51** · screenshot of it. You can see here's the

**9:52** · screenshot for number one, here's

**9:54** · version two, here's version three,

**9:55** · here's version four. So, we can see it

**9:57** · in real time getting better and better

**9:59** · with each version, with each iteration.

**10:01** · But still, this is the one that it gave

**10:02** · me at the end and obviously that looks

**10:03** · nothing like the picture. We've got the

**10:05** · car here, we've got the trees, we've got

**10:06** · the road, we've got yellow, black, gray,

**10:09** · light blue, just like the actual image.

**10:11** · If I go back here, did I say yellow? I

**10:13** · meant to say white. White, black, dark

**10:15** · gray, light blue. And so, obviously it's

**10:17** · nothing like it. If we would have done

**10:18** · this with image generation, it could

**10:20** · have been probably much closer. But I

**10:22** · just wanted to try how that would work

**10:23** · with pure code. The point being, it had

**10:26** · the verification checks, it had the

**10:27** · ability to take screenshots and look

**10:29** · through each of its iterations,

**10:31** · understand how did this still not look

**10:33** · like the reference image, and what

**10:35** · changes do we need to make each time?

**10:37** · And so, that's why a loop is only going

**10:38** · to be as good as it's done check, as the

**10:41** · done criteria. So, there's two things

**10:42** · you need to think about before you build

**10:44** · your first loop or your goals. What does

**10:46** · done mean? And then how will it check?

**10:48** · Because let's say you're building an

**10:49** · actual game, a game that you can open up

**10:51** · on your PC and play. It would have to

**10:53** · check that in many ways. It would have

**10:55** · to check visually, it would have to

**10:56** · check functionally, and it would have to

**10:58** · play the levels and see if anything

**10:59** · breaks. If you're writing some sort of

**11:01** · like script, how does it check? It

**11:03** · doesn't need to check visually, it just

**11:04** · needs to check flow. It needs to check

**11:06** · that it sounds like your tone of voice.

**11:07** · It needs to check in other ways. So,

**11:09** · based on what you're building, the

**11:10** · verification checks obviously look

**11:12** · different and it's your job to make sure

**11:13** · that your agents have the right tools in

**11:15** · order to do those checks. And then of

**11:17** · course, on the other side, what does

**11:18** · done mean? Like I mentioned earlier, if

**11:20** · you can get as objective as possible

**11:22** · with a specific metric, then that's

**11:23** · best. But sometimes you can't. Sometimes

**11:25** · you have to say until you're 100%

**11:27** · confident, right? And so like, my most

**11:29** · common use of these loops is when I use

**11:31** · hyper frames in Cloud Code to edit

**11:32** · videos because I will basically chuck it

**11:34** · in, do a slash goal, and it does

**11:36** · everything for me. It has to get the

**11:37** · transcript, cut out the mistakes and the

**11:39** · pauses, it has to make the beats, it has

**11:41** · to sync the beats, it has to obviously

**11:43** · render them, and then it has a ton of

**11:44** · verification on making sure that all of

**11:46** · the beats are in bounds and that they

**11:47** · line up with the transcript correctly.

**11:49** · And that is how you're able to see a lot

**11:50** · of these people say, "Okay, I did this

**11:52** · with one shot, with one prompt." Because

**11:54** · it was a loop, because it had

**11:55** · verification and iteration. So, what

**11:57** · makes a loop actually work? A checkable

**11:59** · goal, a hard stop, good tools, memory, a

**12:03** · separate checker, planning first,

**12:06** · logging, and then making it make sense

**12:08** · with the cost. Because a lot of times

**12:10** · these loops can run for a long time, and

**12:13** · especially if you have a pretty hard

**12:15** · goal, a goal that might take a lot of

**12:16** · iteration, and then if the done criteria

**12:19** · is also very hard, where maybe it just

**12:21** · can't actually ever hit that, then that

**12:23** · thing's going to run for a long time.

**12:24** · So, I've had a couple loops that have

**12:25** · gone for 12 hours plus, and they're just

**12:27** · not like super useful to me. Most of the

**12:29** · time when I'm running loops that run for

**12:31** · a while, it's usually more like these.

**12:32** · It's usually things that take like 35

**12:35** · minutes or maybe a couple hours, but I

**12:37** · don't need a loop that's going to run

**12:38** · for 4 days straight. I just don't really

**12:40** · need that. So, another kind of message

**12:42** · that I'm trying to send here is just

**12:43** · because you're seeing someone like Peter

**12:45** · Steinberger saying something like this,

**12:47** · doesn't actually mean that this applies

**12:48** · directly to you and your use case.

**12:50** · Because he's a hardcore coder, he's

**12:52** · building agents, he works at OpenAI.

**12:55** · This probably makes a lot of sense for

**12:56** · the way that he works and has probably

**12:58** · 10xed his productivity. And that's the

**12:59** · cool thing about AI is that it because

**13:01** · it's going to seep into every single

**13:02** · vertical and every single role, not

**13:04** · everyone will use it the same. So, it's

**13:05** · good to stay up to date with what people

**13:07** · like Peter Steinberger are saying, but

**13:09** · that doesn't mean you have to drop

**13:10** · everything right now and go try it. Or

**13:12** · maybe it's good to try it, but that

**13:13** · doesn't mean you have to fully integrate

**13:14** · it into every single Cloud Code session

**13:17** · forever.

**13:18** · So, anyways, coming from a non-coding

**13:21** · background, coming from a perspective of

**13:23** · someone who uses Cloud Code all all

**13:25** · time, 24/7, but I use it for knowledge

**13:27** · work rather than massive database code

**13:30** · base refactors and building software and

**13:33** · building apps every day. That's kind of

**13:34** · the way that I feel about these agent

**13:36** · loops, and I've been seeing a ton of

**13:37** · stuff about them lately, so I felt like

**13:38** · I needed to come in here and just share

**13:40** · my opinions on it. Some of you guys may

**13:42** · disagree with this, but that's the way

**13:43** · that I've been using them because I do

**13:44** · use them. I just don't go for those

**13:46** · fancy runs that run for like 3 days

**13:47** · straight. A lot of times if I have a big

**13:49** · goal, I will shoot off a nice chunky

**13:51** · loop before I go to bed, and I can wake

**13:53** · up with something that's ran for maybe 4

**13:54** · or maybe 8 hours, and that is truly very

**13:56** · beneficial. But a lot of that stuff is

**13:58** · more experimental for me, and then I'm

**13:59** · able to take that output I got from the

**14:01** · overnight run, and then chuck it back

**14:03** · into some more loops or iterate on that

**14:04** · myself as a human. So, there's a little

**14:06** · bit more detail that was covered in this

**14:07** · slide deck as well as this full audit,

**14:09** · which is way more wordy and super ugly

**14:11** · to look at, but I will attach both of

**14:13** · these sources in my free school

**14:14** · community if you guys want to check all

**14:16** · that out. The link for that is down in

**14:17** · the description. You'll hop in the free

**14:18** · school community, you'll go to

**14:19** · classroom, you'll click on all YouTube

**14:21** · resources, and you can find everything

**14:23** · in there. But, that's going to do it for

**14:24** · today. So, if you guys enjoyed the video

**14:25** · or you learned something new, please

**14:27** · give it a like. Helps me out a ton. And

**14:28** · as always, I appreciate you guys making

**14:29** · it to the end of the video, and I'll see

**14:31** · you on the next one.

**14:32** · Thanks, guys.
