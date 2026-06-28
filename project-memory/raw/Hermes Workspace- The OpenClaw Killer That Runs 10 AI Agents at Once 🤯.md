---
title: "Hermes Workspace: The OpenClaw Killer That Runs 10 AI Agents at Once 🤯"
source: "https://www.youtube.com/watch?v=9kbzwtFhrzw"
author:
  - "[[The AI Doctor]]"
published: 2026-05-13
created: 2026-06-28
description: "🔗 HERMES (coupon: GOHERMESAI): https://www.hostinger.fr/gohermesai  🔗 Documentation: https://automatisation.notion.site/Hermes-Workspace-II-35e3d6550fd980e5acd2ca27404d1447  🚀 Herm..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=9kbzwtFhrzw)

🔗 HERMES (coupon: GOHERMESAI): https://www.hostinger.fr/gohermesai

🔗 Documentation: https://automatisation.notion.site/Hermes-Workspace-II-35e3d6550fd980e5acd2ca27404d1447

🚀 Hermes Workspace lets you build your own AI agent team that works 24/7 on your private VPS.

In this quick tutorial, I’ll show you how to install and use Hermes Workspace, a powerful AI orchestration platform that lets you run a real team of autonomous AI agents on your own server.

No more expensive monthly subscriptions. With Hermes Workspace + a Claude API key, you can create your own AI infrastructure running continuously, 24/7.

In this video, you’ll learn how to install Hermes Workspace step by step, configure your first AI agent team, understand the difference between Operations and Swarm, and explore the 4 powerful modes: Profiles, Operations, Swarm, and Conductor.

Whether you’re an entrepreneur, developer, content creator, or AI enthusiast, Hermes Workspace can help you automate complex tasks using specialized AI agents that collaborate together.

✅ What You’ll Learn
How to choose the right VPS to host Hermes Workspace
Full step-by-step installation with your Claude API key
How to use the 4 main modes: Profiles, Operations, Swarm, and Conductor
The difference between Operations and Swarm
How to configure your first custom AI agent team
How to fix common issues like the permission-related error 500
⏱ Chapters

00:00 - Intro: Why Hermes Workspace can change the way you work
02:01 - Choosing the right VPS to host Hermes Workspace
04:35 - Step-by-step Hermes Workspace installation with Claude API
06:05 - First login and interface overview
10:25 - Profiles explained: the foundation of every Hermes setup
12:23 - Operations vs Swarm: which AI agent team should you use?
16:02 - Full Hermes dashboard tour: the 4 modes explained
18:13 - What Hermes case study should I build next?

#HermesWorkspace #AIAgents #ClaudeAI

## Transcript

_Caption track: English auto-generated or provided._

**0:00** · It's official today. Hermes agent is

**0:02** · ranked the number one agent in the world

**0:04** · according to Open Router. This was

**0:07** · shared by the company that created

**0:09** · Hermes and it really shows the power of

**0:11** · this tool.

**0:12** · So this discovery, or rather this news,

**0:15** · comes because today, thanks to Hermes

**0:17** · agent, they have created what is called

**0:19** · a management interface.

**0:21** · So the interface is called Hermes

**0:23** · Workspace. It's the one that actually

**0:25** · shows you the agent, the agents you've

**0:27** · created, and above all, it allows me to

**0:29** · create what are called profiles. It's

**0:31** · like on a computer where you have

**0:32** · multiple user sessions. So I wanted to

**0:35** · make a video where I show you how I

**0:37** · installed this installation directly

**0:39** · into Hermes Workspace in a simple way,

**0:41** · as simply as possible, without having to

**0:43** · type in lines of code, and we'll just

**0:45** · try to understand a little bit about

**0:47** · this new interface where I can see the

**0:49** · tasks to create the sessions and the

**0:52** · communications between myself and

**0:54** · Hermes. This is truly a very easy to use

**0:56** · interface. So this one is the reference.

