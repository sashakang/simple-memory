---
title: "How to Build a Company OS in Claude Code | Jiaona Zhang | Product Growth"
source: "https://www.youtube.com/watch?v=qsDX0PMKcaE"
author:
  - "[[Aakash Gupta]]"
published: 2026-06-24
created: 2026-06-29
description: "Jiaona Zhang screenshares Laurel's GitHub-based Company OS, playbook-to-skill pipeline, Slack automations, AI Ops team model, and four AI-maturity levels."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=qsDX0PMKcaE)

Jiaona Zhang (JZ) is the CPO at Laurel, an AI timesheet platform. She has led product at Airbnb, Dropbox, Webflow, and WeWork. Today she runs a product team that ships front-end and back-end features end-to-end. In this episode, she screenshares Laurel's full Company OS live, walks through the agent pipeline, shows how non-technical team members ship to production using AI, and breaks down the 4 levels of AI maturity she uses to assess every candidate she interviews.

Full Writeup: https://www.news.aakashg.com/p/how-to-build-an-ai-native-team
Transcript: https://www.aakashg.com/how-to-build-ai-native-team/
Laurel: https://www.laurel.ai/

---

Timestamps:
0:00 - Intro
1:46 - Episode begins
2:04 - The Company OS: GitHub structure screenshare
5:40 - The 1% vs 99% problem
9:00 - 3 steps to build your own Company OS
10:05 - Ads
12:30 - Slack automation demo: feature request triage
14:31 - Playbook to agent pipeline
22:51 - Company culture and the companywide hackathon
29:02 - PMs shipping front-end and back-end features
29:44 - The captain model explained
30:34 - Ads
32:37 - Continuation to captain model
37:38 - Two-track product reviews
50:08 - The AI Ops team and the Sasha model
57:59 - The screen-share interview
59:01 - The 4 levels of AI maturity
1:06:08 - Outro

## Transcript

**0:00** · You got these people who are these 1% AI users. They're highly AI pilled. And

**0:04** · users. They're highly AI pilled. And then you have the 90 to 99% of the rest

**0:06** · then you have the 90 to 99% of the rest of the organization who isn't sure what

**0:08** · of the organization who isn't sure what to use when.

**0:09** · to use when. >> Meet Jay-Z. She's the chief product

**0:11** · >> Meet Jay-Z. She's the chief product officer at Luro, the $100

**0:14** · officer at Luro, the $100 AI time platform. She teaches PM at

**0:16** · AI time platform. She teaches PM at Stanford. Before Jay-Z, she was the CPO

**0:18** · Stanford. Before Jay-Z, she was the CPO at Linktree, and she's led product at

**0:21** · at Linktree, and she's led product at Airbnb, Webflow, Dropbox, and WeWork.

**0:24** · Airbnb, Webflow, Dropbox, and WeWork. >> something pretty crazy in your

**0:26** · >> something pretty crazy in your interviews. Can you tell me how you

**0:27** · interviews. Can you tell me how you interview people and really find these

**0:30** · interview people and really find these damn AI pale super IC PM?

**0:32** · damn AI pale super IC PM? >> The fundamentals and the principles have

**0:34** · >> The fundamentals and the principles have never changed. In fact, they're even

**0:37** · never changed. In fact, they're even more important than ever before, but the

**0:38** · more important than ever before, but the tools and the way you operate, that's

**0:41** · tools and the way you operate, that's radically changed.

**0:42** · radically changed. >> How should people be thinking about in

**0:44** · >> How should people be thinking about in an AI native organization? This is the

**0:46** · an AI native organization? This is the role of a PM.

**0:47** · role of a PM. >> And so those are the four levels. Level

**0:49** · >> And so those are the four levels. Level one is you're talking to ChatGPT, you're

**0:50** · one is you're talking to ChatGPT, you're talking to Claude. You're really using

**0:52** · talking to Claude. You're really using AI kind of in chat mode. Level two is

**0:54** · AI kind of in chat mode. Level two is where you start to automate a workflow.

**0:55** · where you start to automate a workflow. Level three is when you start building,

**0:57** · Level three is when you start building, you know, apps. And then level four I'd

**0:59** · you know, apps. And then level four I'd say is where you're actually building I

**1:00** · say is where you're actually building I call them shared apps.

**1:02** · call them shared apps. >> How does someone start from step one?

**1:04** · >> How does someone start from step one? What is the process somebody needs to go

**1:06** · What is the process somebody needs to go through in order to build up and create

**1:08** · through in order to build up and create their own company operating system?

**1:15** · Before we go any further, do me a favor and check that you are subscribed on

**1:18** · and check that you are subscribed on YouTube and following on Apple and

**1:19** · YouTube and following on Apple and Spotify podcasts. And if you want to get

**1:22** · Spotify podcasts. And if you want to get access to amazing AI tools, check out my

**1:25** · access to amazing AI tools, check out my bundle.

**1:26** · bundle. Where if you become an annual subscriber

**1:28** · Where if you become an annual subscriber to my newsletter, you get a full year

**1:30** · to my newsletter, you get a full year free of the paid plans of Maven, Arise,

**1:33** · free of the paid plans of Maven, Arise, Relay App, Dovetail, Linear, Magic

**1:35** · Relay App, Dovetail, Linear, Magic Patterns, Deep Sky, Reforge, Build,

**1:36** · Patterns, Deep Sky, Reforge, Build, Descript, and Speechify. So be sure to

**1:38** · Descript, and Speechify. So be sure to check that out at bundle.akashg.com, and

**1:41** · check that out at bundle.akashg.com, and now into today's episode.

**1:46** · Jay-Z, I've been teaching people a lot about how to use Claude code with

**1:50** · about how to use Claude code with personal operating systems, with team

**1:52** · personal operating systems, with team operating systems. You guys at Luro have

**1:55** · operating systems. You guys at Luro have taken it to a level I have not seen

**1:57** · taken it to a level I have not seen before. You guys have built out a

**1:59** · before. You guys have built out a company operating system.

**2:01** · company operating system. Can you show me what this is and what it

**2:04** · Can you show me what this is and what it does?

**2:04** · does? >> Of course. All right, let me screen

**2:06** · >> Of course. All right, let me screen share here. Okay, let's start here.

**2:08** · share here. Okay, let's start here. Let's go to GitHub, our favorite place.

**2:10** · Let's go to GitHub, our favorite place. And so you'll see here that we have in

**2:13** · And so you'll see here that we have in GitHub a company-wide operating system

**2:16** · GitHub a company-wide operating system where for every single function in a

**2:18** · where for every single function in a company, customer success, data science,

**2:21** · company, customer success, data science, design, engineering, finance, imitation,

**2:24** · design, engineering, finance, imitation, legal, marketing, we have um

**2:27** · legal, marketing, we have um essentially all these folders that share

**2:30** · essentially all these folders that share how do you think about each phase of

**2:33** · how do you think about each phase of work that that function does. So in

**2:35** · work that that function does. So in customer success, you do account

**2:37** · customer success, you do account management. And within account

**2:38** · management. And within account management, you're thinking about, you

**2:40** · management, you're thinking about, you know, renewals, upsells. Um you do a

**2:43** · know, renewals, upsells. Um you do a customer enablement. And within that, we

**2:45** · customer enablement. And within that, we essentially work with our customers, we

**2:47** · essentially work with our customers, we do office hours. We help them with roll

**2:49** · do office hours. We help them with roll out. We do training and onboarding.

**2:52** · out. We do training and onboarding. Each of these folders have a skill. And

**2:55** · Each of these folders have a skill. And I think uh for those of you who are less

**2:57** · I think uh for those of you who are less familiar with GitHub, we'll actually hop

**2:59** · familiar with GitHub, we'll actually hop over here to something that is very

**3:01** · over here to something that is very familiar, which is essentially your file

**3:03** · familiar, which is essentially your file structure, your folder structure. And so

**3:05** · structure, your folder structure. And so going to customer success, you can see

**3:07** · going to customer success, you can see that each of these folders have a series

**3:11** · that each of these folders have a series of um you know, folders that are the are

**3:14** · of um you know, folders that are the are the activities that they do. And then

**3:16** · the activities that they do. And then within each of them, they have skills.

**3:18** · within each of them, they have skills. So how do you actually think about

**3:20** · So how do you actually think about creating the right assets for the

**3:22** · creating the right assets for the negotiation support or the right

**3:23** · negotiation support or the right references? I'll go back one more. Um

**3:25** · references? I'll go back one more. Um for renewals, right? Um what is the

**3:28** · for renewals, right? Um what is the skill file there to really think about

**3:30** · skill file there to really think about how do you walk through a renewal

**3:32** · how do you walk through a renewal correctly with a customer?

**3:34** · correctly with a customer? And now you're like, okay, cool, you

**3:36** · And now you're like, okay, cool, you have some folders in GitHub, you have,

**3:38** · have some folders in GitHub, you have, you know, some some stuff that you can

**3:40** · you know, some some stuff that you can download. How does this all come to

**3:42** · download. How does this all come to drive

**3:43** · drive like real change? And the way I'll talk

**3:46** · like real change? And the way I'll talk about this is, you know, at the end of

**3:47** · about this is, you know, at the end of the day, we all live in some form of

**3:51** · the day, we all live in some form of email or Slack. And so what I'll do

**3:53** · email or Slack. And so what I'll do really quickly is I'll open up my Slack.

**3:55** · really quickly is I'll open up my Slack. And again, this is not real data in the

**3:57** · And again, this is not real data in the sense that we do have very sensitive

**3:59** · sense that we do have very sensitive data that I'm not going to be be

**4:00** · data that I'm not going to be be sharing. So, this is a little bit more

**4:02** · sharing. So, this is a little bit more mock, but it shows you exactly how our

**4:04** · mock, but it shows you exactly how our how our team operates. So, for example,

**4:07** · how our team operates. So, for example, every single morning

**4:08** · every single morning every person on a lot of these

**4:10** · every person on a lot of these customer-facing teams, right? They're

**4:12** · customer-facing teams, right? They're highly repeatable motions, the more we

**4:15** · highly repeatable motions, the more we can sing from one voice and say the same

**4:18** · can sing from one voice and say the same thing the way we can create consistency

**4:21** · thing the way we can create consistency in the awesomeness of the customer

**4:24** · in the awesomeness of the customer experience, that makes your company, you

**4:27** · experience, that makes your company, you know, much more unified and

**4:30** · know, much more unified and it's a big part of the brand. And so,

**4:31** · it's a big part of the brand. And so, when you think about that and you think

**4:33** · when you think about that and you think about a customer success person waking

**4:35** · about a customer success person waking up in their day

**4:36** · up in their day and really seeing, let me go here. This

**4:38** · and really seeing, let me go here. This is a example for customer success.

**4:40** · is a example for customer success. Here's your calendar. Here are all the

**4:42** · Here's your calendar. Here are all the meetings that you have, the check-ins

**4:44** · meetings that you have, the check-ins that you have, you know, the onboarding

**4:46** · that you have, you know, the onboarding sessions you have.

**4:47** · sessions you have. This is something that a lot of people

**4:49** · This is something that a lot of people are building. This is a example of a

**4:50** · are building. This is a example of a chief of staff light concept, but what

**4:53** · chief of staff light concept, but what we're now doing is we're integrating all

**4:55** · we're now doing is we're integrating all the skills. So, for example, when we do

**4:57** · the skills. So, for example, when we do a handoff, when we do a session prep,

**5:00** · a handoff, when we do a session prep, all of these are actual skills. And what

**5:02** · all of these are actual skills. And what happens is then when anyone is using

**5:05** · happens is then when anyone is using Claude, for example, I'll just go into

**5:08** · Claude, for example, I'll just go into I'll go I'll go really quickly into the

**5:10** · I'll go I'll go really quickly into the organization settings and I go into your

**5:12** · organization settings and I go into your skills. You can start to see that you

**5:14** · skills. You can start to see that you can upload all of these skills into your

**5:17** · can upload all of these skills into your company context. And as a result, when

**5:19** · company context. And as a result, when you're going through your day, you can

**5:21** · you're going through your day, you can essentially say, "Great. I'm going

**5:23** · essentially say, "Great. I'm going through my day. I'm doing all these

**5:24** · through my day. I'm doing all these things.

**5:25** · things. My

**5:27** · My I will use these skills so that I no

**5:29** · I will use these skills so that I no longer have to spend all the time

**5:31** · longer have to spend all the time creating that one deck or spend all that

**5:33** · creating that one deck or spend all that time creating an email. It is actually

**5:35** · time creating an email. It is actually something You know exactly what skill to

**5:37** · something You know exactly what skill to use when. And I think that's the biggest

**5:39** · use when. And I think that's the biggest thing that companies struggle with,

**5:41** · thing that companies struggle with, which is you got these people who are

**5:42** · which is you got these people who are these 1% AI users. They're tinkering

**5:45** · these 1% AI users. They're tinkering with their workflows. They're highly AI

**5:47** · with their workflows. They're highly AI piled, and then you have the, you know,

**5:49** · piled, and then you have the, you know, 90 to 99% of the rest of the

**5:51** · 90 to 99% of the rest of the organization who isn't sure what to use

**5:54** · organization who isn't sure what to use when. And so, as a result, you can

**5:55** · when. And so, as a result, you can actually integrate your skills, again,

**5:58** · actually integrate your skills, again, at a company level. So, across every

**6:00** · at a company level. So, across every single one of these functions, going

**6:02** · single one of these functions, going back to files, each one of these

**6:04** · back to files, each one of these functions and all the activity that they

**6:05** · functions and all the activity that they do in order to be able to understand

**6:08** · do in order to be able to understand what, um, skill should I should I be

**6:10** · what, um, skill should I should I be using when, and where should I be

**6:11** · using when, and where should I be spending my time? Maybe the last thing

**6:13** · spending my time? Maybe the last thing I'll just show to kind of, uh, to really

**6:15** · I'll just show to kind of, uh, to really bring this to life is every single

**6:17** · bring this to life is every single company, you can map every single

**6:19** · company, you can map every single function's work to what I call an

**6:21** · function's work to what I call an ontology. So, in sales, you know, all of

**6:24** · ontology. So, in sales, you know, all of the work in sales maps to these

**6:26** · the work in sales maps to these categories that they're supposed to be

**6:27** · categories that they're supposed to be doing. And within each category, there

**6:30** · doing. And within each category, there are series of tasks that happen. And

**6:32** · are series of tasks that happen. And this is actually what has informed the

**6:34** · this is actually what has informed the ontology that I just showed you. We've

**6:35** · ontology that I just showed you. We've done the really hard work of mapping

**6:37** · done the really hard work of mapping out, okay, for every single function,

**6:39** · out, okay, for every single function, again, I'll scroll through this.

**6:41** · again, I'll scroll through this. Marketing, sales, customer success,

**6:43** · Marketing, sales, customer success, implementation, design, engineering, so

**6:44** · implementation, design, engineering, so on and so forth. These are the things

**6:46** · on and so forth. These are the things that we believe that each function

**6:47** · that we believe that each function should be doing. How do we actually

**6:49** · should be doing. How do we actually create, um, a set of skills to for for

**6:53** · create, um, a set of skills to for for you to, um,

**6:54** · you to, um, do the things that we want you to be

**6:55** · do the things that we want you to be doing more, and to also automate the

**6:58** · doing more, and to also automate the things that we don't want you to be

**6:59** · things that we don't want you to be doing anymore. So, I'll go to product,

**7:01** · doing anymore. So, I'll go to product, which is, you know, a lot of the

**7:02** · which is, you know, a lot of the audience here today. In product, what's

**7:04** · audience here today. In product, what's really interesting is that,

**7:06** · really interesting is that, you know, you should be spending your

**7:08** · you know, you should be spending your time like an engineer in many ways. And

**7:10** · time like an engineer in many ways. And we talk about this later where, you

**7:11** · we talk about this later where, you know, the ontology or the work map of a

**7:13** · know, the ontology or the work map of a product manager is starting to look look

**7:15** · product manager is starting to look look a lot more like an engineer. But there

**7:17** · a lot more like an engineer. But there are a lot of things that used to be in

**7:19** · are a lot of things that used to be in the, um, day-to-day of a product

**7:21** · the, um, day-to-day of a product manager, doing competitive market

**7:22** · manager, doing competitive market analysis, doing these all these like,

**7:25** · analysis, doing these all these like, writing for stakeholder management, or,

**7:28** · writing for stakeholder management, or, um, really mundane, tedious

**7:30** · um, really mundane, tedious organization, um, getting people on a

**7:32** · organization, um, getting people on a phone, synthesizing, um, feedback, etc.

**7:35** · phone, synthesizing, um, feedback, etc. All of these things, as we all know, are

**7:37** · All of these things, as we all know, are starting to get automated. But again,

**7:39** · starting to get automated. But again, it's automated in a really lumpy way,

**7:41** · it's automated in a really lumpy way, where one PM might be doing a really,

**7:43** · where one PM might be doing a really, really well and other p.m. I might not

**7:44** · really well and other p.m. I might not be doing it as well. So, what we can do

**7:46** · be doing it as well. So, what we can do here is when you onboard everyone with a

**7:48** · here is when you onboard everyone with a company OS, again going back to this

**7:51** · company OS, again going back to this GitHub,

**7:52** · GitHub, and going to, let's say, product, right?

**7:55** · and going to, let's say, product, right? Um

**7:56** · Um you can start to say, "Hey, these are

**7:57** · you can start to say, "Hey, these are all the playbooks, all the skills that I

**8:00** · all the playbooks, all the skills that I want to give every single person on my

**8:02** · want to give every single person on my team." And then, when they come in for

**8:04** · team." And then, when they come in for their daily briefing, what ends up

**8:06** · their daily briefing, what ends up happening is that they are able to see

**8:09** · happening is that they are able to see their day at a glance, and we

**8:10** · their day at a glance, and we essentially tell you where you can

**8:12** · essentially tell you where you can automate your day. So, you take the

**8:13** · automate your day. So, you take the thing that is a that is essentially

**8:15** · thing that is a that is essentially designed by the 1% of of every any given

**8:18** · designed by the 1% of of every any given function, the person who is playing

**8:19** · function, the person who is playing around the most, and are able to spread

**8:21** · around the most, and are able to spread those learnings throughout the entire

**8:23** · those learnings throughout the entire rest of the organization.

**8:25** · rest of the organization. >> Wow. I think this is so powerful because

**8:27** · >> Wow. I think this is so powerful because we all have been working in different

**8:28** · we all have been working in different teams where there's that one person

**8:31** · teams where there's that one person who's got their skills locked, but if

**8:34** · who's got their skills locked, but if they're just compounding in a bucket,

**8:35** · they're just compounding in a bucket, then nobody can really benefit. This

**8:37** · then nobody can really benefit. This company OS, this is bringing that power

**8:40** · company OS, this is bringing that power to everybody.

**8:42** · to everybody. Now, you guys are an AI-native company.

**8:45** · Now, you guys are an AI-native company. You guys are an AI company yourselves,

**8:47** · You guys are an AI company yourselves, and so you guys would have certain

**8:49** · and so you guys would have certain advantages

**8:50** · advantages in building this. How does someone start

**8:53** · in building this. How does someone start from step one? What is the process

**8:55** · from step one? What is the process somebody needs to go through in order to

**8:57** · somebody needs to go through in order to build up and create their own company

**8:59** · build up and create their own company operating system?

**9:00** · operating system? >> I like to think about it as three

**9:02** · >> I like to think about it as three different steps. And so, let me screen

**9:03** · different steps. And so, let me screen share again, and I will um share how do

**9:06** · share again, and I will um share how do I think about essentially um getting

**9:08** · I think about essentially um getting your steps in, going from most simple to

**9:11** · your steps in, going from most simple to most advanced. So, the first way to

**9:13** · most advanced. So, the first way to think about this is, how do you just

**9:14** · think about this is, how do you just start small? What is one workflow that

**9:17** · start small? What is one workflow that you or your team does that is incredibly

**9:20** · you or your team does that is incredibly tedious that you shouldn't be doing

**9:22** · tedious that you shouldn't be doing again? So, typically, for many, many

**9:24** · again? So, typically, for many, many functions, it is, you know, I write this

**9:26** · functions, it is, you know, I write this email, and I want this email to have a

**9:28** · email, and I want this email to have a template that is automatically, you

**9:30** · template that is automatically, you know, um kicked off for me when um XYZ

**9:33** · know, um kicked off for me when um XYZ things happen, or there's a sequence of

**9:35** · things happen, or there's a sequence of things that happen. I don't want to

**9:36** · things that happen. I don't want to input um my data into our CRM anymore. I

**9:39** · input um my data into our CRM anymore. I want that to be automated. So, there's

**9:41** · want that to be automated. So, there's some degree of thinking about what is

**9:43** · some degree of thinking about what is super mundane, takes a lot of time out

**9:45** · super mundane, takes a lot of time out of your day-to-day, and if that were to

**9:48** · of your day-to-day, and if that were to be automated away, you'd be thrilled

**9:49** · be automated away, you'd be thrilled about. And I'll give you one very

**9:52** · about. And I'll give you one very product-oriented example, which is there

**9:55** · product-oriented example, which is there are so many companies out there, so many

**9:57** · are so many companies out there, so many PMs out there that spend a lot of their

**9:59** · PMs out there that spend a lot of their days responding to questions,

**10:01** · days responding to questions, escalations. So, the sales team comes

**10:04** · escalations. So, the sales team comes into a channel

**10:05** · into a channel >> I'm notoriously bad at my inboxes. I

**10:07** · >> I'm notoriously bad at my inboxes. I guess there's a version of that where I

**10:09** · guess there's a version of that where I seem cool and unavailable, but the

**10:11** · seem cool and unavailable, but the reality is I miss sponsor emails, guest

**10:12** · reality is I miss sponsor emails, guest pitches, and stuff that my team actually

**10:14** · pitches, and stuff that my team actually needs me [music] for. So, I got an AI

**10:16** · needs me [music] for. So, I got an AI assistant, the sponsor of today's

**10:18** · assistant, the sponsor of today's episode, Arise.

**10:20** · episode, Arise. Arise connects to my email, calendar,

**10:22** · Arise connects to my email, calendar, and [music] Slack. Then I just chat with

**10:23** · and [music] Slack. Then I just chat with it over Slack, and it helps me with

**10:25** · it over Slack, and it helps me with everything. It builds workflows to

**10:27** · everything. It builds workflows to respond to emails, resolve [music]

**10:29** · respond to emails, resolve [music] customer issues, prep me for meetings.

**10:31** · customer issues, prep me for meetings. It actually comes to my meetings,

**10:33** · It actually comes to my meetings, >> [music]

**10:33** · >> [music] >> updates its own notes, and remembers

**10:35** · >> updates its own notes, and remembers context from past conversations. So,

**10:38** · context from past conversations. So, every time I talk to it, it already

**10:40** · every time I talk to it, it already knows what I'm working on.

**10:41** · knows what I'm working on. >> [music]

**10:41** · >> [music] >> I used to pay for Granola and Lindy

**10:43** · >> I used to pay for Granola and Lindy separately. Arise replaced both. One

**10:45** · separately. Arise replaced both. One tool does more, and it lives right in

**10:47** · tool does more, and it lives right in Slack where I already work. [music]

**10:48** · Slack where I already work. [music] Check it out at arise.ai/akash.

**10:51** · Check it out at arise.ai/akash. That's a r i s o dot a i slash a a k a s

**10:55** · That's a r i s o dot a i slash a a k a s h.

**10:55** · h. >> Here's the dirty secret about

**10:56** · >> Here's the dirty secret about prototyping. You spend two weeks

**10:58** · prototyping. You spend two weeks building a prototype, you validate your

**11:00** · building a prototype, you validate your assumptions, engineering loves the

**11:01** · assumptions, engineering loves the direction. Then what happens? You throw

**11:03** · direction. Then what happens? You throw the whole thing away. Bolt changes this

**11:05** · the whole thing away. Bolt changes this completely. When you prototype in Bolt,

**11:07** · completely. When you prototype in Bolt, you're not building throwaway mock-up.

**11:09** · you're not building throwaway mock-up. You're building real front-end code that

**11:11** · You're building real front-end code that integrates with your existing design

**11:13** · integrates with your existing design system. So, when you hand it to

**11:14** · system. So, when you hand it to engineering, they don't throw it away,

**11:16** · engineering, they don't throw it away, they ship on top of what you've built. I

**11:18** · they ship on top of what you've built. I use Bolt every single day. I host my

**11:20** · use Bolt every single day. I host my land PM job cohort on it, and honestly,

**11:23** · land PM job cohort on it, and honestly, I'm up till 2:00 a.m. some days just

**11:25** · I'm up till 2:00 a.m. some days just vibing in the tool, having fun, and

**11:27** · vibing in the tool, having fun, and building. That's when you know a product

**11:28** · building. That's when you know a product is good. When you're using it past

**11:30** · is good. When you're using it past midnight not because you need to, but

**11:31** · midnight not because you need to, but because you want to. Check out bold at

**11:33** · because you want to. Check out bold at bold.new/akash.

**11:35** · bold.new/akash. That's b o l d . n e w / a a k a s h.

**11:40** · That's b o l d . n e w / a a k a s h. Link in the show notes. Today's podcast

**11:42** · Link in the show notes. Today's podcast is brought to you by Pendo, the leading

**11:43** · is brought to you by Pendo, the leading software experience management platform.

**11:45** · software experience management platform. McKinsey found that 78% of companies are

**11:48** · McKinsey found that 78% of companies are using gen AI, but just as many have

**11:50** · using gen AI, but just as many have reported no bottom line improvements.

**11:52** · reported no bottom line improvements. So, how do you know if your AI agents

**11:54** · So, how do you know if your AI agents are actually working? Are they giving

**11:56** · are actually working? Are they giving users the wrong answers, creating more

**11:58** · users the wrong answers, creating more work instead of less, improving

**11:59** · work instead of less, improving retention, or hurting it? When your

**12:01** · retention, or hurting it? When your software data and AI data are

**12:02** · software data and AI data are disconnected, you can't answer these

**12:03** · disconnected, you can't answer these questions. But, when you bring all your

**12:05** · questions. But, when you bring all your usage data together in one place, you

**12:08** · usage data together in one place, you can see what users do before, during,

**12:10** · can see what users do before, during, and after they use AI. Showing you an

**12:12** · and after they use AI. Showing you an agent's work, how they help you grow,

**12:14** · agent's work, how they help you grow, and when to prioritize on your road map.

**12:16** · and when to prioritize on your road map. Pendo agent analytics is the only

**12:18** · Pendo agent analytics is the only solution built to do this for product

**12:20** · solution built to do this for product teams. Start measuring your AI's

**12:21** · teams. Start measuring your AI's performance with agent analytics at

**12:23** · performance with agent analytics at pendo.io/akash.

**12:25** · pendo.io/akash. That's p e n d o . i o / a a k a s h.

**12:30** · That's p e n d o . i o / a a k a s h. >> Okay, so let's move into Slack and see

**12:32** · >> Okay, so let's move into Slack and see what this might look like. You know, a

**12:33** · what this might look like. You know, a lot of companies, if you just go into

**12:35** · lot of companies, if you just go into any ask product channel or any channel,

**12:37** · any ask product channel or any channel, you see so many um success folks, um

**12:41** · you see so many um success folks, um support folks, sales folks, um other

**12:43** · support folks, sales folks, um other teams hitting up that channel asking

**12:46** · teams hitting up that channel asking people, "Hey, I have a question. I have

**12:47** · people, "Hey, I have a question. I have a feature request." And so, the very

**12:49** · a feature request." And so, the very small workflow that we did, and I'll go

**12:50** · small workflow that we did, and I'll go all the way down, is we created a Slack

**12:53** · all the way down, is we created a Slack automation that essentially said, "Look,

**12:56** · automation that essentially said, "Look, when a feature request comes in, we

**12:58** · when a feature request comes in, we typically spend a bunch of time going

**12:59** · typically spend a bunch of time going back and forth asking about how many

**13:01** · back and forth asking about how many times was this asked about, send me the

**13:04** · times was this asked about, send me the gong recording where I could watch what

**13:06** · gong recording where I could watch what the customer's actually saying, um what

**13:08** · the customer's actually saying, um what is the impact of this for your customer,

**13:10** · is the impact of this for your customer, which requires some degree of judgment

**13:11** · which requires some degree of judgment from the person managing the account, um

**13:13** · from the person managing the account, um what is actually going on here, give me

**13:15** · what is actually going on here, give me some more details." All of those things

**13:17** · some more details." All of those things usually require back and forth. So,

**13:19** · usually require back and forth. So, again, if I go back to this this system

**13:21** · again, if I go back to this this system of how do you think about a place to

**13:23** · of how do you think about a place to start? What is something that you do

**13:24** · start? What is something that you do over and over again that you could

**13:26** · over and over again that you could really easily automate. And that

**13:28** · really easily automate. And that automation for us was as simple as,

**13:31** · automation for us was as simple as, "Hey, let's just automate what we ask

**13:33** · "Hey, let's just automate what we ask someone to fill in. And then what often

**13:36** · someone to fill in. And then what often happens is you then have to triage it.

**13:37** · happens is you then have to triage it. You say, 'Hey, you know, is it for this

**13:40** · You say, 'Hey, you know, is it for this team or that team? Is it for this PM or

**13:42** · team or that team? Is it for this PM or that PM? And what's the SLA to getting

**13:44** · that PM? And what's the SLA to getting back to the requester on what we're

**13:47** · back to the requester on what we're doing about this feature request?'" And

**13:50** · doing about this feature request?'" And so all of that you can build into

**13:51** · so all of that you can build into something as simple as Slack. So again,

**13:53** · something as simple as Slack. So again, a lot of people have Slack, Teams,

**13:55** · a lot of people have Slack, Teams, whatever it is you're using to chat with

**13:56** · whatever it is you're using to chat with your teams. You can do something very

**13:58** · your teams. You can do something very simple where you essentially say,

**14:00** · simple where you essentially say, "Okay, great. I come in here. I'm going

**14:02** · "Okay, great. I come in here. I'm going to automatically ask for all of this

**14:05** · to automatically ask for all of this information. So, you know, what is it?

**14:07** · information. So, you know, what is it? Who is it coming from? What's going on

**14:09** · Who is it coming from? What's going on here?" It automatically assigns it to

**14:12** · here?" It automatically assigns it to the person that makes the most sense to

**14:15** · the person that makes the most sense to go look at this. And then it

**14:16** · go look at this. And then it automatically creates some kind of

**14:17** · automatically creates some kind of ticket so that we can track it. And so

**14:20** · ticket so that we can track it. And so all of that, again, this is 101, I would

**14:21** · all of that, again, this is 101, I would say, right? It's just like a very small

**14:23** · say, right? It's just like a very small step in in creating your operating

**14:25** · step in in creating your operating system. So, I start there.

**14:26** · system. So, I start there. The next step is this idea of how do you

**14:29** · The next step is this idea of how do you start to really automate based on a

**14:32** · start to really automate based on a bunch of things that your team is doing.

**14:35** · bunch of things that your team is doing. And so the example here I have is, you

**14:37** · And so the example here I have is, you know, again, a team that usually has a

**14:39** · know, again, a team that usually has a lot of people, a lot of humans.

**14:41** · lot of people, a lot of humans. At Laurel, we have a large, you know,

**14:44** · At Laurel, we have a large, you know, GTM team. And within GTM, go-to-market,

**14:47** · GTM team. And within GTM, go-to-market, we have really awesome success folks

**14:50** · we have really awesome success folks who are essentially, you know, what I

**14:51** · who are essentially, you know, what I call like time consultants. They're

**14:53** · call like time consultants. They're getting kind of forward deployed into

**14:55** · getting kind of forward deployed into these organizations, helping them use

**14:57** · these organizations, helping them use Laurel as a as a product. And so what

**14:59** · Laurel as a as a product. And so what we've done is we've essentially created

**15:00** · we've done is we've essentially created a playbook. And again, this is very,

**15:02** · a playbook. And again, this is very, very long. I think anyone who's ever

**15:04** · very long. I think anyone who's ever created a playbook before, this is 50

**15:06** · created a playbook before, this is 50 pages. It covers everything from

**15:08** · pages. It covers everything from implementation to onboarding to user

**15:10** · implementation to onboarding to user onboarding. And and depending on who you

**15:12** · onboarding. And and depending on who you are, is it the admin, is it the actual

**15:14** · are, is it the admin, is it the actual timekeeper, etc. You know, different

**15:16** · timekeeper, etc. You know, different onboarding. These things, by the way,

**15:18** · onboarding. These things, by the way, are very fast now with Claude. You can

**15:20** · are very fast now with Claude. You can actually create this from a lot of

**15:21** · actually create this from a lot of sources and have it be written really

**15:23** · sources and have it be written really quickly. But what the struggle most

**15:25** · quickly. But what the struggle most companies has is now that I've created a

**15:27** · companies has is now that I've created a playbook,

**15:29** · playbook, how do I actually get people to do the

**15:30** · how do I actually get people to do the playbook? And how much of the playbook

**15:32** · playbook? And how much of the playbook is actually done by the human versus

**15:34** · is actually done by the human versus actually done by, you know, agents or

**15:37** · actually done by, you know, agents or workflow automations, right? And so this

**15:39** · workflow automations, right? And so this is where, again, going back to this

**15:40** · is where, again, going back to this concept of of the playbook um model,

**15:43** · concept of of the playbook um model, this is where you can say, "Okay, well,

**15:45** · this is where you can say, "Okay, well, I've created a playbook. I've went

**15:47** · I've created a playbook. I've went through and I've audited the things

**15:49** · through and I've audited the things that, again, it requires a human to do.

**15:51** · that, again, it requires a human to do. It requires a human to get on the phone

**15:52** · It requires a human to get on the phone with someone. It requires a human to go

**15:54** · with someone. It requires a human to go fly on site. Um but here are the things

**15:57** · fly on site. Um but here are the things that we think we can automate." This is

**15:58** · that we think we can automate." This is either um something we can productize or

**16:01** · either um something we can productize or this is something that we can create an

**16:02** · this is something that we can create an agent to do. And so that is, I would

**16:03** · agent to do. And so that is, I would say, the the next step that you graduate

**16:05** · say, the the next step that you graduate to, where you essentially create a

**16:06** · to, where you essentially create a playbook and then off of the playbook

**16:08** · playbook and then off of the playbook you decide on a set of skills. And And

**16:11** · you decide on a set of skills. And And that's, by the way, where we um

**16:13** · that's, by the way, where we um we started to to get the first version

**16:16** · we started to to get the first version of the OS I showed you earlier. When we

**16:18** · of the OS I showed you earlier. When we went into customer success and we said,

**16:19** · went into customer success and we said, "What are all the things that someone

**16:21** · "What are all the things that someone might be doing?" These large buckets. It

**16:23** · might be doing?" These large buckets. It was largely off of playbooks. The

**16:26** · was largely off of playbooks. The playbooks for implementation, the

**16:27** · playbooks for implementation, the playbooks for um activating a customer,

**16:30** · playbooks for um activating a customer, the playbooks for really um