**0:59** · So there you go, they just released this

**1:01** · update. It's actually only been 5 days

**1:04** · since this interface was officially

**1:05** · added to Hermes and we're going to

**1:07** · install it directly. We're not going to

**1:09** · install Hermes and then add the

**1:11** · interface. We'll do it directly with

**1:12** · Hermes Workspace.

**1:14** · With a simple installation, we'll have

**1:16** · access to everything.

**1:17** · So in the course, we'll start by

**1:19** · understanding the architecture. This is

**1:21** · very important and of course I'll

**1:22** · provide you with my course materials

**1:25** · where I'll include all the links and

**1:26** · details that I'll be using in this

**1:28** · training. You'll find the documentation

**1:30** · in the description of this video.

**1:33** · You'll also receive it by email, so just

**1:35** · open the link and you're good to go.

**1:38** · We're going to start working on this

**1:39** · intelligence right away. Hermes is the

**1:42** · number one agent in the world.

**1:44** · So the first step is to install Hermes

**1:46** · on an external VPS.

**1:48** · You need to be very careful. Hermes is

**1:50** · still a dangerous agent, just like Open

**1:52** · Cloud or other agents, even Paperclip.

**1:55** · Why? Because these kinds of agents

**1:57** · actually have access to your hard drive.

**1:59** · And if there's what's called prompt

**2:01** · injection, someone could actually

**2:02** · retrieve your photos, videos, or even

**2:04** · your passwords.

**2:06** · That's why we install Hermes on a VPS

**2:08** · like here. I'm putting it on Hostinger.

**2:10** · So, as a result, there are neither my

**2:11** · data nor my files on this VPS server.

**2:14** · And that's extremely important. Never

**2:16** · install Hermes or any AI agent on your

**2:18** · own machine.

**2:19** · So, here I'm choosing the KVM 2 plan,

**2:22** · which gives me two processors with 8 GB

**2:24** · of RAM. It's a very good processor. It's

**2:27** · powerful. And as for the RAM, 8 GB lets

**2:29** · me actually run daily tasks smoothly.

**2:32** · So, if you're a business or a

**2:33** · freelancer, you need to have at least 8

**2:35** · GB of RAM.

**2:37** · Also, be careful. You need to be on this

**2:40** · specific page. I'll leave the link to

**2:42** · this page in the description because

**2:43** · there are two types of Hermes

**2:45** · installations.

**2:46** · There's the Hermes workspace and the

**2:48** · classic Hermes agent. The one I'm

**2:50** · interested in right now isn't that one.

**2:52** · It's the workspace version. I'll leave

**2:54** · you the link.

**2:55** · This one will simply give me access to

**2:57** · this interface.

**2:59** · The other one will give me a classic

**3:00** · interface, not the workspace.

**3:03** · So, once I'm here, I'll simply click

**3:04** · here to deploy.

**3:07** · And here, I'm actually going to use a

**3:08** · coupon that was posted on Hostinger's

**3:10** · blog.

**3:12** · So, the coupon will give me a discount.

**3:14** · And in order to use it, I had to be a

**3:16** · first-time customer on Hostinger. So,

**3:19** · quite simply, here I'm going to log out

**3:22** · of my old account because I'm going to

**3:24** · use another email address so that for

**3:26** · Hostinger, I'm considered a new

**3:29** · customer. So, that's the trick to make

**3:30** · the coupon work. So, now I'm going to

**3:33** · enter the coupon, which is gohermesai.

**3:35** · There you go.

**3:37** · Take note of it. With this coupon, when

**3:39** · I click on apply, it will automatically

**3:41** · give me a 10% discount.

**3:44** · Of course, I actually have a 30-day

**3:45** · trial period. That's something really

**3:47** · interesting about Hostinger. So, you can

**3:49** · go ahead and do the installation, set up

**3:51** · the system, and everything. You have 30

**3:53** · days to test it out, which is basically

**3:55** · free.