**16:32** · the playbooks for really um talking to them the right way to make

**16:34** · talking to them the right way to make sure that they're set up for success.

**16:36** · sure that they're set up for success. And so that is really the the second way

**16:37** · And so that is really the the second way to think about it. And um maybe I'll

**16:39** · to think about it. And um maybe I'll share one thing here, which is there are

**16:41** · share one thing here, which is there are a lot of um agent builders out there

**16:43** · a lot of um agent builders out there today in the world. So you could use,

**16:44** · today in the world. So you could use, you know, Claude itself. They've

**16:46** · you know, Claude itself. They've launched, obviously, a lot of um agents.

**16:48** · launched, obviously, a lot of um agents. You can use um uh

**16:50** · You can use um uh a lot of things from Open AI as well.

**16:52** · a lot of things from Open AI as well. You can use a Glean. You can use a Dust.

**16:54** · You can use a Glean. You can use a Dust. We at Laurel use Dust. And so I'll take

**16:58** · We at Laurel use Dust. And so I'll take a moment to see if this loads.

**16:59** · a moment to see if this loads. >> So if somebody hasn't heard of Dust,

**17:01** · >> So if somebody hasn't heard of Dust, yeah, this is an agent building tool?

**17:03** · yeah, this is an agent building tool? >> This is an agent building tool. And what

**17:05** · >> This is an agent building tool. And what we find is often a lot of the um things

**17:08** · we find is often a lot of the um things that someone does can be turned into a

**17:11** · that someone does can be turned into a series of repeatable steps that gets

**17:13** · series of repeatable steps that gets automatically triggered. And so a great

**17:15** · automatically triggered. And so a great example, and I'll just go scroll down

**17:17** · example, and I'll just go scroll down here really quickly.

**17:19** · here really quickly. All of these are agents that we have

**17:21** · All of these are agents that we have built. So, going back to the

**17:23** · built. So, going back to the the playbook concept, if you say, "Hey,

**17:26** · the playbook concept, if you say, "Hey, I have a playbook of all the things that

**17:28** · I have a playbook of all the things that you need to be doing here." And again,

**17:30** · you need to be doing here." And again, 55 pages worth, I don't think anyone's

**17:32** · 55 pages worth, I don't think anyone's going to read anything here. What we can

**17:34** · going to read anything here. What we can start to do is go into an agent builder

**17:36** · start to do is go into an agent builder and say, "I'm going to create an agent

**17:37** · and say, "I'm going to create an agent for each of these steps." If I have to

**17:40** · for each of these steps." If I have to draft emails a lot as a customer success

**17:42** · draft emails a lot as a customer success manager, if I have to actually scrape

**17:44** · manager, if I have to actually scrape LinkedIn a lot as a salesperson, if I

**17:47** · LinkedIn a lot as a salesperson, if I have to look at the market as a

**17:48** · have to look at the market as a salesperson, or think about prospecting

**17:50** · salesperson, or think about prospecting questions, each of these can be you can

**17:52** · questions, each of these can be you can build an agent for each of the

**17:55** · build an agent for each of the um

**17:55** · um parts of the workflow here. And then

**17:57** · parts of the workflow here. And then going back to really thinking about how

**17:59** · going back to really thinking about how does everyone engage with your operating

**18:01** · does everyone engage with your operating system thoughtfully? No one's going to

**18:04** · system thoughtfully? No one's going to remember that they're going to call the

**18:05** · remember that they're going to call the specific agent that's going to do the

**18:07** · specific agent that's going to do the email, and the specific agent that's

**18:09** · email, and the specific agent that's going to do the RFP. The the big

**18:11** · going to do the RFP. The the big learning that we've had is how do you

**18:12** · learning that we've had is how do you create a wrap like a like a mega agent,

**18:15** · create a wrap like a like a mega agent, something like the like a

**18:17** · something like the like a a go-to-market agent that can be called

**18:19** · a go-to-market agent that can be called by the sales team at any point, by the

**18:22** · by the sales team at any point, by the success team at any point, and then that

**18:24** · success team at any point, and then that agent is able to route the ask, the the

**18:28** · agent is able to route the ask, the the need, or the help to whatever one of

**18:30** · need, or the help to whatever one of these sub-agents that is actually

**18:33** · these sub-agents that is actually useful.

**18:34** · useful. And then going back to like it really

**18:36** · And then going back to like it really the delivery piece is so important. Even

**18:38** · the delivery piece is so important. Even the friction of coming to something like

**18:41** · the friction of coming to something like a different interface, coming to a desk

**18:43** · a different interface, coming to a desk and asking it questions, is is really

**18:45** · and asking it questions, is is really low. In- instead, actually going into

**18:48** · low. In- instead, actually going into your um

**18:49** · your um your Slacks, your emails, and delivering

**18:51** · your Slacks, your emails, and delivering people um just-in-time

**18:54** · people um just-in-time playbooks and automations is really the

**18:56** · playbooks and automations is really the way to go to get to the point where

**18:58** · way to go to get to the point where you're you're actually getting people to

**18:59** · you're you're actually getting people to use the agents and the workflows that

**19:01** · use the agents and the workflows that you've built.

**19:01** · you've built. >> So, help me understand this part. Why

**19:04** · >> So, help me understand this part. Why use Dust instead of just all Claude or

**19:06** · use Dust instead of just all Claude or Claude code?

**19:07** · Claude code? >> Yeah, that's a great uh question. We

**19:09** · >> Yeah, that's a great uh question. We started using Dust back in fall of last

**19:12** · started using Dust back in fall of last year. And so I think there was just a

**19:13** · year. And so I think there was just a maturity of the tools. Um back then, it

**19:17** · maturity of the tools. Um back then, it was just much easier to use something

**19:19** · was just much easier to use something that specialize in agent building like a

**19:21** · that specialize in agent building like a Glean or a Dust. I do think today

**19:23** · Glean or a Dust. I do think today there's

**19:24** · there's um that gap is shrinking quite rapidly.

**19:27** · um that gap is shrinking quite rapidly. And so as a result, I don't think you

**19:28** · And so as a result, I don't think you need to go out there and buy a

**19:30** · need to go out there and buy a specialized tool that does these. And in

**19:32** · specialized tool that does these. And in fact, you can just build them in Claude.

**19:34** · fact, you can just build them in Claude. Um and and this is actually a little bit

**19:36** · Um and and this is actually a little bit where we're going, which is um if I go

**19:37** · where we're going, which is um if I go back to the operating system that I was

**19:39** · back to the operating system that I was showing you earlier. And all of these no

**19:42** · showing you earlier. And all of these no longer have to go through a Dust or a

**19:44** · longer have to go through a Dust or a Claude. Um

**19:46** · Claude. Um instead, what we're able to do, make

**19:49** · instead, what we're able to do, make this much larger, is we can we can take

**19:51** · this much larger, is we can we can take all of these skill files and go into

**19:53** · all of these skill files and go into Claude itself and put them in as skill

**19:56** · Claude itself and put them in as skill files. And so as a result, you could um

**19:58** · files. And so as a result, you could um now you can literally just say, "Hey,

**20:00** · now you can literally just say, "Hey, I'm inside whatever it is I'm doing, and

**20:03** · I'm inside whatever it is I'm doing, and I can just call the, you know, that

**20:05** · I can just call the, you know, that skill

**20:06** · skill /morning briefing product." And as a

**20:08** · /morning briefing product." And as a result, it gives me my briefing right

**20:10** · result, it gives me my briefing right there as opposed to me having to go and

**20:12** · there as opposed to me having to go and call an agent builder.

**20:13** · call an agent builder. >> Mhm. And then should people be setting

**20:16** · >> Mhm. And then should people be setting up like Claude automations on top of

**20:18** · up like Claude automations on top of these to be running these as your daily

**20:20** · these to be running these as your daily morning like running on a schedule or

**20:21** · morning like running on a schedule or something like that?

**20:23** · something like that? >> Yeah, that's a great question. It's so

**20:24** · >> Yeah, that's a great question. It's so funny. Um I'll go I'll share a little

**20:26** · funny. Um I'll go I'll share a little bit of my personal experience. So I set

**20:28** · bit of my personal experience. So I set up a bunch of these scheduled things.

**20:29** · up a bunch of these scheduled things. And even if I just go to scheduled, um

**20:32** · And even if I just go to scheduled, um I'll go right here. You can see that I

**20:34** · I'll go right here. You can see that I have a lot of these scheduled tasks. And

**20:37** · have a lot of these scheduled tasks. And you only see a couple of these pinned.

**20:39** · you only see a couple of these pinned. And what I found was that um

**20:42** · And what I found was that um I it was almost overkill. It was like I

**20:45** · I it was almost overkill. It was like I sat there. I was like, "Oh, I might

**20:46** · sat there. I was like, "Oh, I might automate this." And so I built it. I was

**20:48** · automate this." And so I built it. I was like, "Oh, I might automate that." And

**20:49** · like, "Oh, I might automate that." And so I built it. I was like, "That might

**20:50** · so I built it. I was like, "That might be interesting information." I built it.

**20:51** · be interesting information." I built it. And actually I think we're in a world

**20:53** · And actually I think we're in a world where we are we have information

**20:55** · where we are we have information overload. And so this is why we took the

**20:57** · overload. And so this is why we took the time as a company to be like, "We can't

**20:59** · time as a company to be like, "We can't just assume that people, first of all,

**21:01** · just assume that people, first of all, that they're going to do this for

**21:02** · that they're going to do this for themselves. And second of all, that

**21:03** · themselves. And second of all, that they're not going to be overwhelmed by

**21:05** · they're not going to be overwhelmed by the number of like automations and you

**21:07** · the number of like automations and you know

**21:08** · know schedule things that happen. And as a

**21:10** · schedule things that happen. And as a result, that's how we consolidated it

**21:12** · result, that's how we consolidated it all into what I was showing you earlier,

**21:14** · all into what I was showing you earlier, which is this this idea of actually

**21:16** · which is this this idea of actually having all in one place, because the

**21:18** · having all in one place, because the chances that you're going to come back

**21:20** · chances that you're going to come back and say, "Okay."

**21:22** · and say, "Okay." And again, this is this is this is also

**21:24** · And again, this is this is this is also to to make sure that the information or

**21:26** · to to make sure that the information or like the adoption of AI is actually

**21:28** · like the adoption of AI is actually consistent across the org. And that's

**21:29** · consistent across the org. And that's the main thing. I think that you see a

**21:31** · the main thing. I think that you see a lot of let's say PMs be super AI native,

**21:33** · lot of let's say PMs be super AI native, a lot of engineers be super AI native.

**21:35** · a lot of engineers be super AI native. You don't see the same across all the

**21:37** · You don't see the same across all the functions and potentially sometimes they

**21:39** · functions and potentially sometimes they go to market functions. And so, as a

**21:41** · go to market functions. And so, as a result, we really think hard about how

**21:43** · result, we really think hard about how do we deliver that to you in the form of

**21:46** · do we deliver that to you in the form of something that you can look at on a

**21:48** · something that you can look at on a daily basis and really be integrated

**21:50** · daily basis and really be integrated with

**21:51** · with your workflow. And the last thing I'll

**21:53** · your workflow. And the last thing I'll share at Laurel is we think a lot about

**21:56** · share at Laurel is we think a lot about how do we surface it even more just in

**21:57** · how do we surface it even more just in time. And what we're able to do in terms

**22:00** · time. And what we're able to do in terms of our product is we're able to detect

**22:02** · of our product is we're able to detect what it is you're working on when.

**22:04** · what it is you're working on when. >> Okay, so I think I get it, right? The

**22:06** · >> Okay, so I think I get it, right? The thing that you are encoding that's most

**22:08** · thing that you are encoding that's most important is not the scheduled tasks or

**22:11** · important is not the scheduled tasks or this particular interface in Dust, it is

**22:13** · this particular interface in Dust, it is the actual skills and you are enabling

**22:16** · the actual skills and you are enabling the least AI proficient people at your

**22:18** · the least AI proficient people at your company to operate at a similar level to

**22:21** · company to operate at a similar level to those AI native people. What is the

**22:24** · those AI native people. What is the right company culture? How do you really

**22:26** · right company culture? How do you really get people to take advantage of a

**22:27** · get people to take advantage of a company OS like this?

**22:29** · company OS like this? >> Yeah, absolutely. I think it really

**22:31** · >> Yeah, absolutely. I think it really starts with culture. I just have a few

**22:33** · starts with culture. I just have a few photos from our offsite

**22:36** · photos from our offsite about 3 months ago. And

**22:40** · about 3 months ago. And it's really important to for it to start

**22:42** · it's really important to for it to start from the top, from leadership to say,

**22:44** · from the top, from leadership to say, "This is so important to us. It is not

**22:45** · "This is so important to us. It is not just an engineering thing. It is a

**22:47** · just an engineering thing. It is a cross-company thing." And what we did at

**22:50** · cross-company thing." And what we did at this offsite is we did a company-wide

**22:53** · this offsite is we did a company-wide hackathon. And I do know of a lot of

**22:54** · hackathon. And I do know of a lot of companies that do this on a regular

**22:56** · companies that do this on a regular basis. How do we do a company-wide

**22:58** · basis. How do we do a company-wide hackathon

**22:59** · hackathon every quarter, every 6 weeks, right? Or

**23:03** · every quarter, every 6 weeks, right? Or how do we even get the just the

**23:04** · how do we even get the just the go-to-market teams to do a company do a

**23:06** · go-to-market teams to do a company do a hackathon and show what it is that

**23:08** · hackathon and show what it is that they're building. So, that the

**23:09** · they're building. So, that the expectation that, you know, everyone is

**23:11** · expectation that, you know, everyone is a builder is is true everywhere in the

**23:13** · a builder is is true everywhere in the company, not just in engineering. So,

**23:16** · company, not just in engineering. So, with this, um what we did is we did two

**23:18** · with this, um what we did is we did two things. One, we did um training. And so,

**23:21** · things. One, we did um training. And so, what we did is we actually did a lot of

**23:23** · what we did is we actually did a lot of training around like how do you actually

**23:24** · training around like how do you actually ship to production, even if you're not

**23:26** · ship to production, even if you're not technical. Uh so, we created this

**23:29** · technical. Uh so, we created this um enablement guide for how to ship

**23:31** · um enablement guide for how to ship features with Devon.

**23:32** · features with Devon. And so, you know, Devon essentially is

**23:34** · And so, you know, Devon essentially is like an agentic engineer. Um you can

**23:36** · like an agentic engineer. Um you can give it tasks. It It It started off, I

**23:39** · give it tasks. It It It started off, I would say, a year ago, 2 years ago, when

**23:41** · would say, a year ago, 2 years ago, when we first started using this as almost

**23:43** · we first started using this as almost like intern-level engineer. And today, I

**23:45** · like intern-level engineer. And today, I think it it's actually, you know, a

**23:46** · think it it's actually, you know, a decent software engineer. It's not a

**23:48** · decent software engineer. It's not a staff-level software engineer, but it

**23:49** · staff-level software engineer, but it does a lot of things. And as a result,

**23:52** · does a lot of things. And as a result, you know, um my team is able to ship.

**23:54** · you know, um my team is able to ship. And I'll just give go through a couple

**23:56** · And I'll just give go through a couple examples.

**23:57** · examples. Here is um a feature, an end-to-end

**24:00** · Here is um a feature, an end-to-end feature, which includes front end

**24:02** · feature, which includes front end changes and back end changes, where um

**24:04** · changes and back end changes, where um you know, we enable people to

**24:06** · you know, we enable people to to delete temporary initiatives. So,

**24:08** · to delete temporary initiatives. So, when you're keeping your time, sometimes

**24:10** · when you're keeping your time, sometimes you don't know um what matter or what

**24:12** · you don't know um what matter or what project you're working on yet, but you

**24:14** · project you're working on yet, but you know that you're doing some amount of

**24:15** · know that you're doing some amount of work that should be grouped together and

**24:16** · work that should be grouped together and submitted at the end of the day. And so,

**24:18** · submitted at the end of the day. And so, that's where temporary initiatives is

**24:19** · that's where temporary initiatives is really powerful. Now, that again is a

**24:21** · really powerful. Now, that again is a front end and back end feature. It is

**24:23** · front end and back end feature. It is not just a front end um like almost like

**24:26** · not just a front end um like almost like cosmetic change. It's actually pretty

**24:28** · cosmetic change. It's actually pretty deeply rooted in how does it interact

**24:31** · deeply rooted in how does it interact with PMSs and other systems and when

**24:34** · with PMSs and other systems and when does it release versus not? There

**24:35** · does it release versus not? There There's a lot of complexity in something

**24:36** · There's a lot of complexity in something like um temporary initiatives. And so,

**24:39** · like um temporary initiatives. And so, this, by the way, you know, if you look

**24:40** · this, by the way, you know, if you look at the person actually um

**24:43** · at the person actually um knocking down those tickets and

**24:44** · knocking down those tickets and committing these PRs, this is actually a

**24:46** · committing these PRs, this is actually a PM on my team. And I'll just go to their

**24:48** · PM on my team. And I'll just go to their LinkedIn briefly. Um Nick, who's

**24:51** · LinkedIn briefly. Um Nick, who's awesome, has been at Laurel for some

**24:52** · awesome, has been at Laurel for some time. If I go back to his educational

**24:55** · time. If I go back to his educational history, right? Like um we we didn't

**24:57** · history, right? Like um we we didn't grow up. Many of us didn't grow up as

**24:59** · grow up. Many of us didn't grow up as engineers. And yet Nick, um,

**25:03** · engineers. And yet Nick, um, I would say he probably identifies

**25:04** · I would say he probably identifies self-identifies more on the design side