**3:56** · And after that, I choose the location of

**3:58** · my server. I choose France, and I simply

**4:01** · click on continue to receive or generate

**4:03** · my password and enter my cloud API. So

**4:06** · here, I just click on continue.

**4:09** · So the first thing to do is to save this

**4:10** · password. This is our password that will

**4:13** · allow us to access the Hermes work space

**4:15** · interface later on. So we need to save

**4:17** · this password in a secure place.

**4:19** · Next, we actually need to provide an API

**4:22** · to our system, an LLM API, which acts

**4:25** · like the brain.

**4:26** · It's thanks to this system that Hermes

**4:28** · can think and actually carry out tasks.

**4:31** · So you'll see there are actually several

**4:32** · LLMs available. There's Mistral, Grok,

**4:35** · Google, OpenRouter, and also those from

**4:37** · Anthropic and OpenAI. So for me, I use

**4:40** · the one from Anthropic.

**4:42** · And how do you do it, or how do you get

**4:44** · your code? It's simple. You go to

**4:46** · Google, type in Cloud Platform, and

**4:48** · click on the first link.

**4:50** · This link allows you to actually create

**4:52** · what are called APIs. So here, I click

**4:54** · on create API.

**4:57** · For example, I'll just call it Hermes

**4:59** · like this, and I click on add, because

**5:01** · when I click on add, it will add or

**5:03** · create generate the key for me.

**5:05** · Of course, the key is actually secret,

**5:07** · it's important, and you shouldn't share

**5:09** · it. You should also store it in a secure

**5:11** · place.

**5:12** · So here, I'm going to create it,

**5:14** · generate it.

**5:15** · Then I'll simply place my key right

**5:17** · here. There you go. So we place the key,

**5:20** · and all we have to do is simply click on

**5:21** · next to actually confirm this

**5:23** · installation. And there you have it.

**5:25** · Hermes is now installed on my server,

**5:27** · which is Hostinger. All I have to do,

**5:29** · you'll see here that there's actually

**5:31** · the option to open and launch the

**5:32** · system. We have a small button to open

**5:34** · it and a button to go to the terminal.

**5:36** · So if I click open, you'll see that it

**5:38** · tells me you need to validate the

**5:40** · connection. That's completely normal,

**5:42** · because here, our URL isn't HTTPS.

**5:46** · So there's no problem, don't worry. You

**5:47** · just click here to allow access to this

**5:49** · site because it's not a dangerous site.

**5:51** · It's your own website.

**5:53** · So, now Hermes is loading. We're going

**5:55** · to increase the size a bit. And now it's

**5:58** · asking me for the password.

**6:00** · So, I enter the password we created

**6:01** · together and click continue.

**6:04** · Now, the system is creating my

**6:05** · workspace.

**6:06** · Here, there's a step to connect the back

**6:08** · end. So, I confirm it.

**6:11** · And now, quite simply, we're just going

**6:13** · to click continue.

**6:15** · Here, it's actually giving me the back

**6:17** · end URL. Now, I press continue here.

**6:20** · So, here there's an important step to

**6:22** · select the model. For us, we're going to

**6:24** · choose the Anthropic model. Now, there

**6:27** · are those who actually have the pro

**6:28** · subscription.

**6:29** · They can connect ChatGPT directly with

**6:32** · this system. But be careful, it's the

**6:34** · pro package. So, it's $120 per month.

**6:37** · So, if you have the plus or business

**6:39** · package, it can't connect. So, for me, I

**6:41** · actually recommend uh using the API we

**6:44** · created with Anthropic with Claude.

**6:47** · There are several other providers that

**6:48** · you can simply connect as well. There's

**6:50** · this one, Kiki May, which is also very

**6:52** · interesting and has proven itself. So,

**6:55** · for me, I work with Anthropic. Quite

**6:57** · simply, I select Anthropic here and then

**6:59** · I should enter. Remember, we created the

**7:02** · key with Claude.