**25:06** · self-identifies more on the design side than on the engineering side, is able to

**25:08** · than on the engineering side, is able to take this feature end-to-end, which I

**25:11** · take this feature end-to-end, which I think is just so cool. Um, similar to

**25:14** · think is just so cool. Um, similar to similarly, um,

**25:15** · similarly, um, within,

**25:17** · within, you know, many parts of our product,

**25:18** · you know, many parts of our product, I'll just go through another example

**25:19** · I'll just go through another example here.

**25:21** · here. This is, um, the empty state for when

**25:23** · This is, um, the empty state for when someone comes in. So, really think about

**25:25** · someone comes in. So, really think about new user onboarding. What is it that

**25:27** · new user onboarding. What is it that they see? How do How do we make that

**25:29** · they see? How do How do we make that experience super delightful? All of this

**25:31** · experience super delightful? All of this is done by, um, by Jessica, who is,

**25:34** · is done by, um, by Jessica, who is, again, a PM on my team, not an engineer,

**25:37** · again, a PM on my team, not an engineer, and also not a PM who necessarily

**25:39** · and also not a PM who necessarily started their career in, um, in

**25:42** · started their career in, um, in engineering or studied computer science.

**25:45** · engineering or studied computer science. And so, I think this is just such a

**25:46** · And so, I think this is just such a great example of people being able to

**25:48** · great example of people being able to ship even when they're not technical.

**25:50** · ship even when they're not technical. And maybe the last thing I'll show you,

**25:52** · And maybe the last thing I'll show you, cuz I think this is

**25:53** · cuz I think this is even cooler, is, uh, this little picture

**25:56** · even cooler, is, uh, this little picture here, um, which is this is someone on

**25:58** · here, um, which is this is someone on our customer success team. Ashley's

**26:00** · our customer success team. Ashley's amazing. She deeply understands our

**26:02** · amazing. She deeply understands our customers and their needs. And by

**26:04** · customers and their needs. And by working with the PMs on the team to

**26:06** · working with the PMs on the team to really create this enablement guide for

**26:08** · really create this enablement guide for Devon, they worked on this together.

**26:10** · Devon, they worked on this together. So, that, again, if if you are even less

**26:12** · So, that, again, if if you are even less technical than a PM, right? If you're on

**26:14** · technical than a PM, right? If you're on the success team, how might you use this

**26:17** · the success team, how might you use this guide to be able to really ship the way,

**26:20** · guide to be able to really ship the way, um,

**26:21** · um, you know, in a safe way, in in a

**26:24** · you know, in a safe way, in in a reliable way. And then all of these

**26:25** · reliable way. And then all of these pieces we then broke down to say, "Well,

**26:27** · pieces we then broke down to say, "Well, should we start building skill files,

**26:29** · should we start building skill files, you know, agents to help you?" So, that

**26:31** · you know, agents to help you?" So, that when you're trying to do this thing that

**26:33** · when you're trying to do this thing that typically is a playbook. And again, this

**26:34** · typically is a playbook. And again, this is not 55 pages, but it's still eight

**26:36** · is not 55 pages, but it's still eight pages.

**26:37** · pages. You are able to get the help and the

**26:39** · You are able to get the help and the support you need. And so, that is

**26:41** · support you need. And so, that is really, again, the the crux of it all is

**26:43** · really, again, the the crux of it all is understanding what is the work that

**26:45** · understanding what is the work that you're doing, how do you start to

**26:46** · you're doing, how do you start to document that down, and then really

**26:49** · document that down, and then really clearly define these are the parts that

**26:50** · clearly define these are the parts that remain human-centric versus these are

**26:53** · remain human-centric versus these are the parts that should be automated away.

**26:57** · the parts that should be automated away. I'll pause there, but I think it's also

**26:58** · I'll pause there, but I think it's also really cool to look at this ontology,

**27:00** · really cool to look at this ontology, which is essentially, you know, for

**27:01** · which is essentially, you know, for every single function in the company,

**27:03** · every single function in the company, what are all the buckets of work that

**27:05** · what are all the buckets of work that they're doing? And And what we do is

**27:07** · they're doing? And And what we do is actually we we actually spend cycles

**27:09** · actually we we actually spend cycles saying, "You know what? We believe that,

**27:11** · saying, "You know what? We believe that, like I said earlier, a product person

**27:13** · like I said earlier, a product person should be operating like an engineer."

**27:15** · should be operating like an engineer." So, all of the the things that we expect

**27:17** · So, all of the the things that we expect an engineer to do, we expect them to be

**27:20** · an engineer to do, we expect them to be doing feature work. We expect them to be

**27:22** · doing feature work. We expect them to be testing. You know, we're we expect them

**27:24** · testing. You know, we're we expect them to actually like crank through the

**27:25** · to actually like crank through the backlog. The exact same things show up

**27:28** · backlog. The exact same things show up in what we want PMs to do. Um it is it

**27:31** · in what we want PMs to do. Um it is it is not a um

**27:33** · is not a um an error where, you know, here in the

**27:35** · an error where, you know, here in the ontology,

**27:36** · ontology, we really have things like we want you

**27:38** · we really have things like we want you to be, you know, doing feature work with

**27:39** · to be, you know, doing feature work with agents. We want you to be um, you know,

**27:42** · agents. We want you to be um, you know, actually QAing your your product and

**27:44** · actually QAing your your product and fixing the bugs, not just like QAing in

**27:46** · fixing the bugs, not just like QAing in in the ways that people were doing

**27:47** · in the ways that people were doing before.

**27:48** · before. And what we don't want you to be doing

**27:50** · And what we don't want you to be doing is things that were really tedious, like

**27:52** · is things that were really tedious, like synthesizing competitive market, you

**27:54** · synthesizing competitive market, you know, intelligence, um actually writing

**27:56** · know, intelligence, um actually writing these like detailed briefs, doing

**27:57** · these like detailed briefs, doing research planning, doing reach out for

**28:00** · research planning, doing reach out for the the research, synthesizing the

**28:02** · the the research, synthesizing the research. Like all of that, um you know,

**28:04** · research. Like all of that, um you know, competitive analysis is a great example.

**28:06** · competitive analysis is a great example. It should You should be spending time

**28:08** · It should You should be spending time building the agent to pull the

**28:10** · building the agent to pull the competitive data, and you should just be

**28:11** · competitive data, and you should just be moderating it, but you shouldn't

**28:13** · moderating it, but you shouldn't actually be doing the deep work every

**28:15** · actually be doing the deep work every single day. And like set up the system

**28:16** · single day. And like set up the system instead. And so, when we actually create

**28:19** · instead. And so, when we actually create this ontology, we're able to say, "Well,

**28:21** · this ontology, we're able to say, "Well, we want these numbers to go up. We want

**28:24** · we want these numbers to go up. We want everything in green, the time spent

**28:26** · everything in green, the time spent doing that to go up. I want to see Nick

**28:29** · doing that to go up. I want to see Nick doing this. I want to see Jess, you

**28:31** · doing this. I want to see Jess, you know, shipping this this this feature

**28:33** · know, shipping this this this feature end-to-end. But what I want you to stop

**28:36** · end-to-end. But what I want you to stop doing is I want you to stop doing these

**28:38** · doing is I want you to stop doing these things that are really tedious, or the

**28:40** · things that are really tedious, or the very least be calling an agent every

**28:42** · very least be calling an agent every single time that you want to do that."

**28:44** · single time that you want to do that." And And then

**28:45** · And And then again, going back to how do we make that

**28:48** · again, going back to how do we make that true? By building the skill files, by

**28:51** · true? By building the skill files, by building the agent agentic workflows

**28:53** · building the agent agentic workflows where necessary, and making sure that

**28:55** · where necessary, and making sure that we're surfacing for surfacing them where

**28:57** · we're surfacing for surfacing them where people work. And that's ultimately the

**28:59** · people work. And that's ultimately the the key pieces of the system.

**29:01** · the key pieces of the system. >> Wow, there is so much gold buried

**29:05** · >> Wow, there is so much gold buried in the various parts of your answer

**29:07** · in the various parts of your answer there. The first part I want to double

**29:09** · there. The first part I want to double click on first is PMs shipping to

**29:11** · click on first is PMs shipping to production. Okay, people have heard

**29:13** · production. Okay, people have heard about that. But PMs not just shipping,

**29:16** · about that. But PMs not just shipping, okay, here's this little growth

**29:18** · okay, here's this little growth experiment where we change the text in a

**29:20** · experiment where we change the text in a button, which is a front-end only

**29:22** · button, which is a front-end only change, but a front-end plus back-end

**29:25** · change, but a front-end plus back-end core feature, this temporary initiatives

**29:27** · core feature, this temporary initiatives feature for instance that we looked at.

**29:29** · feature for instance that we looked at. That's crazy. So, talk to me a little

**29:31** · That's crazy. So, talk to me a little bit about

**29:33** · bit about what is the scope of what PMs do ship to

**29:36** · what is the scope of what PMs do ship to production, and how should people be

**29:38** · production, and how should people be thinking about in an AI-native

**29:39** · thinking about in an AI-native organization,

**29:41** · organization, this is the role of a PM today.

**29:44** · this is the role of a PM today. >> We talk a lot about this in terms of

**29:47** · >> We talk a lot about this in terms of what is engineering anyways, what is

**29:48** · what is engineering anyways, what is product anyways, what is design anyways,

**29:50** · product anyways, what is design anyways, and we really landed on this concept of

**29:53** · and we really landed on this concept of um

**29:54** · um we want there always to be a captain of

**29:57** · we want there always to be a captain of any given initiative, and the captain is

**30:00** · any given initiative, and the captain is the person where that skill set is the

**30:03** · the person where that skill set is the most important. And so, there are lots

**30:06** · most important. And so, there are lots of features, um let's say we need to

**30:09** · of features, um let's say we need to overhaul

**30:10** · overhaul a system in order to make it much easier

**30:13** · a system in order to make it much easier for, let's say, PMs to ship agents to

**30:15** · for, let's say, PMs to ship agents to work in that codebase. Usually, the

**30:17** · work in that codebase. Usually, the captain is an engineering captain

**30:18** · captain is an engineering captain because that's an architectural change.

**30:20** · because that's an architectural change. If we have a feature where um like the

**30:24** · If we have a feature where um like the interaction is really king, you know,

**30:26** · interaction is really king, you know, we're doing this really cool stuff on

**30:27** · we're doing this really cool stuff on mobile to make it so easy and delightful

**30:29** · mobile to make it so easy and delightful to kind of like look at how you spend

**30:31** · to kind of like look at how you spend your time in a given day and get

**30:33** · your time in a given day and get insights from that.

**30:34** · insights from that. >> I hope you're enjoying today's episode.

**30:36** · >> I hope you're enjoying today's episode. Are you interested in becoming an AI

**30:38** · Are you interested in becoming an AI product manager making hundreds of

**30:40** · product manager making hundreds of thousands of dollars more joining OpenAI

**30:42** · thousands of dollars more joining OpenAI and Anthropic, then you might want to do

**30:44** · and Anthropic, then you might want to do a course that I've taken myself, the

**30:46** · a course that I've taken myself, the AIPM certificate ran by OpenAI product

**30:49** · AIPM certificate ran by OpenAI product leader Mickdad Jaffer. If you use my

**30:51** · leader Mickdad Jaffer. If you use my code and my link, you get a special

**30:54** · code and my link, you get a special discount on this course. It is a course

**30:56** · discount on this course. It is a course that I highly recommend. We have done a

**30:58** · that I highly recommend. We have done a lot of collaborations together on things

**31:00** · lot of collaborations together on things like AI product strategy. So, check out

**31:02** · like AI product strategy. So, check out our newsletter articles if you want to

**31:04** · our newsletter articles if you want to see the quality of the type of thinking

**31:06** · see the quality of the type of thinking you'll get. One of my frequent

**31:07** · you'll get. One of my frequent collaborators, Pavel Hearn, is the build

**31:10** · collaborators, Pavel Hearn, is the build labs leader, so you're going to live

**31:11** · labs leader, so you're going to live build an AI product with Pavel's

**31:13** · build an AI product with Pavel's feedback if you take this AIPM

**31:15** · feedback if you take this AIPM certificate. So, be sure to check that

**31:17** · certificate. So, be sure to check that out. Be sure to use my code and my link

**31:19** · out. Be sure to use my code and my link in order to get a special discount. And

**31:20** · in order to get a special discount. And now back into today's episode. I used to

**31:22** · now back into today's episode. I used to think I had a retention problem. Turns

**31:24** · think I had a retention problem. Turns out I had a messaging problem. I was

**31:26** · out I had a messaging problem. I was sending the same onboarding emails to

**31:28** · sending the same onboarding emails to every new user, whether they activated

**31:30** · every new user, whether they activated on day one or never logged in again. I

**31:32** · on day one or never logged in again. I had no [music] idea who was slipping or

**31:33** · had no [music] idea who was slipping or why. Customer.io changed that. Every

**31:35** · why. Customer.io changed that. Every message I send is now based [music] on

**31:37** · message I send is now based [music] on what users actually do in the product.

**31:40** · what users actually do in the product. Someone hits a key activation moment,

**31:41** · Someone hits a key activation moment, they get nudged to the next one. Someone

**31:43** · they get nudged to the next one. Someone goes quiet, [music] they get a different

**31:44** · goes quiet, [music] they get a different path entirely. Their AI agent makes it

**31:46** · path entirely. Their AI agent makes it fast. I describe the campaign I [music]

**31:48** · fast. I describe the campaign I [music] want and it builds the full journey for

**31:49** · want and it builds the full journey for me. Triggers, timing, copy, even

**31:52** · me. Triggers, timing, copy, even branching logic. And when I want to know

**31:54** · branching logic. And when I want to know how something is performing, [music] I

**31:55** · how something is performing, [music] I just ask the agent directly and it tells

**31:57** · just ask the agent directly and it tells me what to do next. They also have an

**31:59** · me what to do next. They also have an MCP server, [music] which means AI tools

**32:01** · MCP server, [music] which means AI tools like Claude can see directly what's

**32:03** · like Claude can see directly what's happening in your Customer.io workspace.

**32:05** · happening in your Customer.io workspace. [music] Your segments, your customer

**32:06** · [music] Your segments, your customer data, your attribution, all of it. So,

**32:08** · data, your attribution, all of it. So, instead of explaining your business

**32:10** · instead of explaining your business [music] context every time you need

**32:11** · [music] context every time you need help, Claude already knows it. Notion

**32:13** · help, Claude already knows it. Notion used Customer.io to personalize their

**32:15** · used Customer.io to personalize their onboarding and hit nearly 50% open rate,

**32:19** · onboarding and hit nearly 50% open rate, improved conversion by 6 to 7% with

**32:21** · improved conversion by 6 to 7% with localized campaigns, and pushed open

**32:23** · localized campaigns, and pushed open rates up another 20% through AB testing.

**32:26** · rates up another 20% through AB testing. [music] The idea is simple. Customer.io

**32:28** · [music] The idea is simple. Customer.io helps you deliver more impact from every

**32:30** · helps you deliver more impact from every message you send. If you're a PM or

**32:32** · message you send. If you're a PM or founder and your onboarding is still one

**32:33** · founder and your onboarding is still one size fits all, try Customer.io at

**32:35** · size fits all, try Customer.io at Customer.io. That is more so than

**32:38** · Customer.io. That is more so than anything, it's it's a data problem. So,

**32:40** · anything, it's it's a data problem. So, we have, you know, data science really

**32:41** · we have, you know, data science really plugged in there. But, really um

**32:44** · plugged in there. But, really um the interaction is the most important

**32:46** · the interaction is the most important thing to really sweat and make sure it's

**32:48** · thing to really sweat and make sure it's delightful. And as a result, a designer

**32:50** · delightful. And as a result, a designer is a captain of that work stream. And

**32:52** · is a captain of that work stream. And then something like what I just showed

**32:53** · then something like what I just showed you, something like temporary

**32:55** · you, something like temporary initiatives, something like the empty

**32:57** · initiatives, something like the empty states,

**32:58** · states, really having deep customer

**33:00** · really having deep customer understanding, but also business context

**33:03** · understanding, but also business context is really important. How do I know what

**33:05** · is really important. How do I know what people want to do with temporary

**33:06** · people want to do with temporary initiatives? How do I know what the user

**33:08** · initiatives? How do I know what the user wants to do, but also how do I know what

**33:10** · wants to do, but also how do I know what the firm really wants to get out of it

**33:13** · the firm really wants to get out of it and or not? And so, what we spend a lot

**33:15** · and or not? And so, what we spend a lot of time now thinking about is what is

**33:17** · of time now thinking about is what is the what is the most critical piece to

**33:20** · the what is the most critical piece to nail for the outcome that we're looking

**33:23** · nail for the outcome that we're looking for and therefore the feature that we're

**33:25** · for and therefore the feature that we're building? And as a result, how do we

**33:27** · building? And as a result, how do we appoint a captain that is skilled in

**33:30** · appoint a captain that is skilled in that particular area? And so, that

**33:32** · that particular area? And so, that that's generally how we think about um

**33:34** · that's generally how we think about um the model evolving. And so, going back

**33:36** · the model evolving. And so, going back to a feature that might touch the front

**33:38** · to a feature that might touch the front end and the back end, if we believe that

**33:41** · end and the back end, if we believe that the back end is in a good enough spot,

**33:43** · the back end is in a good enough spot, and by the way, you can ask GitHub uh

**33:45** · and by the way, you can ask GitHub uh sorry, Devin um or even, you know, you

**33:47** · sorry, Devin um or even, you know, you like anything that's connected to your

**33:48** · like anything that's connected to your GitHub account to to look at the code