**7:04** · And there you go. So, I've entered my

**7:05** · code and now I'll simply click on

**7:07** · continue. And there you go. My key has

**7:09** · been accepted. There's a very important

**7:11** · piece of information. Sometimes when you

**7:13** · add a key, whether it's from OpenAI,

**7:15** · Claude, or another API you've selected,

**7:18** · you might actually get this error

**7:20** · message.

**7:21** · So, let me show you. It's this.

**7:23** · It's an error message with error 500, as

**7:26** · you can see here.

**7:27** · So, in the documentation, I've actually

**7:29** · included a list of commands for you to

**7:31** · simply enter in order to disable this

**7:34** · error. The error is simple.

**7:36** · Basically, Hermes is trying to save your

**7:38** · key to the configuration file.

**7:40** · And by default, the configuration file

**7:42** · doesn't have what's called read-write

**7:44** · access. It's only in read-only mode. So,

**7:47** · these are a series of simple and

**7:49** · straightforward steps.

**7:52** · There are six specific steps that you

**7:53** · can easily follow right now

**7:56** · to successfully enable the settings and

**7:57** · convert the file into a fully functional

**8:00** · read-write file.

**8:01** · Just like the one we have right here.

**8:03** · So, there you go. I've included this in

**8:05** · the documentation in case you want to

**8:07** · run it to solve the blocking issue.

**8:09** · That's it. So, now once we've solved

**8:11** · that problem, we're directly on test

**8:13** · chat. Here it's prompting me to run a

**8:15** · test to see if the system works or not.

**8:18** · And when I click, it's now waiting for

**8:20** · the response.

**8:21** · And there you go. It simply tells me

**8:23** · that my interface is working perfectly

**8:26** · and that Hermes is responding correctly

**8:28** · on this interface.

**8:30** · I can simply click on continue here. As

**8:32** · you can see here, it has activated it on

**8:34** · this port, port 8642. I click on

**8:37** · continue and now I simply ask it to open

**8:39** · my workspace. So, now I'm going to save

**8:41** · the link to this workspace in my URL so

**8:44** · I can access it at any time. Let me

**8:46** · remind you that here actually in your

**8:48** · system from this button, you can launch

**8:51** · the terminal. So, this is your hosting a

**8:53** · terminal where you can run commands,

**8:56** · obviously including the commands listed

**8:58** · here to give access to your server. And

**9:00** · you also have the option to open your

**9:03** · Hermes by clicking on open. So, here

**9:05** · when I open it, it goes directly to the

**9:07** · workspace.

**9:09** · And now I'm on my Hermes workspace

**9:10** · system.

**9:12** · Very good. So, right now we're going to

**9:14** · take a comprehensive and detailed look

**9:16** · at Hermes workspace

**9:18** · in order to gain a thorough

**9:19** · understanding of exactly what the most

**9:21** · important functions are.

**9:23** · And furthermore, I'll walk you through

**9:25** · and explain in detail all of the most

**9:27** · interesting sections available here. So,

**9:29** · what you need to know is that when you

**9:30** · enter this interface, you can create

**9:32** · what are called profiles.

**9:35** · It's like on your computer, you can have

**9:36** · several

**9:37** · sessions, different login sessions.

**9:40** · Each session has its own separate login

**9:42** · and password. Inside you have specific

**9:44** · programs. That's what profiles are. You

**9:46** · can create several profiles to separate,

**9:49** · for example, interest or to separate

**9:50** · clients or even to separate models. This

**9:53** · means that on one profile, I can work

**9:55** · with Cloud and on others with Open Cloud

**9:57** · without having to switch or create

**9:59** · another Hermes account. So, if I go back

**10:02** · to the workflow, this is the profile

**10:03** · section, which is the most interesting

**10:05** · part. As you can see here, I have a

**10:07** · first profile, and this profile works

**10:09** · with this model. So, here it shows me if

**10:11** · there are any skills or competencies