**33:50** · GitHub account to to look at the code and say, you know, in what state is

**33:52** · and say, you know, in what state is this, right? And and it actually gives

**33:53** · this, right? And and it actually gives you a pretty good answer. Hey, you know,

**33:55** · you a pretty good answer. Hey, you know, this this is this is what I would be

**33:57** · this this is this is what I would be careful of. Um uh and then you can

**33:59** · careful of. Um uh and then you can actually pull in engineering um to to on

**34:02** · actually pull in engineering um to to on the parts where you're like, this is

**34:03** · the parts where you're like, this is probably the most contentious or this is

**34:05** · probably the most contentious or this is where it gets the most risky. And again,

**34:07** · where it gets the most risky. And again, you don't do this by yourself because

**34:08** · you don't do this by yourself because you happen to be the most technical

**34:10** · you happen to be the most technical person. We're not. Um you do this

**34:12** · person. We're not. Um you do this through the help of asking, you know,

**34:14** · through the help of asking, you know, Claude code to look at your code base,

**34:16** · Claude code to look at your code base, cursor, what I mean, whatever tool of

**34:18** · cursor, what I mean, whatever tool of choice you choose to use, you can ask it

**34:21** · choice you choose to use, you can ask it to really give you answers the same way

**34:23** · to really give you answers the same way that a marketer would say, "Look, I'm

**34:25** · that a marketer would say, "Look, I'm giving you some copy. Now, battle test

**34:27** · giving you some copy. Now, battle test this and go back and forth." It's the

**34:28** · this and go back and forth." It's the same concept. And and then going back to

**34:31** · same concept. And and then going back to if you are clear on again, what is the

**34:33** · if you are clear on again, what is the hardest thing to to get right in a

**34:35** · hardest thing to to get right in a particular feature? Um for example,

**34:38** · particular feature? Um for example, empty state. The empty state that we're

**34:40** · empty state. The empty state that we're working on here, it's the hardest part

**34:42** · working on here, it's the hardest part to get right is definitely not the

**34:43** · to get right is definitely not the engineering. The hardest part to get

**34:44** · engineering. The hardest part to get right is not even the design, it's the

**34:45** · right is not even the design, it's the content. And again, the content has to

**34:47** · content. And again, the content has to do with the user and the business and

**34:49** · do with the user and the business and the firm, and that is a very classic PM

**34:52** · the firm, and that is a very classic PM thing. And so it makes sense for the PM

**34:54** · thing. And so it makes sense for the PM to be the captain of that. And so that's

**34:56** · to be the captain of that. And so that's really the model we think about.

**34:58** · really the model we think about. Captains, you know, using um um you

**35:01** · Captains, you know, using um um you know, LLMs essentially like ask how hard

**35:04** · know, LLMs essentially like ask how hard something can be. Obviously, we still,

**35:07** · something can be. Obviously, we still, you know, have code review, um and we

**35:09** · you know, have code review, um and we make sure that um engineers are code

**35:11** · make sure that um engineers are code reviewing the things that are risky. Um

**35:13** · reviewing the things that are risky. Um and so all of those pieces together

**35:15** · and so all of those pieces together makes it so that we can all ship,

**35:17** · makes it so that we can all ship, including, you know, customer success,

**35:19** · including, you know, customer success, which is again really wild. And and like

**35:21** · which is again really wild. And and like go-to-market sales.

**35:22** · go-to-market sales. >> And I think we can all immediately see

**35:24** · >> And I think we can all immediately see how that allows engineers to work on the

**35:28** · how that allows engineers to work on the highest leverage back-end tasks, PMs to

**35:31** · highest leverage back-end tasks, PMs to work on higher leverage features if CSM

**35:32** · work on higher leverage features if CSM and go-to-market are enabled. What is

**35:35** · and go-to-market are enabled. What is the

**35:36** · the right set of checks and balances you

**35:38** · right set of checks and balances you need to put in place in your

**35:39** · need to put in place in your organization? How do you You mentioned

**35:42** · organization? How do you You mentioned code reviews. Where Where do those come

**35:44** · code reviews. Where Where do those come in? How do you

**35:45** · in? How do you CSMs or uh

**35:48** · CSMs or uh go-to-market, for instance, make sure

**35:50** · go-to-market, for instance, make sure that what they're building isn't in

**35:51** · that what they're building isn't in conflict with something the product team

**35:52** · conflict with something the product team is building over here, in contact

**35:54** · is building over here, in contact conflict with somebody else's metrics?

**35:56** · conflict with somebody else's metrics? Usually, that's where the PM came in and

**35:58** · Usually, that's where the PM came in and did a lot of the glue work. How do you

**35:59** · did a lot of the glue work. How do you handle that in this new way of working?

**36:01** · handle that in this new way of working? >> Yeah, that's a great question. Um so we

**36:05** · >> Yeah, that's a great question. Um so we again, I believe in the power of humans.

**36:07** · again, I believe in the power of humans. So something as simple as, you know,

**36:08** · So something as simple as, you know, creating a channel like ask Devin

**36:11** · creating a channel like ask Devin reviewers, and being able to go through

**36:13** · reviewers, and being able to go through here, um and making sure that there's

**36:14** · here, um and making sure that there's visibility around all of the Devin um

**36:18** · visibility around all of the Devin um all the ways we're using Devin to ship,

**36:19** · all the ways we're using Devin to ship, and then tagging in the right person,

**36:21** · and then tagging in the right person, tagging in, you know, um a front-end

**36:23** · tagging in, you know, um a front-end engineer to really look at something,

**36:24** · engineer to really look at something, tagging a designer to look at something

**36:26** · tagging a designer to look at something else, really going through and um making

**36:29** · else, really going through and um making it visible. I think the first advice I'd

**36:31** · it visible. I think the first advice I'd give is transparency is everything.

**36:34** · give is transparency is everything. Um the second piece of advice is you do

**36:37** · Um the second piece of advice is you do need to set some ground rules, right? So

**36:39** · need to set some ground rules, right? So again, going back to our enablement

**36:40** · again, going back to our enablement guide, we've set some ground rules here

**36:43** · guide, we've set some ground rules here as part of even the way Devon works. We

**36:46** · as part of even the way Devon works. We often we

**36:47** · often we we actually used to

**36:50** · we actually used to do this quick check where whenever

**36:52** · do this quick check where whenever someone, let's say someone on support

**36:55** · someone, let's say someone on support had an idea.

**36:56** · had an idea. They essentially could go into this

**36:58** · They essentially could go into this channel and post their idea and get a

**37:00** · channel and post their idea and get a really quick check on

**37:03** · really quick check on is this something that

**37:05** · is this something that makes sense? And again, I'll just let me

**37:07** · makes sense? And again, I'll just let me zoom in here. Like I'm proposing a

**37:08** · zoom in here. Like I'm proposing a change to this experience.

**37:11** · change to this experience. Um getting some some feedback, right?

**37:14** · Um getting some some feedback, right? And and being able to say, "Hey, play

**37:15** · And and being able to say, "Hey, play around with the first version of it."

**37:18** · around with the first version of it." And and getting you know, people to

**37:19** · And and getting you know, people to chime in and say, "Hey, this makes

**37:21** · chime in and say, "Hey, this makes sense. This doesn't make sense. I'm I'm

**37:23** · sense. This doesn't make sense. I'm I'm on the engineering team and let me give

**37:24** · on the engineering team and let me give you some feedback. I'm on the success

**37:25** · you some feedback. I'm on the success team. Let me give you some feedback."

**37:27** · team. Let me give you some feedback." What you're really doing is you're

**37:28** · What you're really doing is you're taking what used to be a product review

**37:30** · taking what used to be a product review that used to take time to schedule and

**37:32** · that used to take time to schedule and time to get all the stakeholders in the

**37:34** · time to get all the stakeholders in the same room and you're just compressing

**37:36** · same room and you're just compressing it.

**37:36** · it. >> Double click on product reviews for me.

**37:38** · >> Double click on product reviews for me. You guys have a really interesting

**37:39** · You guys have a really interesting process for when you do and don't do

**37:41** · process for when you do and don't do product reviews. What is

**37:43** · product reviews. What is the right balance so that you enable

**37:45** · the right balance so that you enable people to move fast but you're building

**37:47** · people to move fast but you're building the right level of collaboration on

**37:49** · the right level of collaboration on bigger features?

**37:50** · bigger features? >> Yeah, the same way we have this

**37:52** · >> Yeah, the same way we have this captain's model, I think about a

**37:54** · captain's model, I think about a framework what we call two tracks. So

**37:56** · framework what we call two tracks. So there's one track which is much smaller.

**37:57** · there's one track which is much smaller. If you have something that

**38:00** · If you have something that even some of the features I just showed

**38:01** · even some of the features I just showed you, like they're they're small enough

**38:02** · you, like they're they're small enough where again, a PM, um somebody, a

**38:06** · where again, a PM, um somebody, a product captain or a product builder,

**38:08** · product captain or a product builder, right, can take it end-to-end. Those

**38:10** · right, can take it end-to-end. Those don't go through the same degree of

**38:13** · don't go through the same degree of rigorous review but they do go through

**38:15** · rigorous review but they do go through things like that ask Devon channel. They

**38:17** · things like that ask Devon channel. They go through things, you know, like a like

**38:19** · go through things, you know, like a like someone looking at the PR, making sure

**38:21** · someone looking at the PR, making sure things are good. Um, you, by the way,

**38:23** · things are good. Um, you, by the way, you are responsible for end-to-end

**38:24** · you are responsible for end-to-end testing of your features. I think that's

**38:25** · testing of your features. I think that's actually really positive. The number of

**38:27** · actually really positive. The number of times where in a waterfall model, you

**38:29** · times where in a waterfall model, you would PM throws over to the designer and

**38:31** · would PM throws over to the designer and the designer throws over to the engineer

**38:32** · the designer throws over to the engineer and then engineer throws back to the

**38:33** · and then engineer throws back to the designer, do design, QA, and the

**38:35** · designer, do design, QA, and the designer's like, this is not what

**38:36** · designer's like, this is not what [laughter] I designed. Um, that is just

**38:38** · [laughter] I designed. Um, that is just I think it's just such a It's like it's

**38:40** · I think it's just such a It's like it's almost a meme cuz it happens so often.

**38:43** · almost a meme cuz it happens so often. And so, I think that's actually really

**38:43** · And so, I think that's actually really empowering to say, I am the end-to-end

**38:47** · empowering to say, I am the end-to-end product builder and I take something

**38:49** · product builder and I take something from beginning to end and I own and I'm

**38:51** · from beginning to end and I own and I'm responsible for the quality and impact

**38:54** · responsible for the quality and impact of this thing. And so, first of all, I

**38:55** · of this thing. And so, first of all, I just think that's a much more empowered

**38:56** · just think that's a much more empowered way to work. Um, so, but but then going

**38:59** · way to work. Um, so, but but then going back to the two tracks, you have things

**39:01** · back to the two tracks, you have things that, you know, can really take the

**39:02** · that, you know, can really take the product life cycle and compress it down

**39:04** · product life cycle and compress it down to a day, an hour, you know, like and

**39:07** · to a day, an hour, you know, like and that's how you get the velocity. But,

**39:09** · that's how you get the velocity. But, there are some things where you're like,

**39:10** · there are some things where you're like, look, I think that the way that this

**39:12** · look, I think that the way that this product is going to behave, what I'm

**39:14** · product is going to behave, what I'm suggesting is a change, the feature that

**39:16** · suggesting is a change, the feature that I want to do, it requires more much more

**39:19** · I want to do, it requires more much more alignment. So, a great example is, um,

**39:22** · alignment. So, a great example is, um, within Laurel, if you're going to change

**39:23** · within Laurel, if you're going to change the complete way that activities are

**39:25** · the complete way that activities are displayed,

**39:27** · displayed, that's a that's a pretty radical change.

**39:29** · that's a that's a pretty radical change. Um, and how might someone a user go zoom

**39:31** · Um, and how might someone a user go zoom in and out of their day?

**39:33** · in and out of their day? That is not a small thing. It require It

**39:35** · That is not a small thing. It require It touches, um, it's the whole like user

**39:38** · touches, um, it's the whole like user interaction. And as a result, we say,

**39:40** · interaction. And as a result, we say, look, we do want to do a product review

**39:41** · look, we do want to do a product review for that. Want to make sure that, um, we

**39:43** · for that. Want to make sure that, um, we talk about, well, how do we think about

**39:45** · talk about, well, how do we think about the entire product as a system so that

**39:47** · the entire product as a system so that we're not adding some random thing over

**39:49** · we're not adding some random thing over there and a random thing over there. Um,

**39:51** · there and a random thing over there. Um, but a lot of

**39:53** · but a lot of I think the first step is to actually

**39:54** · I think the first step is to actually even say, what is in what bucket? So

**39:56** · even say, what is in what bucket? So that the things that could be running

**39:58** · that the things that could be running really fast are, but also, I really

**40:00** · really fast are, but also, I really don't believe in this. I think a lot of

**40:02** · don't believe in this. I think a lot of quote-unquote AI-native companies are

**40:03** · quote-unquote AI-native companies are just like, roadmaps are gone, planning

**40:05** · just like, roadmaps are gone, planning is a gone, everything is gone. Um, and

**40:07** · is a gone, everything is gone. Um, and what I say is, well, if everyone's

**40:09** · what I say is, well, if everyone's running in different directions, even if

**40:10** · running in different directions, even if you're running incredibly fast, you're

**40:12** · you're running incredibly fast, you're not really going to get anywhere. And I

**40:14** · not really going to get anywhere. And I see a lot of, um, great like local

**40:17** · see a lot of, um, great like local maximizations, but sometimes it's really

**40:19** · maximizations, but sometimes it's really hard to get to the global max, you know,

**40:21** · hard to get to the global max, you know, a whole new set function change in your

**40:23** · a whole new set function change in your product in your market positioning

**40:25** · product in your market positioning without real rigorous thought around

**40:28** · without real rigorous thought around what is our strategy, what is our plan,

**40:30** · what is our strategy, what is our plan, why are we differentiated? And those are

**40:32** · why are we differentiated? And those are the things that require much more of

**40:34** · the things that require much more of what I call a true product review

**40:36** · what I call a true product review process, where to me it's more like

**40:38** · process, where to me it's more like product strategy review, and then

**40:40** · product strategy review, and then there's architectural review, right?

**40:42** · there's architectural review, right? Making sure that the system actually

**40:44** · Making sure that the system actually will support all the changes that you

**40:45** · will support all the changes that you want and that you can get to a next

**40:47** · want and that you can get to a next level of running fast.

**40:49** · level of running fast. >> Mhm.

**40:50** · >> Mhm. So, did temporary initiatives go through

**40:51** · So, did temporary initiatives go through a product review?

**40:52** · a product review? >> It did not.

**40:53** · >> It did not. >> Wow. Okay. So, what would be the like

**40:56** · >> Wow. Okay. So, what would be the like the right aperture? What have been some

**40:58** · the right aperture? What have been some of your recent product strategy reviews?

**41:00** · of your recent product strategy reviews? >> Yeah, so um

**41:02** · >> Yeah, so um today Laurel is beloved in a lot of

**41:05** · today Laurel is beloved in a lot of firms that think about billable hours.

**41:08** · firms that think about billable hours. And we're starting to find that there

**41:09** · And we're starting to find that there are a lot of firms, even if they don't

**41:11** · are a lot of firms, even if they don't have billable hours, um they really

**41:12** · have billable hours, um they really think they still need to think about the

**41:13** · think they still need to think about the concept of time. Um I would say it even

**41:16** · concept of time. Um I would say it even applies to tech. I think about the

**41:17** · applies to tech. I think about the concept of time all the time. What are

**41:19** · concept of time all the time. What are my PMs doing? Going back to this

**41:21** · my PMs doing? Going back to this ontology um and and this work map of

**41:24** · ontology um and and this work map of every single function. I mean, all of us

**41:25** · every single function. I mean, all of us should be thinking about the concept of

**41:27** · should be thinking about the concept of time. What should sales people be doing

**41:29** · time. What should sales people be doing today versus what should not be human

**41:32** · today versus what should not be human anymore.

**41:33** · anymore. And this is I want to be very clear,

**41:34** · And this is I want to be very clear, this is not a therefore we do not hire

**41:36** · this is not a therefore we do not hire humans. It is a put the humans on the

**41:38** · humans. It is a put the humans on the most important things. And I'll give you

**41:41** · most important things. And I'll give you some great examples in here.

**41:43** · some great examples in here. Relationship building. You just will

**41:45** · Relationship building. You just will never replace a real check-in, a real

**41:48** · never replace a real check-in, a real moment of you know, true hospitality and

**41:51** · moment of you know, true hospitality and delight, an actual on-site, taking a

**41:53** · delight, an actual on-site, taking a champion out to dinner. That cannot be

**41:55** · champion out to dinner. That cannot be replaced by agents.

**41:57** · replaced by agents. But what will make it so much easier to

**42:00** · But what will make it so much easier to operate and and no one actually wants to

**42:02** · operate and and no one actually wants to do these things. What if the scheduling

**42:04** · do these things. What if the scheduling for the on-site and making sure that all

**42:06** · for the on-site and making sure that all of the back and forth and logistics is

**42:07** · of the back and forth and logistics is taken care of. You know, again, in

**42:09** · taken care of. You know, again, in marketing we do a lot of events. What if

**42:10** · marketing we do a lot of events. What if all the logistics of event planning were

**42:12** · all the logistics of event planning were gone? Even this idea of unreasonable

**42:14** · gone? Even this idea of unreasonable hospitality, and I I think this is such

**42:16** · hospitality, and I I think this is such a a great example. It is such a core

**42:19** · a a great example. It is such a core value of us of ours here at Laurel,

**42:22** · value of us of ours here at Laurel, where we really want to delight our

**42:25** · where we really want to delight our customers all the time. We want to

**42:26** · customers all the time. We want to delight each other, want to delight our

**42:27** · delight each other, want to delight our customers, and so we really have

**42:29** · customers, and so we really have codified unreasonable hospitality as as

**42:31** · codified unreasonable hospitality as as almost like a like a cultural principle

**42:33** · almost like a like a cultural principle that we have, a company value.

**42:35** · that we have, a company value. A lot of companies do this, by the way.

**42:36** · A lot of companies do this, by the way. They're like, this is a cultural company

**42:38** · They're like, this is a cultural company value, and then it's in a doc somewhere.

**42:41** · value, and then it's in a doc somewhere. People read it and then they forget

**42:43** · People read it and then they forget about it. And what we do instead is we

**42:44** · about it. And what we do instead is we say, "Well, what does it actually mean?"

**42:46** · say, "Well, what does it actually mean?" We actually want to make sure that no

**42:48** · We actually want to make sure that no matter who you are, even if you're the

**42:51** · matter who you are, even if you're the most thoughtful person in the world, or

**42:52** · most thoughtful person in the world, or you're not the most thoughtful person in

**42:53** · you're not the most thoughtful person in the world, even if you're 4 years into

**42:55** · the world, even if you're 4 years into your time at Laurel, or you're 4 days

**42:57** · your time at Laurel, or you're 4 days into your time at Laurel, you understand

**42:59** · into your time at Laurel, you understand that unreasonable hospitality is a

**43:01** · that unreasonable hospitality is a requirement of how we operate. And

**43:03** · requirement of how we operate. And especially if you're on the customer

**43:05** · especially if you're on the customer success team, we expect that you do this

**43:08** · success team, we expect that you do this with our customers. How do we

**43:09** · with our customers. How do we systematize that? And and and that's a

**43:12** · systematize that? And and and that's a real real question. You know, again,

**43:14** · real real question. You know, again, there are people on our team who

**43:16** · there are people on our team who just from who they are as humans,

**43:18** · just from who they are as humans, they're the kind of people who's like,

**43:19** · they're the kind of people who's like, "Someone told me that they're going to

**43:20** · "Someone told me that they're going to Mexico." And so, and it's the first

**43:22** · Mexico." And so, and it's the first time, by the way, that they're traveling

**43:23** · time, by the way, that they're traveling outside of the country. And so, I bought

**43:25** · outside of the country. And so, I bought them an engraved passport holder.

**43:28** · them an engraved passport holder. That is, by the way, a lot of people on

**43:30** · That is, by the way, a lot of people on the Laurel team, but if I were to scale

**43:32** · the Laurel team, but if I were to scale that to like a lot a lot of people and

**43:34** · that to like a lot a lot of people and make sure that everyone's doing it every

**43:36** · make sure that everyone's doing it every point in time, even when they're really

**43:37** · point in time, even when they're really busy with other stuff, it's pretty

**43:39** · busy with other stuff, it's pretty unlikely that's going to happen.

**43:41** · unlikely that's going to happen. Instead, we say, "Well, we actually want

**43:43** · Instead, we say, "Well, we actually want to make sure that unreasonable

**43:44** · to make sure that unreasonable hospitality is a check that we put in."

**43:46** · hospitality is a check that we put in." And so, again, going back to the OS I

**43:47** · And so, again, going back to the OS I was showing you, "Hey, if you have a

**43:49** · was showing you, "Hey, if you have a check-in with someone,

**43:51** · check-in with someone, and you know, you haven't actually done

**43:53** · and you know, you haven't actually done anything like this in a while, you

**43:55** · anything like this in a while, you haven't had an in-person touchpoint, how

**43:57** · haven't had an in-person touchpoint, how might you surprise and delight them?"

**43:59** · might you surprise and delight them?" And here's some ideas that we've already

**44:00** · And here's some ideas that we've already pulled for you. We pulled from your Gong

**44:03** · pulled for you. We pulled from your Gong transcripts that these are things that

**44:04** · transcripts that these are things that they love. And we pulled um, from the

**44:07** · they love. And we pulled um, from the fact that they love these things,

**44:08** · fact that they love these things, instead of making you do all the work of

**44:10** · instead of making you do all the work of figuring out, is it a passport holder?

**44:12** · figuring out, is it a passport holder? How do I even get a passport holder

**44:13** · How do I even get a passport holder engraved? We are going to we're going to

**44:15** · engraved? We are going to we're going to systematize that. And so, that's this

**44:17** · systematize that. And so, that's this real idea of like deeply understanding

**44:19** · real idea of like deeply understanding your your your company's work, your

**44:22** · your your your company's work, your team's work. What are the things that

**44:25** · team's work. What are the things that makes you special? Where do you put the

**44:27** · makes you special? Where do you put the humans on the things that make you

**44:29** · humans on the things that make you special? And then, where do you even in

**44:30** · special? And then, where do you even in those moments, like unreasonable

**44:32** · those moments, like unreasonable hospitality, make it so it's easier to

**44:34** · hospitality, make it so it's easier to do that job and to deliver that

**44:36** · do that job and to deliver that particular feeling.

**44:37** · particular feeling. >> So, you This isn't your first rodeo.

**44:40** · >> So, you This isn't your first rodeo. You've been in product for a really long

**44:44** · You've been in product for a really long time. If we rewind back to some of those

**44:46** · time. If we rewind back to some of those experiences, those formative

**44:47** · experiences, those formative experiences, let's say like Airbnb in

**44:50** · experiences, let's say like Airbnb in 2015

**44:51** · 2015 or Dropbox in 2013 or WeWork in 2019,

**44:55** · or Dropbox in 2013 or WeWork in 2019, you've been in these large organizations

**44:57** · you've been in these large organizations that most people listening to this

**44:59** · that most people listening to this podcast have been in where

**45:01** · podcast have been in where the PM traditionally never had access to

**45:04** · the PM traditionally never had access to get

**45:05** · get let alone like the amount we're showing

**45:07** · let alone like the amount we're showing here where they have a dev and agent

**45:08** · here where they have a dev and agent that is shipping front end and back end

**45:10** · that is shipping front end and back end features.

**45:12** · features. And you'd be surprised, even at

**45:13** · And you'd be surprised, even at companies like Adobe, PMs are still

**45:15** · companies like Adobe, PMs are still living in that world that you and I were

**45:17** · living in that world that you and I were in back then. They still don't have

**45:19** · in back then. They still don't have access. They're looking at what we've

**45:21** · access. They're looking at what we've just showed them and they're saying,

**45:23** · just showed them and they're saying, "Gosh, this is too far away from my

**45:25** · "Gosh, this is too far away from my reality.

**45:26** · reality. Is it true that like this just won't

**45:28** · Is it true that like this just won't work in certain type of companies or

**45:31** · work in certain type of companies or will they eventually get there?

**45:33** · will they eventually get there? It is just a matter of time."

**45:34** · It is just a matter of time." >> I'll start with the end, which is I do

**45:36** · >> I'll start with the end, which is I do think it is a matter of time that every

**45:37** · think it is a matter of time that every company is going to have to get there.

**45:40** · company is going to have to get there. You can't keep doing the same thing if

**45:42** · You can't keep doing the same thing if everyone else, including all your

**45:43** · everyone else, including all your competitors, are moving at 10 times the

**45:46** · competitors, are moving at 10 times the speed. So, I do think that there will be

**45:48** · speed. So, I do think that there will be pressure to ultimately get there for

**45:50** · pressure to ultimately get there for everyone. Now, what you want to be for

**45:53** · everyone. Now, what you want to be for the company and for the individual is

**45:55** · the company and for the individual is you want to be, um, as far, uh, you

**45:58** · you want to be, um, as far, uh, you know, as as advanced as it's

**46:00** · know, as as advanced as it's right, in that curve as opposed to just

**46:02** · right, in that curve as opposed to just waiting for it to happen to you. And

**46:04** · waiting for it to happen to you. And this is where I go back to, you know,

**46:06** · this is where I go back to, you know, the first step is just start small.

**46:08** · the first step is just start small. Start with one workflow that you are

**46:11** · Start with one workflow that you are doing. Um and or I really I really push

**46:14** · doing. Um and or I really I really push on this. I think this is really

**46:16** · on this. I think this is really uh a great way to to get your feet wet

**46:18** · uh a great way to to get your feet wet and and start to think about this. Go

**46:19** · and and start to think about this. Go find another team in your company

**46:21** · find another team in your company somewhere. And even if you're like, "I

**46:23** · somewhere. And even if you're like, "I I'm not quite ready to ship to

**46:24** · I'm not quite ready to ship to production for whatever reason." And

**46:26** · production for whatever reason." And usually the reasons are not that you

**46:28** · usually the reasons are not that you can't like you're not physically able

**46:30** · can't like you're not physically able to. It's usually something about the the

**46:33** · to. It's usually something about the the system or the process that it's not

**46:35** · system or the process that it's not quite there yet. But but let's just say

**46:37** · quite there yet. But but let's just say that you you don't feel like you can in

**46:38** · that you you don't feel like you can in the next month. Go somewhere else where

**46:42** · the next month. Go somewhere else where there's always somewhere in the org that

**46:43** · there's always somewhere in the org that is hungry for product thinking and

**46:46** · is hungry for product thinking and hungry for a tool to make their life

**46:48** · hungry for a tool to make their life better.

**46:49** · better. And I would start with let's just go

**46:51** · And I would start with let's just go build a tool for somebody in a different

**46:54** · build a tool for somebody in a different org to make their life better. And

**46:56** · org to make their life better. And simultaneously pick up one part of your

**46:58** · simultaneously pick up one part of your workflow that is taking you a lot of

**47:00** · workflow that is taking you a lot of time and there's really no reason that

**47:02** · time and there's really no reason that you should be doing that. Again, great

**47:04** · you should be doing that. Again, great examples. I'm getting into a customer

**47:05** · examples. I'm getting into a customer call.

**47:06** · call. I would love to be pre I would love to

**47:08** · I would love to be pre I would love to be prepped for that in a way that, you

**47:10** · be prepped for that in a way that, you know, an agent is serving me that

**47:12** · know, an agent is serving me that information as opposed to me having to

**47:14** · information as opposed to me having to pull from multiple different sources,

**47:15** · pull from multiple different sources, right? That's a very simple example. I

**47:17** · right? That's a very simple example. I write the same um

**47:19** · write the same um same email over and over again. It

**47:21** · same email over and over again. It should be auto-populated. Again, these

**47:23** · should be auto-populated. Again, these are just small small little automations.

**47:25** · are just small small little automations. Or you can call them templates. Whatever

**47:27** · Or you can call them templates. Whatever it is that you that um makes sense to

**47:29** · it is that you that um makes sense to you. Start there.

**47:31** · you. Start there. And then I would say if you're ready to

**47:33** · And then I would say if you're ready to take on something bigger, this idea of

**47:35** · take on something bigger, this idea of like, "What does a function do? Or what

**47:37** · like, "What does a function do? Or what is an end-to-end

**47:39** · is an end-to-end um operational journey look like?" And

**47:43** · um operational journey look like?" And there I would start to say map out your

**47:45** · there I would start to say map out your ontology or take your playbook and

**47:48** · ontology or take your playbook and really, you know, write that down. And

**47:50** · really, you know, write that down. And again, what I what I find really fun is

**47:53** · again, what I what I find really fun is like these playbooks, I think if someone

**47:55** · like these playbooks, I think if someone was tasked to write a playbook back in

**47:56** · was tasked to write a playbook back in the day, they'd be like, okay, I'll do

**47:58** · the day, they'd be like, okay, I'll do it. It'll take me a couple weeks. These

**48:00** · it. It'll take me a couple weeks. These playbooks can be written in an hour.

**48:03** · playbooks can be written in an hour. Actually, the first draft can be written

**48:04** · Actually, the first draft can be written in sub a minute, but to make it actually

**48:07** · in sub a minute, but to make it actually right and and you know, really

**48:09** · right and and you know, really reflective of your business, yeah, it

**48:10** · reflective of your business, yeah, it will take a little bit more time, but

**48:12** · will take a little bit more time, but we're talking hours here, maybe days

**48:14** · we're talking hours here, maybe days max. We're not talking weeks. And so, I

**48:16** · max. We're not talking weeks. And so, I think when you get a feel for how much

**48:19** · think when you get a feel for how much you can enable yourself and you can

**48:21** · you can enable yourself and you can enable others, you're going to create a

**48:23** · enable others, you're going to create a culture, again, even just going back to

**48:24** · culture, again, even just going back to culture change. You're going to create a

**48:26** · culture change. You're going to create a culture where um

**48:29** · culture where um it's celebrated and it's fun. And and

**48:31** · it's celebrated and it's fun. And and again, if you're leadership, what I'd

**48:32** · again, if you're leadership, what I'd really encourage you to do is make that

**48:34** · really encourage you to do is make that the culture. Celebrate those wins. Take

**48:37** · the culture. Celebrate those wins. Take the people who are your 1% and take

**48:40** · the people who are your 1% and take their workflows and figure out how to

**48:42** · their workflows and figure out how to scale that workflow to every single

**48:44** · scale that workflow to every single person on the team. When you create that

**48:46** · person on the team. When you create that um expectation and you celebrate those

**48:49** · um expectation and you celebrate those wins, you'll get more and more of that

**48:50** · wins, you'll get more and more of that behavior.

**48:51** · behavior. >> For you guys, did it happen as a

**48:53** · >> For you guys, did it happen as a transformation? Were you guys always

**48:55** · transformation? Were you guys always this way? Did it start with the CEO and

**48:57** · this way? Did it start with the CEO and the founder? How did it come about so

**48:59** · the founder? How did it come about so that now you guys do feel the confidence

**49:01** · that now you guys do feel the confidence that you have this enablement playbook

**49:03** · that you have this enablement playbook of Devin where anyone can ship to

**49:04** · of Devin where anyone can ship to production?

**49:05** · production? >> Yeah.

**49:06** · >> Yeah. Um I think there were a lot of pieces,

**49:08** · Um I think there were a lot of pieces, but I'll highlight the pieces that I

**49:09** · but I'll highlight the pieces that I think are most relevant that someone

**49:11** · think are most relevant that someone listening to this could take and and

**49:12** · listening to this could take and and replicate. Um the first piece I've

**49:15** · replicate. Um the first piece I've already shared, which is the idea of

**49:16** · already shared, which is the idea of just doing a hackathon. And in the

**49:18** · just doing a hackathon. And in the hackathon um making everyone participate

**49:21** · hackathon um making everyone participate cuz it changes this idea of you have to

**49:23** · cuz it changes this idea of you have to be technical to build something. But and

**49:25** · be technical to build something. But and and and again, I think most people have

**49:27** · and and again, I think most people have done that. Um so, I would expect that,

**49:30** · done that. Um so, I would expect that, you know, 90% of the people listening

**49:31** · you know, 90% of the people listening have participated in some kind of

**49:33** · have participated in some kind of hackathon. If you have not, that's the

**49:35** · hackathon. If you have not, that's the first step. Um the second step is to

**49:38** · first step. Um the second step is to really think about all the different

**49:41** · really think about all the different ways you can again, automate the

**49:43** · ways you can again, automate the workflow. I think that a structural

**49:45** · workflow. I think that a structural thing that I would really recommend is

**49:48** · thing that I would really recommend is actually making this idea of playing

**49:52** · actually making this idea of playing with AI tooling, creating workflows,

**49:55** · with AI tooling, creating workflows, automating, you know, large swaths of

**49:57** · automating, you know, large swaths of somebody's day in a way that makes them

**49:59** · somebody's day in a way that makes them much more productive, make that the

**50:02** · much more productive, make that the actual charter and mandate of a full of

**50:04** · actual charter and mandate of a full of a person full-time. And what I really

**50:06** · a person full-time. And what I really find is a lot of times when you say it's

**50:08** · find is a lot of times when you say it's everyone's responsibility, it's no one's

**50:10** · everyone's responsibility, it's no one's responsibility. And so what we have at

**50:12** · responsibility. And so what we have at Laurel is we actually have an AI

**50:14** · Laurel is we actually have an AI operations team. And to me AI ops is a

**50:17** · operations team. And to me AI ops is a new biz ops. Before biz ops, they were

**50:19** · new biz ops. Before biz ops, they were doing I'm really meaningful things, but

**50:22** · doing I'm really meaningful things, but often it was it was very

**50:24** · often it was it was very high-level, all the different hats, a

**50:26** · high-level, all the different hats, a lot of like market level stuff. Now if

**50:29** · lot of like market level stuff. Now if you repurpose this idea of having biz

**50:30** · you repurpose this idea of having biz ops, which is really again a Swiss Army

**50:32** · ops, which is really again a Swiss Army knife in many ways, to finding people

**50:36** · knife in many ways, to finding people who are insanely curious, tinkering with

**50:38** · who are insanely curious, tinkering with the latest technology, and relentless

**50:41** · the latest technology, and relentless about finding efficiencies, that's the

**50:43** · about finding efficiencies, that's the DNA I really look for. And so we've

**50:45** · DNA I really look for. And so we've actually built out an AI operations

**50:47** · actually built out an AI operations team. We started with Sasha,

**50:50** · team. We started with Sasha, who has built out a lot of the things

**50:52** · who has built out a lot of the things that I've I've shown today.

**50:54** · that I've I've shown today. And what he did is basically was like,

**50:56** · And what he did is basically was like, I'm going to demonstrate value in having

**50:58** · I'm going to demonstrate value in having AI operations. And very soon when you