**10:13** · that are installed. By the way, I can

**10:15** · click here on details to see, for

**10:17** · example, even the disk space used by

**10:19** · this profile and to view, for instance,

**10:21** · the environment file and to see, well,

**10:23** · the basic information like here, it

**10:25** · works with the provider Anthropic.

**10:28** · If I want to create other profiles, for

**10:30** · example, I click here and then I give a

**10:32** · name to that profile.

**10:34** · I can actually clone the same

**10:36** · configuration from an old profile to

**10:37** · modify it, and you'll see that it will

**10:39** · actually create a new space on the disk

**10:42** · for it. So, generally, we don't need

**10:44** · profiles unless we really want to test

**10:46** · several providers or several LLMs in

**10:49** · different ways. And each profile can

**10:51** · have its own company. And I'll show you

**10:53** · how I can create agents or sub-agents

**10:56** · within each profile. Then a very

**10:57** · important part here is that I can choose

**11:00** · the mode.

**11:01** · Either I work with what we call

**11:03** · operations or with swarm.

**11:05** · So, the first part, operation simply

**11:08** · means that I will just create the

**11:09** · different agents myself. That means here

**11:12** · I will click on operation.

**11:14** · You'll see that right here I already

**11:16** · have, let's say, a first,

**11:18** · let's say, agent in my system. So, here

**11:21** · this is an agent.

**11:22** · And I can click here to add several

**11:24** · agents. It's like having a team with

**11:26** · several colleagues. These colleagues,

**11:28** · basically, will work in my company, and

**11:30** · each one will be specialized.

**11:32** · So, here in the operation, you need to

**11:34** · know that for it to work and run, I had

**11:36** · to come here to Kanban as you can see

**11:38** · here.

**11:39** · And here I create tasks.

**11:41** · When I create tasks, I can actually

**11:43** · assign or allocate agents to handle

**11:45** · those tasks. And uh so the operations

**11:48** · part is let's say not actually done by

**11:50** · autopilot.

**11:51** · That means it needs me to give it the

**11:53** · command for me to actually define a task

**11:57** · for me to say for example to our

**11:58** · orchestration chief directly here in the

**12:00** · chat and we talk with Hermes. So uh the

**12:03** · default agent, let's say the conductor.

**12:06** · I can tell it, "Okay, go execute this

**12:07** · task." And either I tell it, "I want

**12:10** · this specific agent to do it." or I say,

**12:13** · "Listen, no. I simply want you to follow

**12:15** · here in the location." Here when I've

**12:17** · added the tasks, I can actually just

**12:19** · specify myself which agent will perform

**12:22** · the task. So that's the operations part.

**12:25** · And when we talk about the operations

**12:26** · part, we also need to talk about the

**12:28** · second part. This is actually a part

**12:30** · where we could say it's like a project

**12:32** · team, but it's self-organized. That

**12:34** · means we have a team leader who

**12:36** · distributes the work to his or her

**12:37** · employees and who can even orchestrate

**12:40** · what we would call complex projects.

**12:42** · That means he has the authority, in fact

**12:44** · he has the ability to simply create

**12:46** · these tasks, actually create reviews,

**12:48** · that is check these tasks, make

**12:50** · schedules, carry out executions, and

**12:53** · validate. So if I come back here, you'll

**12:55** · see that here I actually have this

**12:57** · section called swarm.

**12:59** · In this section, so here I can simply

**13:01** · add the mission. This is what we call a

**13:03** · commission.

**13:05** · And you'll see that of course I have a

**13:06** · main agent, but here I'm going to create

**13:08** · several agents.

**13:10** · And you'll see that of course I can call

**13:11** · here click here on con- conductor.

**13:14** · And here I'll see my different agents.

**13:16** · It's like a company, you know, I'll have

**13:18** · a little visual interface to see them

**13:20** · even in real time how they're actually

**13:21** · carrying out the tasks. And that's why