**51:00** · AI operations. And very soon when you when you have one person who's doing an

**51:02** · when you have one person who's doing an excellent job, every single other

**51:04** · excellent job, every single other function is like, I want my Sasha.

**51:06** · function is like, I want my Sasha. I want my own AI Sasha. And that is how

**51:08** · I want my own AI Sasha. And that is how you then get the buy-in to say, okay,

**51:10** · you then get the buy-in to say, okay, well maybe we have an AI person AI

**51:13** · well maybe we have an AI person AI operations person just doing

**51:14** · operations person just doing go-to-market, and a separate AI

**51:16** · go-to-market, and a separate AI operations person just doing product,

**51:18** · operations person just doing product, and a separate AI operations person just

**51:20** · and a separate AI operations person just doing finance. Because all of these

**51:22** · doing finance. Because all of these functions, by the way, finance, rev ops,

**51:25** · functions, by the way, finance, rev ops, product ops, research ops, you name it,

**51:28** · product ops, research ops, you name it, all of them are changing so

**51:29** · all of them are changing so dramatically. And so being able to

**51:31** · dramatically. And so being able to retool your the way that your company

**51:34** · retool your the way that your company works with someone who's really

**51:36** · works with someone who's really dedicated to pushing that forward really

**51:38** · dedicated to pushing that forward really really accelerates the the journey.

**51:40** · really accelerates the the journey. >> Mhm. That's really interesting. And you

**51:42** · >> Mhm. That's really interesting. And you guys were founded before the AI

**51:44** · guys were founded before the AI revolution. So

**51:46** · revolution. So I guess like for other companies that

**51:48** · I guess like for other companies that were founded before then, I think you

**51:49** · were founded before then, I think you were 2018, like where

**51:53** · were 2018, like where who is like the right driver? It feels

**51:55** · who is like the right driver? It feels to me like it probably has to start like

**51:56** · to me like it probably has to start like literally with the CEO, right?

**51:58** · literally with the CEO, right? >> Yeah, I was going to say I want to give

**51:59** · >> Yeah, I was going to say I want to give a ton of credit to Ryan. So, yes, um

**52:02** · a ton of credit to Ryan. So, yes, um Laurel um was founded actually I would

**52:04** · Laurel um was founded actually I would say Time by Ping, this is what Laurel

**52:06** · say Time by Ping, this is what Laurel was called uh previously, was founded in

**52:07** · was called uh previously, was founded in 2018. Um but Ryan actually had the the

**52:11** · 2018. Um but Ryan actually had the the foresight and and the the courage really

**52:14** · foresight and and the the courage really to say, you know what? When I think

**52:15** · to say, you know what? When I think about what time looks like in a world of

**52:19** · about what time looks like in a world of AI and LLMs, it's very different. And

**52:21** · AI and LLMs, it's very different. And when I think about um at the time our

**52:23** · when I think about um at the time our core product um timekeeping, right? Like

**52:26** · core product um timekeeping, right? Like what does timekeeping look like in a

**52:27** · what does timekeeping look like in a world that um where you have to kind of

**52:30** · world that um where you have to kind of enter it manually or just do it through

**52:32** · enter it manually or just do it through call it what I call integrations um

**52:34** · call it what I call integrations um versus a world where you can actually

**52:36** · versus a world where you can actually start to really see everything that's

**52:38** · start to really see everything that's happening on your computer and

**52:39** · happening on your computer and synthesize that and run that through an

**52:41** · synthesize that and run that through an LLM. Like he basically had the foresight

**52:43** · LLM. Like he basically had the foresight and again courage to say, I'm going to

**52:46** · and again courage to say, I'm going to re-architect my entire product, my

**52:49** · re-architect my entire product, my entire company to be AI native. And so

**52:52** · entire company to be AI native. And so it's it's really interesting. Like I

**52:54** · it's it's really interesting. Like I really believe that um and I experience

**52:56** · really believe that um and I experience this day to day. Um I wouldn't you know,

**52:58** · this day to day. Um I wouldn't you know, like I I I was like I I I want to be

**53:00** · like I I I was like I I I want to be building at the cutting edge. Um

**53:03** · building at the cutting edge. Um Laurel is AI native.

**53:05** · Laurel is AI native. Although it was founded like more than 3

**53:08** · Although it was founded like more than 3 years ago. Um and so that it does start

**53:10** · years ago. Um and so that it does start with the CEO. Um but even if it if uh

**53:14** · with the CEO. Um but even if it if uh people don't have that degree of change

**53:17** · people don't have that degree of change um

**53:17** · um and and conviction, I think you can

**53:19** · and and conviction, I think you can still do it at every single level where,

**53:21** · still do it at every single level where, you know, if you are not the CEO, but

**53:23** · you know, if you are not the CEO, but you're uh an executive, you can say,

**53:25** · you're uh an executive, you can say, well, this is how I expect my function

**53:27** · well, this is how I expect my function to really operate. Here in my function,

**53:30** · to really operate. Here in my function, I am a marketing leader. I fully expect

**53:32** · I am a marketing leader. I fully expect that this is what we are doing and let

**53:35** · that this is what we are doing and let me go color code everything in here that

**53:38** · me go color code everything in here that should be AI enabled, right? Like when

**53:39** · should be AI enabled, right? Like when you think about copywriting today, you

**53:41** · you think about copywriting today, you should not be writing copy by hand. You

**53:43** · should not be writing copy by hand. You should be editing when you're doing

**53:44** · should be editing when you're doing videos. Like if you're not using um a

**53:47** · videos. Like if you're not using um a lot of the AI tooling out there, you're

**53:49** · lot of the AI tooling out there, you're spending a lot of money on studio, on

**53:51** · spending a lot of money on studio, on video in a way that you don't need to

**53:53** · video in a way that you don't need to anymore. So, being able to go line by

**53:55** · anymore. So, being able to go line by line in terms of your again your your

**53:58** · line in terms of your again your your work map. What is it that all my humans

**54:01** · work map. What is it that all my humans do and how do I really think about where

**54:03** · do and how do I really think about where do I need to keep that person versus

**54:05** · do I need to keep that person versus where can I actually really AI charge

**54:07** · where can I actually really AI charge supercharge them?

**54:08** · supercharge them? >> Amazing. So, I think that's the key

**54:11** · >> Amazing. So, I think that's the key point for a lot of people that I talk to

**54:13** · point for a lot of people that I talk to at least is that they have they don't

**54:15** · at least is that they have they don't have any access to the stuff we're

**54:17** · have any access to the stuff we're showing and probably it needs to start

**54:19** · showing and probably it needs to start like all the way at the CEO level and

**54:22** · like all the way at the CEO level and then it can work its way down where like

**54:24** · then it can work its way down where like you need really amazing CPO like

**54:26** · you need really amazing CPO like yourself who is also AI filled in order

**54:28** · yourself who is also AI filled in order to make this happen and that's kind of

**54:30** · to make this happen and that's kind of the next layer I want to talk about is

**54:33** · the next layer I want to talk about is as an AI filled CPO, what is your take

**54:36** · as an AI filled CPO, what is your take on the types of product teams we're

**54:38** · on the types of product teams we're going to see in the future? What types

**54:40** · going to see in the future? What types of product managers are you hiring and

**54:43** · of product managers are you hiring and what is the shape of their role today?

**54:45** · what is the shape of their role today? >> I think for many people, um I'm sure

**54:47** · >> I think for many people, um I'm sure this is dialogue that's happening

**54:48** · this is dialogue that's happening everywhere. This idea of are you a

**54:50** · everywhere. This idea of are you a product manager or you're just a product

**54:52** · product manager or you're just a product builder? And how many people are product

**54:55** · builder? And how many people are product builders? Meaning is it just the product

**54:58** · builders? Meaning is it just the product person themselves by functional title or

**55:01** · person themselves by functional title or is it also the designer? Is it also the

**55:03** · is it also the designer? Is it also the engineer? Um I'm a big believer of the

**55:05** · engineer? Um I'm a big believer of the fact that I think everyone should be a

**55:07** · fact that I think everyone should be a product builder. It goes back to my um

**55:10** · product builder. It goes back to my um uh how we operate the team today with

**55:12** · uh how we operate the team today with captains and taking features end to end.

**55:14** · captains and taking features end to end. Um what I do look for specifically in in

**55:16** · Um what I do look for specifically in in product uh builders who are product

**55:19** · product uh builders who are product managers by training, um I look for a

**55:22** · managers by training, um I look for a couple of things. Um I found that uh if

**55:25** · couple of things. Um I found that uh if you're incredibly senior in the sense

**55:27** · you're incredibly senior in the sense that you have the judgment, you've gone

**55:29** · that you have the judgment, you've gone through the hellfire, you've shipped

**55:31** · through the hellfire, you've shipped things that haven't worked and I think

**55:33** · things that haven't worked and I think for all of us that have shipped things,

**55:35** · for all of us that have shipped things, most of the time it doesn't work in the

**55:36** · most of the time it doesn't work in the first go around.

**55:38** · first go around. If you have if you kind of have that

**55:40** · If you have if you kind of have that battle-tested judgment, I'm finding that

**55:42** · battle-tested judgment, I'm finding that the combination of that experience plus

**55:45** · the combination of that experience plus this intense curiosity, this desire to

**55:47** · this intense curiosity, this desire to be hands-on, I think you see

**55:49** · be hands-on, I think you see a little bit of a bifurcation. There are

**55:50** · a little bit of a bifurcation. There are a lot of people who are very experienced

**55:52** · a lot of people who are very experienced and almost scared that their job is

**55:54** · and almost scared that their job is changing and um they're feeling more

**55:58** · changing and um they're feeling more fear than I would say excitement. And I

**56:00** · fear than I would say excitement. And I would say that there's another group of

**56:01** · would say that there's another group of people who are very experienced and

**56:03** · people who are very experienced and they've been they've never been more

**56:05** · they've been they've never been more excited. Like I I've never been more

**56:07** · excited. Like I I've never been more excited by the way to

**56:08** · excited by the way to not be doing all these things I used to

**56:10** · not be doing all these things I used to do in the past that took me forever that

**56:12** · do in the past that took me forever that there was no part of me that wanted to

**56:13** · there was no part of me that wanted to be doing that. Instead, I love, you

**56:16** · be doing that. Instead, I love, you know, actually like shaping a product,

**56:18** · know, actually like shaping a product, really getting hands-on. Um and then so

**56:22** · really getting hands-on. Um and then so so being able to find those people who

**56:24** · so being able to find those people who are excited, who are curious, but yet

**56:26** · are excited, who are curious, but yet have the the judgment and the reps is

**56:28** · have the the judgment and the reps is really really important. And so again,

**56:31** · really really important. And so again, um this is not necessarily by design,

**56:32** · um this is not necessarily by design, but what I found really interesting was

**56:35** · but what I found really interesting was you know, there are a number of people

**56:36** · you know, there are a number of people who previously were, you know, CPOs, VP

**56:39** · who previously were, you know, CPOs, VP of products, head of products. They've

**56:40** · of products, head of products. They've come in and they they're the ones

**56:42** · come in and they they're the ones building end-to-end. They're the ones

**56:43** · building end-to-end. They're the ones shipping end-to-end. Um and again,

**56:45** · shipping end-to-end. Um and again, they've never been more excited. They've

**56:47** · they've never been more excited. They've never been more excited to not have a

**56:51** · never been more excited to not have a team to have to manage because they

**56:52** · team to have to manage because they realize that a lot of that is just

**56:54** · realize that a lot of that is just overhead. A lot of that is just coord-

**56:56** · overhead. A lot of that is just coord- coordinate coordination cost. They've

**56:58** · coordinate coordination cost. They've realized that a lot of it is just

**57:00** · realized that a lot of it is just coordination cost and instead they can

**57:02** · coordination cost and instead they can just be um enabled to get right in there

**57:05** · just be um enabled to get right in there and drive the change they want to see.

**57:07** · and drive the change they want to see. >> That's crazy. So you have embraced the

**57:09** · >> That's crazy. So you have embraced the super senior ICPM. I think you said

**57:12** · super senior ICPM. I think you said something pretty crazy actually when we

**57:14** · something pretty crazy actually when we were talking before which was

**57:16** · were talking before which was the more senior you get, the longer

**57:18** · the more senior you get, the longer you've been in product, the smaller your

**57:20** · you've been in product, the smaller your orgs have become. Is that the trend of

**57:22** · orgs have become. Is that the trend of the future, smaller and smaller product

**57:24** · the future, smaller and smaller product orgs?

**57:25** · orgs? >> I think so. Yeah, I mean I've had

**57:26** · >> I think so. Yeah, I mean I've had hundreds of people and today I have five

**57:29** · hundreds of people and today I have five PMs and four designers and um there

**57:33** · PMs and four designers and um there isn't a real reason to grow that um

**57:37** · isn't a real reason to grow that um because again, like when you add more

**57:38** · because again, like when you add more people, you add more coordination costs.

**57:40** · people, you add more coordination costs. You actually um

**57:42** · You actually um it have a harder time making making

**57:44** · it have a harder time making making people feel like they are absolutely

**57:46** · people feel like they are absolutely responsible for taking something

**57:47** · responsible for taking something end-to-end. And so, I do think of that

**57:50** · end-to-end. And so, I do think of that as the future. I think that um the best

**57:52** · as the future. I think that um the best teams are going to be lean, but not so

**57:56** · teams are going to be lean, but not so lean that they're starved. And so, it's

**57:57** · lean that they're starved. And so, it's really important to find that line.

**57:59** · really important to find that line. >> So, you said you do something pretty

**58:01** · >> So, you said you do something pretty crazy in your interviews. Can you tell

**58:03** · crazy in your interviews. Can you tell me how you interview people um and

**58:05** · me how you interview people um and really find these gem AI pilled super

**58:08** · really find these gem AI pilled super senior ICPMs?

**58:10** · senior ICPMs? >> I think a lot of people are talking

**58:12** · >> I think a lot of people are talking about. Of course, you know, you do a

**58:13** · about. Of course, you know, you do a session where people have to build with

**58:14** · session where people have to build with AI. Um I I think that's all fine and um

**58:18** · AI. Um I I think that's all fine and um uh I think it makes a lot of sense to do

**58:20** · uh I think it makes a lot of sense to do that. Um it it takes cycles, by the way,

**58:22** · that. Um it it takes cycles, by the way, to even have a standardized interview

**58:24** · to even have a standardized interview loop. Um some companies it makes sense

**58:26** · loop. Um some companies it makes sense because they're large enough where

**58:27** · because they're large enough where they're hiring, you know, enough PMs.

**58:29** · they're hiring, you know, enough PMs. But again, I I do think many people are

**58:31** · But again, I I do think many people are saying, "Hey, let's actually get a

**58:32** · saying, "Hey, let's actually get a little bit more um particular about who

**58:35** · little bit more um particular about who we hire and make sure that they're

**58:36** · we hire and make sure that they're really seasoned. And we'd rather pay a

**58:38** · really seasoned. And we'd rather pay a few really seasoned people, you know, a

**58:40** · few really seasoned people, you know, a lot more than having just an army of

**58:42** · lot more than having just an army of people." And so, um what I've been

**58:44** · people." And so, um what I've been doing, and I I do this, by the way, for

**58:46** · doing, and I I do this, by the way, for every function, not just product or

**58:47** · every function, not just product or designer, so you know, so and so forth,

**58:50** · designer, so you know, so and so forth, um is I I do ask people to screen share.

**58:52** · um is I I do ask people to screen share. And what I found is it is so easy to

**58:55** · And what I found is it is so easy to say, "Hey, we are, you know, I'm AI

**58:58** · say, "Hey, we are, you know, I'm AI pilled, we're AI pilled, we do a bunch

**58:59** · pilled, we're AI pilled, we do a bunch of stuff with AI." But as soon as you

**59:01** · of stuff with AI." But as soon as you get into um like if you really peek

**59:03** · get into um like if you really peek under the hood, you're like, "Actually,

**59:05** · under the hood, you're like, "Actually, I think you're what I call like level

**59:07** · I think you're what I call like level one." And maybe I'll just take a moment

**59:08** · one." And maybe I'll just take a moment and talk about the levels for me. Level

**59:10** · and talk about the levels for me. Level one is you're talking to, you know,

**59:13** · one is you're talking to, you know, you're talking to ChatGPT, you're

**59:14** · you're talking to ChatGPT, you're talking to Claude. You're really using

**59:16** · talking to Claude. You're really using um AI kind of in a chat mode. Almost

**59:19** · um AI kind of in a chat mode. Almost like like search mode, right? Like I ask

**59:21** · like like search mode, right? Like I ask a question, you give me an answer. Level

**59:23** · a question, you give me an answer. Level two is where you start to automate a

**59:24** · two is where you start to automate a workflow, right? And this is what I was

**59:26** · workflow, right? And this is what I was showing earlier around just the first

**59:29** · showing earlier around just the first step is like start small. An OS does not

**59:32** · step is like start small. An OS does not start necessarily as an OS, but it

**59:33** · start necessarily as an OS, but it starts with a first

**59:35** · starts with a first um automation.

**59:36** · um automation. Right? A first little piece of workflow

**59:39** · Right? A first little piece of workflow that everyone's going to start doing.

**59:40** · that everyone's going to start doing. And so that's level two. Um level three

**59:43** · And so that's level two. Um level three is when you start building, you know,

**59:44** · is when you start building, you know, apps. Right? You say, "Hey, you know,

**59:46** · apps. Right? You say, "Hey, you know, it's really important that I um I'm I'm

**59:48** · it's really important that I um I'm I'm doing this thing. It's really tedious.

**59:50** · doing this thing. It's really tedious. I'm going to build an app to make it

**59:51** · I'm going to build an app to make it like less tedious." And then level four

**59:53** · like less tedious." And then level four I'd say is where you're actually

**59:55** · I'd say is where you're actually building I call it shared apps and or um

**59:57** · building I call it shared apps and or um if you really think about the product

**59:58** · if you really think about the product life cycle, you're you're really

**59:59** · life cycle, you're you're really shipping to your customers. And so those

**1:00:01** · shipping to your customers. And so those are the the maybe the four levels um

**1:00:04** · are the the maybe the four levels um that you can assess yourself on. You can

**1:00:06** · that you can assess yourself on. You can assess a given company on like which of

**1:00:08** · assess a given company on like which of those four levels is the majority of the

**1:00:10** · those four levels is the majority of the organization um

**1:00:12** · organization um operating at. And so um what I find is

**1:00:15** · operating at. And so um what I find is when you actually ask someone to screen

**1:00:17** · when you actually ask someone to screen share and show them how and show you how

**1:00:19** · share and show them how and show you how they AI, you're very you can very

**1:00:22** · they AI, you're very you can very quickly get a sense of

**1:00:24** · quickly get a sense of are you at level one? Are you basically

**1:00:26** · are you at level one? Are you basically just talking to chat GPT? Um or have you

**1:00:28** · just talking to chat GPT? Um or have you actually created um like a a some way to

**1:00:31** · actually created um like a a some way to really like scale yourself, some kind of

**1:00:33** · really like scale yourself, some kind of workflow, some kind of agent? Or are you

**1:00:35** · workflow, some kind of agent? Or are you starting to build like apps? And or, you

**1:00:38** · starting to build like apps? And or, you know, what are you shipping? Like truly

**1:00:39** · know, what are you shipping? Like truly truly shipping? And so really getting to

**1:00:41** · truly shipping? And so really getting to see that um live on screen is really

**1:00:45** · see that um live on screen is really really interesting because otherwise

**1:00:46** · really interesting because otherwise it's really easy just be like, "This is

**1:00:48** · it's really easy just be like, "This is what I do." And it's you know, pulled

**1:00:50** · what I do." And it's you know, pulled from LinkedIn or pulled from the latest

**1:00:51** · from LinkedIn or pulled from the latest thing you saw on the internet. Um but

**1:00:53** · thing you saw on the internet. Um but actually peeling it back and be like,

**1:00:54** · actually peeling it back and be like, "What is on your screen?" is is really

**1:00:57** · "What is on your screen?" is is really fascinating.

**1:00:58** · fascinating. >> Wow. People don't believe me when I keep

**1:01:00** · >> Wow. People don't believe me when I keep saying this is the new interview. This

**1:01:02** · saying this is the new interview. This is what I'm hearing. You've heard it

**1:01:04** · is what I'm hearing. You've heard it from a CPO herself. So,

**1:01:07** · from a CPO herself. So, a lot of people are feeling pretty bad

**1:01:09** · a lot of people are feeling pretty bad about this whole transition. Like there

**1:01:12** · about this whole transition. Like there there's a lot of FUD going around in the

**1:01:14** · there's a lot of FUD going around in the PM field. If you check out Reddit or

**1:01:16** · PM field. If you check out Reddit or something, people are feeling a lot very

**1:01:18** · something, people are feeling a lot very nervous about this change. They're

**1:01:20** · nervous about this change. They're saying, "Hey, we're compressing out the

**1:01:21** · saying, "Hey, we're compressing out the juniors."

**1:01:23** · juniors." You had a really interesting take on

**1:01:24** · You had a really interesting take on this, which is that

**1:01:26** · this, which is that the best PMs are actually getting more

**1:01:28** · the best PMs are actually getting more roles and the rest are feeling fear and

**1:01:30** · roles and the rest are feeling fear and destruction. Can you unpack that for us?

**1:01:32** · destruction. Can you unpack that for us? >> I think it's because one PM can do so

**1:01:34** · >> I think it's because one PM can do so much more than ever before, but there

**1:01:36** · much more than ever before, but there aren't that many of them who are that

**1:01:39** · aren't that many of them who are that skilled, that have that judgment, who

**1:01:41** · skilled, that have that judgment, who are AI pilled, um who fearlessly are

**1:01:43** · are AI pilled, um who fearlessly are going through all of these pieces and by

**1:01:46** · going through all of these pieces and by the way know that one of the most

**1:01:47** · the way know that one of the most important things forever and will never

**1:01:49** · important things forever and will never change about the PM role is that they

**1:01:50** · change about the PM role is that they have to stay close to their customers.

**1:01:52** · have to stay close to their customers. Right? So like the the Venn diagram of

**1:01:54** · Right? So like the the Venn diagram of all of those traits is not large in

**1:01:58** · all of those traits is not large in terms of the actual number of people

**1:01:59** · terms of the actual number of people that fall into that and that's what

**1:02:01** · that fall into that and that's what every company's going to want.

**1:02:03** · every company's going to want. And and around the edges it's like why

**1:02:05** · And and around the edges it's like why do I why would I go hire someone who is

**1:02:07** · do I why would I go hire someone who is not all of those things? I'm going to

**1:02:08** · not all of those things? I'm going to have to supplement them in some way and

**1:02:11** · have to supplement them in some way and it's going to create overhead.

**1:02:12** · it's going to create overhead. And then when when in in many ways I can

**1:02:14** · And then when when in in many ways I can take that piece that is not excellent

**1:02:16** · take that piece that is not excellent and I can build like, you know, again a

**1:02:18** · and I can build like, you know, again a workflow and agent around that. So I I

**1:02:20** · workflow and agent around that. So I I think it's really finding who I call the

**1:02:22** · think it's really finding who I call the orchestrators, right? The people who are

**1:02:25** · orchestrators, right? The people who are big picture in terms of their thinking,

**1:02:27** · big picture in terms of their thinking, but you know, down to the detail in

**1:02:29** · but you know, down to the detail in terms of terms of their execution. Those

**1:02:31** · terms of terms of their execution. Those are the people who are worth their

**1:02:32** · are the people who are worth their weight in gold and I think that a lot of

**1:02:34** · weight in gold and I think that a lot of people who need to be complemented by a

**1:02:37** · people who need to be complemented by a designer or complemented by an engineer

**1:02:39** · designer or complemented by an engineer or like you know, complemented by many

**1:02:41** · or like you know, complemented by many many many other people, it just doesn't

**1:02:42** · many many other people, it just doesn't make sense anymore because why go hire

**1:02:45** · make sense anymore because why go hire all these people when again one person

**1:02:47** · all these people when again one person can be the end-end builder.

**1:02:48** · can be the end-end builder. >> It's not me saying it's guys, it's her.

**1:02:51** · >> It's not me saying it's guys, it's her. I've been preaching this for months and

**1:02:52** · I've been preaching this for months and months.

**1:02:54** · months. This is the future of product

**1:02:56** · This is the future of product management. We just gave you

**1:02:58** · management. We just gave you the entire playbook. She just screen

**1:03:00** · the entire playbook. She just screen shared literally everything, the company

**1:03:02** · shared literally everything, the company OS, how their

**1:03:04** · OS, how their PMs are knocking down linear tickets. If

**1:03:07** · PMs are knocking down linear tickets. If you want a really amazing job, apply to

**1:03:09** · you want a really amazing job, apply to Laurel. Julie is not just doing this

**1:03:12** · Laurel. Julie is not just doing this though, right? You actually have so much

**1:03:15** · though, right? You actually have so much cool stuff going on. You teach product

**1:03:17** · cool stuff going on. You teach product management at Stanford.

**1:03:20** · management at Stanford. I think you had at some point have been

**1:03:21** · I think you had at some point have been involved with Reforge. Can you catch us

**1:03:23** · involved with Reforge. Can you catch us up outside of Laurel? What's the world

**1:03:25** · up outside of Laurel? What's the world of JZ? What's going on?

**1:03:28** · of JZ? What's going on? >> Um I do teach every year at Stanford. Um

**1:03:30** · >> Um I do teach every year at Stanford. Um I do it for the love of um really just

**1:03:34** · I do it for the love of um really just getting to meet the next generation of

**1:03:36** · getting to meet the next generation of of builders. Um I also get the really

**1:03:39** · of builders. Um I also get the really awesome benefit of meeting people like

**1:03:42** · awesome benefit of meeting people like the Sasha's of the world who, you know,

**1:03:44** · the Sasha's of the world who, you know, once took my class, then TA'd for me,

**1:03:46** · once took my class, then TA'd for me, and now is at Laurel. Um and uh you

**1:03:49** · and now is at Laurel. Um and uh you know, teaching for me has been a

**1:03:50** · know, teaching for me has been a combination of of passion and honestly

**1:03:52** · combination of of passion and honestly uh of pipeline. Um so I teach at

**1:03:54** · uh of pipeline. Um so I teach at Stanford, um I teach at Yale, and I

**1:03:56** · Stanford, um I teach at Yale, and I teach at Reforge. Um and it's it's just

**1:03:59** · teach at Reforge. Um and it's it's just how I think that when you teach

**1:04:00** · how I think that when you teach something, you have to know it like the

**1:04:02** · something, you have to know it like the back of your hand in order to actually

**1:04:05** · back of your hand in order to actually share that with someone else. Um so I I

**1:04:07** · share that with someone else. Um so I I again I just find this really funny. A

**1:04:09** · again I just find this really funny. A lot of times I'll teach and then I'll be

**1:04:10** · lot of times I'll teach and then I'll be like, "Ah, good reminder, JZ. Like uh

**1:04:13** · like, "Ah, good reminder, JZ. Like uh were you doing that today in your

**1:04:15** · were you doing that today in your day-to-day? Uh were you customer-centric

**1:04:17** · day-to-day? Uh were you customer-centric enough? Were you problem-space first and

**1:04:19** · enough? Were you problem-space first and not solution first enough?" And so I

**1:04:21** · not solution first enough?" And so I just find it both um so gratifying

**1:04:23** · just find it both um so gratifying personally, but also um such a great

**1:04:26** · personally, but also um such a great reminder of of what product really is.

**1:04:28** · reminder of of what product really is. And I'll I'll say one last thing, which

**1:04:29** · And I'll I'll say one last thing, which is

**1:04:30** · is what's funny is that

**1:04:32** · what's funny is that um so I I I teach AI leadership through

**1:04:35** · um so I I I teach AI leadership through Reforge, and that curriculum changes

**1:04:37** · Reforge, and that curriculum changes literally by the month. Um you know, we

**1:04:40** · literally by the month. Um you know, we teach it every 6 months, and the amount

**1:04:41** · teach it every 6 months, and the amount of change between the 6 months is

**1:04:42** · of change between the 6 months is massive. But when you actually teach the

**1:04:45** · massive. But when you actually teach the fundamentals, when you teach the what I

**1:04:47** · fundamentals, when you teach the what I call like PM 101, those core principles

**1:04:50** · call like PM 101, those core principles have not changed. You should still

**1:04:52** · have not changed. You should still always never jump to the solution. And

**1:04:54** · always never jump to the solution. And now that you can build faster than ever

**1:04:56** · now that you can build faster than ever before, it doesn't mean you just build

**1:04:57** · before, it doesn't mean you just build everything. Like what actually is

**1:04:59** · everything. Like what actually is important is to know why and for whom

**1:05:02** · important is to know why and for whom you're building for, and what is it that

**1:05:03** · you're building for, and what is it that you're trying to solve for, and what

**1:05:04** · you're trying to solve for, and what success looks like, and therefore you

**1:05:06** · success looks like, and therefore you actually know you've hit your target.

**1:05:08** · actually know you've hit your target. And so what's really ironic is that

**1:05:11** · And so what's really ironic is that through teaching all these different

**1:05:12** · through teaching all these different levels of of product people over the

**1:05:14** · levels of of product people over the years, I find that the the fundamentals

**1:05:17** · years, I find that the the fundamentals and the principles have never changed.

**1:05:20** · and the principles have never changed. In fact, they're even more important

**1:05:22** · In fact, they're even more important than ever before, but the tools and the

**1:05:24** · than ever before, but the tools and the way you operate and the way you

**1:05:26** · way you operate and the way you can blast through the bureaucracy and

**1:05:28** · can blast through the bureaucracy and feel empowered, that's radically

**1:05:30** · feel empowered, that's radically changed. And so as a as a leader, the

**1:05:32** · changed. And so as a as a leader, the way you empower your team is very

**1:05:34** · way you empower your team is very different. Do you have the right

**1:05:37** · different. Do you have the right culture? Do you have the right team? Do

**1:05:40** · culture? Do you have the right team? Do you have the right space for people to

**1:05:42** · you have the right space for people to even build? Do you have the right

**1:05:44** · even build? Do you have the right operating system? Do you have the right

**1:05:46** · operating system? Do you have the right knowledge of what people are doing

**1:05:48** · knowledge of what people are doing day-to-day? Do you have all of those

**1:05:50** · day-to-day? Do you have all of those pieces? That is changing dramatically,

**1:05:52** · pieces? That is changing dramatically, but in your actual, you know, one on one

**1:05:55** · but in your actual, you know, one on one on one basics around what it is that a

**1:05:57** · on one basics around what it is that a product person is supposed to be doing,

**1:06:00** · product person is supposed to be doing, um

**1:06:01** · um the speed has changed dramatically, but

**1:06:03** · the speed has changed dramatically, but what you're supposed to be doing at the

**1:06:04** · what you're supposed to be doing at the heart of it, that has not changed.

**1:06:06** · heart of it, that has not changed. >> What a way to end it. All right, guys,

**1:06:08** · >> What a way to end it. All right, guys, we have hit a crazy milestone when we

**1:06:10** · we have hit a crazy milestone when we crossed 40,000 YouTube subscribers. We

**1:06:12** · crossed 40,000 YouTube subscribers. We have also crossed 565,000

**1:06:15** · have also crossed 565,000 average views per listen per episode.

**1:06:17** · average views per listen per episode. When I started this podcast 2 years ago,

**1:06:19** · When I started this podcast 2 years ago, I wouldn't have believed it. I want all

**1:06:21** · I wouldn't have believed it. I want all 565,000

**1:06:22** · 565,000 of you to flood Laurel's PM

**1:06:25** · of you to flood Laurel's PM applications. For my money, this is like

**1:06:27** · applications. For my money, this is like the coolest PM job you could possibly

**1:06:30** · the coolest PM job you could possibly have. And I would say if you are in a PM

**1:06:32** · have. And I would say if you are in a PM job where everything we were just

**1:06:34** · job where everything we were just talking about feels really foreign and

**1:06:36** · talking about feels really foreign and like 10 steps away from what you are,

**1:06:39** · like 10 steps away from what you are, find a job like this with an AI PM CPO

**1:06:43** · find a job like this with an AI PM CPO like JZ. You are going to learn so much

**1:06:46** · like JZ. You are going to learn so much more than if you get to this 4 years

**1:06:48** · more than if you get to this 4 years from now and then you learn it. Apply to

**1:06:50** · from now and then you learn it. Apply to Laurel, get her the best AI PMs in the

**1:06:52** · Laurel, get her the best AI PMs in the world. Check out her class at Stanford

**1:06:55** · world. Check out her class at Stanford if you are in the Bay Area so you can

**1:06:57** · if you are in the Bay Area so you can really learn AI PM. And if you are a

**1:06:59** · really learn AI PM. And if you are a leader, check out her course at Reforge.

**1:07:01** · leader, check out her course at Reforge. This is just me saying this. You can see

**1:07:03** · This is just me saying this. You can see how much value I got out of this

**1:07:04** · how much value I got out of this episode. You can see I'll be writing

**1:07:06** · episode. You can see I'll be writing about a company OS soon in my

**1:07:08** · about a company OS soon in my newsletter.

**1:07:09** · newsletter. Jazy has absolutely killed it. Thank you

**1:07:11** · Jazy has absolutely killed it. Thank you so much, Jazy.

**1:07:12** · so much, Jazy. >> Thanks for having me.

**1:07:13** · >> Thanks for having me. >> I hope you enjoyed that episode. If you

**1:07:15** · >> I hope you enjoyed that episode. If you could take a moment to double-check that

**1:07:16** · could take a moment to double-check that you have followed on Apple and Spotify

**1:07:18** · you have followed on Apple and Spotify podcasts, subscribed on YouTube, left a

**1:07:20** · podcasts, subscribed on YouTube, left a rating or review on Apple or Spotify,

**1:07:22** · rating or review on Apple or Spotify, and commented on YouTube, all these

**1:07:25** · and commented on YouTube, all these things will help the algorithm

**1:07:26** · things will help the algorithm distribute the show to more and more

**1:07:28** · distribute the show to more and more people. As we distribute the show to

**1:07:30** · people. As we distribute the show to more people, we can grow the show,

**1:07:32** · more people, we can grow the show, improve the quality of the content and

**1:07:33** · improve the quality of the content and the production to get you better

**1:07:35** · the production to get you better insights to stay ahead in your career.

**1:07:37** · insights to stay ahead in your career. Finally, do check out my bundle at

**1:07:40** · Finally, do check out my bundle at bundle.akashsharma.com

**1:07:41** · bundle.akashsharma.com to get access to nine AI products for an

**1:07:44** · to get access to nine AI products for an entire year for free. This includes

**1:07:47** · entire year for free. This includes Dovetail, Mobbin, Linear, Reforge,

**1:07:49** · Dovetail, Mobbin, Linear, Reforge, Build, Descript, and many other amazing

**1:07:52** · Build, Descript, and many other amazing tools that will help you as an AI

**1:07:55** · tools that will help you as an AI product manager or builder succeed. I'll

**1:07:57** · product manager or builder succeed. I'll see you in the next episode.