**13:23** · here at the end I always have a visual

**13:26** · that lets me see the agents as they're

**13:28** · being executed. So, either I work in a

**13:31** · manual way, I create my agents myself.

**13:33** · And for those agents, I actually give

**13:35** · them the necessary skills and

**13:36** · competencies. And then I set up what I

**13:39** · need, the project, or quite simply I can

**13:41** · go with the idea of creating what we

**13:43** · call a mission.

**13:44** · And this mission, of course, will use an

**13:46** · artificial intelligence model. Like

**13:49** · here, I can use Anthropic's or another

**13:51** · one and give it an entire complete

**13:53** · project. And then it's up to it to break

**13:55** · down the project and find the right

**13:57** · people to do it. And well, when I say

**13:59** · the right people, I mean the right

**14:00** · agents, of course, and it's the one that

**14:02** · actually does the planning.

**14:04** · So, to finish up the interface section,

**14:07** · it's very important to know that here in

**14:08** · the chat I can have an exchange with

**14:10** · Hermes. It's as if I can also talk to

**14:12** · Hermes on Telegram. It's the same thing.

**14:15** · But here it's more detailed because

**14:17** · thanks to this I can actually add

**14:19** · attachments and that's very interesting.

**14:21** · And of course, this allows me to, you

**14:23** · know, play a bit with the model to

**14:25** · switch from a classic mode to, for

**14:27** · example, a higher mode.

**14:29** · And this also gives me some very

**14:31** · important information because in the

**14:32** · chat I can change the profile here. So,

**14:35** · remember, here in the profile section,

**14:37** · if I select another profile, it's just

**14:39** · like switching sessions and I can simply

**14:42** · work with another profile directly in

**14:44** · the chat and it will automatically open

**14:46** · a new session. Another very important

**14:49** · piece of information is the job section

**14:51** · here where I can simply create, let's

**14:53** · say, a repetitive or scheduled task so

**14:55** · that the system can repeat it every 30

**14:58** · minutes, every hour, every 6 hours,

**15:00** · every day, or every week.

**15:02** · And I can give it the prompt, you see?

**15:04** · And thanks to this, actually, it's a

**15:06** · system where the system can even deliver

**15:08** · the response on Telegram, for example,

**15:10** · and can tell me whether it was done or

**15:12** · not.

**15:13** · I can tell it to repeat endlessly or I

**15:15** · can tell it to repeat, for example, five

**15:17** · times or six times. That's a very

**15:19** · interesting aspect and that's why when

**15:21** · you install Hermes on a VPS, it can work

**15:24** · 24 hours a day, 7 days a week.

**15:27** · And I'd also like to show you that today

**15:29** · when you install Hermes by default, you

**15:31** · automatically have 82 skills installed.

**15:34** · That's very interesting.

**15:36** · And these are the

**15:38** · the the basic skills that are important

**15:40** · in the system, as I can of course

**15:41** · install them myself manually or actually

**15:44** · provide the URLs on GitHub for new

**15:46** · Hermes skills.

**15:48** · This is the model. So, it's a complete

**15:50** · physical model as you can clearly see

**15:51** · here,

**15:52** · which is now fully ready to be

**15:54** · operational.

**15:55** · And of course, we can successfully

**15:57** · launch various tests and important

**15:58** · missions for the Hermes project. So, now

**16:01** · Hermes is properly installed. Now, I

**16:03** · would like you to write in the comments

**16:04** · which case study you want me to test

**16:06** · with Hermes and make a video about it.

**16:09** · So, here's an idea, a repetitive task or

**16:11** · a task that you currently do manually at

**16:13** · work, and you want me to show you how I

**16:16** · can automate it 100% with Hermes.

**16:19** · So, go ahead and leave your comments.

**16:21** · Rest assured, I read all the comments

**16:22** · from my subscribers. If I find an

**16:25** · interesting idea, I promise I will

**16:26** · record it in a separate video.
