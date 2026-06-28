---
title: "How This Ex-Meta L8 Engineer Ships 40 PRs a Day with AI Agents | Kun Chen"
source: "https://www.youtube.com/watch?v=88B6DimMD2g"
author:
  - "[[Peter Yang]]"
published: 2026-06-07
created: 2026-06-28
description: "Kun is an ex-L8 principal engineer at Meta and Microsoft who now ships 40 PRs a day without manually reviewing code. In our episode, he walked through the free tools he built to ma..."
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=88B6DimMD2g)

Kun is an ex-L8 principal engineer at Meta and Microsoft who now ships 40 PRs a day without manually reviewing code. In our episode, he walked through the free tools he built to make that possible: Lavish for visual planning in HTML artifacts, Treehouse for parallel agents, and No Mistakes for catching AI coding errors before they make it to production.

Kun and I talked about:

(00:00) Why he doesn't review code anymore
(01:04) Agentic engineering: Plan, code, validate
(06:22) Demo: Fixing an AI tutor screen with agents
(08:40) Demo: Why HTML is better than markdown for planning
(19:53) How to turn a rough idea into an AI-ready spec
(23:21) How Kun runs 20-30 agents in parallel
(32:04) No Mistakes: Kun's free AI code review tool
(45:19) What Kun checks before merging AI-written code
(50:18) How to get better at agentic engineering

Thanks to our sponsors:
Linear: The AI agent platform for modern teams https://linear.app/behind-the-craft
Wispr Flow: 4x faster than typing with your voice https://ref.wisprflow.ai/peteryang
Riverside: All-in-one AI studio for podcasts and video https://creators.riverside.com/PeterYang

📌 Get the takeaways: https://creatoreconomy.so/p/how-this-ex-meta-l8-engineer-ships-40-prs-a-day-with-ai-kun-chen

📌 Get my personal AI operating system with all my skills and prompts: https://www.behindthecraft.com/

Where to find Kun:
GitHub: https://github.com/kunchenguid
X: https://x.com/kunchenguid

Kun's free tools from the episode:
Lavish (HTML editor): https://github.com/kunchenguid/lavish-axi
Treehouse: https://github.com/kunchenguid/treehouse
No Mistakes (AI code review): https://github.com/kunchenguid/no-mistakes

Subscribe to this channel - more interviews coming soon!

## Transcript

_Caption track: English auto-generated or provided._

**0:00** · If you review every single line of code,

**0:02** · you become the bottleneck. So I don't

**0:04** · reveal this first pass code from the

**0:06** · agent. Eventually I got to a point where

**0:09** · I find myself never catching anything

**0:11** · the agents don't catch. I typically have

**0:13** · like at least five different sessions

**0:15** · actively running. On average, there's

**0:17** · like 20 to 30 agents running. Most of

**0:19** · the time, uh, it's like 20 to 40 kind of

**0:22** · PRs every day. Our workflows and how our

**0:25** · teams work were built at a time when we

**0:28** · spend most of our time coding. But when

**0:30** · you start to write like 10 times more

**0:32** · PRs, we are not ready for that to really

**0:35** · scale up how much we can get from the

**0:37** · agents. We have to move ourselves out of

**0:40** · the loop as much as possible.

**0:44** · Hey everyone, today I'm really excited

**0:46** · to welcome my friend uh, an L8

**0:48** · engineer from Meta at Microsoft who's

**0:50** · now a solo AI builder. is going to

**0:53** · show us exactly how he builds products

**0:55** · using agents. I've been asking him a lot

**0:57** · of dumb questions about all this. So,

**0:58** · we're really excited for him to show us

**1:00** · live. So, welcome, sir.

**1:02** · >> Thanks for having me here, Peter.

**1:04** · >> All right. So, uh let's get right into

**1:05** · it. Maybe you can start uh by kind of

**1:08** · walking through at a high level how

**1:09** · you're building products with agents.

**1:12** · >> All right. Um that is my workflow. Um

**1:15** · plan, code, and validates. Uh I don't

**1:17** · think this is too different from uh what

**1:19** · everybody does. Um, so I'll probably

**1:21** · talk through the parts where I think I'm

**1:23** · doing something unique. Um, so I think

**1:26** · typically when we build something

**1:27** · meaningful, we typically go through

**1:29** · these phases, right? We plan what the

**1:31** · requirements are. Um, and then we let

**1:33** · the agent code and then we uh have to do

**1:35** · some validation to make sure the agent

**1:37** · actually did what we wanted them to do.

**1:39** · Um, so this uh the high level workflow I

**1:41** · think is pretty standard. Um, where I

**1:44** · think I do something different uh is uh

**1:46** · how much time I spend in each phase. Um

**1:49** · so currently I think I spend more time

**1:51** · in the planning phase. Uh so planning is

**1:54** · like mostly me with assistance from uh

**1:57** · the agents. The coding phase is pretty

**1:59** · much entirely the agents. Um so I once

**2:01** · the requirements are planned very

**2:03** · clearly. Um I trust the agents to do

**2:06** · most of the work. Um and then in

**2:08** · validation phase uh I use agents a lot

**2:10** · as well. Um and agents do most of the

**2:12** · work with some judgment from me when

**2:15** · things are ambiguous. And I think uh the

**2:18** · the the part the part about this is that

**2:21** · um if we actually uh start to delegate

**2:25** · most of the coding to agents.

**2:27** · >> Mhm.

**2:28** · >> What I um the way I think u I can uh get

**2:31** · agents to do more for me is to try to

**2:34** · increase the amount amount of time

**2:36** · agents spends in this phase because this

**2:38** · is entirely agents right so if we can

**2:40** · get the agents to do to go for longer uh

**2:43** · then I'll get more done. So this is one

**2:46** · area where I tried a lot of things to

**2:49** · just scale up the amount of time I can

**2:51** · let the agents run autonomously.

**2:53** · >> Yeah. It's almost like the code and the

**2:55** · validation is a loop that the agent can

**2:57** · run itself, right? And and so that it

**2:59** · can actually code for a longer time

**3:01** · period.

**3:01** · >> Yeah. Yeah. And also I think it depends

**3:03** · on how much time we spend in the

**3:05** · planning phase. So if I uh spend a lot

**3:07** · of time crafting a very detailed plan

**3:09** · then I can let the agents go for longer.

**3:12** · um if I uh only write a very very short

**3:15** · prompt then what I'll find is that uh

**3:17** · very quickly the agents will get work

**3:18** · done and then I'll need to go back and

**3:20** · prompt them again. So uh like how much

**3:23** · time we invest in the planning phase

**3:25** · actually affects this a lot.

**3:26** · >> Okay, that's a really good point because

**3:28** · I I've gone like super lazy with these

**3:29** · agents. I don't actually like I just

**3:32** · give them like one line prompts and yeah

**3:34** · it never works for hours. So yeah would

**3:36** · love to kind of see each face.

**3:39** · >> Yeah. Yeah. So yeah, I think the things

**3:41** · that we we can do differently in the

**3:42** · planning phase is like go from a short

**3:44** · prompt uh to say what is the next action

**3:47** · you should take to something more like a

**3:49** · spec where um you you write down a more

**3:52** · uh a more comprehensive set of details

**3:54** · of the requirements and then go from

**3:56** · spec to a goal. So if you can actually

**3:59** · craft a measurable goal, you can let the

**4:02** · agents do a lot of experimentation.

**4:04** · >> Okay. Okay. So can you show us how this

**4:06** · works? like maybe we can start with the

**4:08** · planning phase like

**4:10** · >> some some example plans that you write.

**4:11** · Yeah.

**4:12** · >> Yeah. Actually uh there's another uh

**4:14** · dimension of how I optimize this flow as

**4:16** · well. Uh which is like if you look at

**4:18** · this uh this uh timeline, right? Um the

**4:22** · parts that need me is only like this

**4:24** · beginning and the end, right? Uh so what

**4:27** · I do is like I I make sure I can

**4:29** · paralyze a lot of sessions. Um so so

**4:32** · that's I'm always spending my time

**4:34** · productively um uh while the agents are

**4:37** · doing the work. So I think increasing

**4:39** · the the amount of concurrent parallel

**4:42** · sessions that's also a very important

**4:43** · aspect of how I get more done.

**4:46** · >> And do you parallelize sessions in the

**4:47** · same uh project and product or like

**4:49** · across products or both?

**4:51** · >> Uh both both. Uh so I have a hybrid of

**4:53** · different projects. Uh but even within

**4:55** · the same project I sometimes have

**4:57** · multiple sessions doing different

**4:58** · things.

**4:59** · >> Yeah. It's funny. It's funny because we

**5:00** · used to uh like you know both of us used

**5:02** · to work in big tech and um it used to be

**5:05** · a lot of context switching between

**5:06** · meetings but now you're context

**5:08** · switching between different threads or

**5:09** · [laughter]

**5:10** · you know it's actually it's actually

**5:12** · faster context switching in some ways.

**5:14** · >> Yeah. Yeah. Totally. I I think uh it's

**5:16** · kind of like a um someone that's

**5:18** · overseeing a very large scope, right?

**5:20** · There's always different things

**5:21** · happening and there are different things

**5:23** · escalating to you and you need to jump

**5:25** · into different things depending on what

**5:27** · is the where you are needed the most. Uh

**5:29** · so this is very much alike.

**5:31** · >> Okay, this episode is brought to you by

**5:33** · linear. When engineers use tools like

**5:35** · cursor, clock code and codeex, a lot of

**5:38** · work happens invisibly. Someone can go

**5:40** · from a bug report in Slack to a shipped

**5:43** · fix without creating any record of what

**5:45** · happened outside of the code editor. And

**5:47** · that's fine for speed, but it makes

**5:48** · coordination harder as you scale. Linear

**5:51** · integrates with the very best agent

**5:53** · coding tools directly like cursor and

**5:55** · codeex. That way, anyone can see what an

**5:58** · agent is working on and who assigned

**6:00** · them to the task. You get the speed of

**6:02** · agents without losing visibility across

**6:04** · the team. Product teams at OpenAI, Ramp,

**6:07** · and Block are all using Linear to

**6:09** · collaborate with AI agents. And I use

**6:11** · LIR myself to run my creator business.

**6:13** · So, check it out at linear.app/

**6:17** · aents. That's linear.app/

**6:20** · aents. Now, back to our episode.

**6:22** · >> Can you show us your, you know, AI stack

**6:23** · or agent decoding setup?

**6:25** · >> Yeah. Yeah, let's do it. Uh, so this is

**6:28** · my terminal. Uh, this is where I I do

**6:30** · like all of my work pretty much. uh

**6:32** · occasionally I I switch to a GUI or a

**6:34** · browser uh but most of the time uh I'm

**6:37** · spending here. Uh so yeah I'm using a

**6:39** · project here as an example to walk

**6:41** · through it. Um so this is this is a

**6:43** · project called hybits. Uh this is the AI

**6:46** · tutor I'm building for my son. Uh it's

**6:48** · an AI uh agentic uh harness uh for kids

**6:52** · basically. And I just um built a new

**6:55** · screen. Um so let me let me show you

**6:57** · what that looks like. Um I revamped uh

**6:59** · the um the main screen a little bit. Um

**7:02** · but this is very messy because I just

**7:04** · did this this morning. Uh and it's not

**7:06** · looking good. Uh this is like this is

**7:08** · not how I want this to look like. Um so

**7:11** · I uh what I'll do uh like very typical

**7:14** · workflow. I'll take a screenshot of

**7:15** · this,

**7:17** · right? Uh take a screenshot and then I

**7:20** · come to my agent.

**7:22** · Um I use open code a lot. Uh so I'm

**7:25** · going to just launch open code in here.

**7:27** · >> Mhm. And you use it because you can use

**7:29** · multiple models.

**7:30** · >> Yeah. Yeah. Exactly. So I I can very

**7:32** · quickly try different models when the

**7:33** · new models come out. Uh that is the uh

**7:36** · big benefits I get from these open

**7:37** · source tools.

**7:38** · >> Makes sense.

**7:39** · >> Um so yeah so what I'll do here is I'll

**7:41** · just say hey look at this uh this

**7:45** · screen. I'll paste uh the image here. Um

**7:49** · and uh I'll say uh the things we saw on

**7:52** · the screen. The things that I'm I was

**7:54** · not very happy about was there is uh too

**7:56** · much technical details not uh that are

**8:01** · not friendly for kids. Uh also there is

**8:05** · a big area of white space uh unused

**8:09** · right those were the problems that we

**8:11** · saw on the screen that's were like

**8:13** · clearly not uh uh ideal. Uh so I'll I'll

**8:16** · point out these problems um and I'll say

**8:19** · hey uh can you propose

**8:23** · uh some options for how we improve right

**8:27** · so this is my uh the request I sent to

**8:29** · the agent so because I sent the

**8:32** · screenshot uh the um the model is going

**8:34** · to be able to see visually uh what is

**8:37** · going on there and then it's going to uh

**8:40** · look at uh the codebase as well this so

**8:42** · yeah it's very quickly came up uh with

**8:44** · this plan So it says like best

**8:46** · direction, option one, option two. The

**8:48** · thing with this plan is that it's not

**8:51** · very easy to read, right? Um so like

**8:53** · when you look at this long wall of text,

**8:55** · I like this I I I I will spend so much

**8:59** · time reading this text. Um so what I do

**9:02** · instead uh let me just try a new

**9:05** · session. Uh what I actually do uh is I

**9:08** · use a visual editor to uh do the

**9:10** · planning. So uh I'll say the same thing.

**9:13** · uh look at this screen there is too much

**9:15** · uh technical details same thing right uh

**9:19** · I will just add one bit to say use

**9:22** · lavish uh to

**9:25** · discuss this with me uh along with any

**9:29** · questions you have um so lavish is a is

**9:34** · a visual editor uh I built um after I

**9:37** · read the article about HTML uh over

**9:40** · markdown uh have you seen Yeah. Yeah.

**9:43** · The from the Yes.

**9:45** · >> Yeah. Yeah. Um, initially when I saw the

**9:47** · article, I was not very sure about that

**9:50** · because I I felt like HTML uh is going

**9:53** · to be so token inefficient, right? Uh

**9:55** · the models will have to write a lot more

**9:57** · than a simple markdown. Um but when I

**10:00** · tried it, it's actually super useful. Um

**10:02** · so I'll show you once uh once we uh have

**10:05** · this result from here. um the HTML as an

**10:08** · artifact can be a lot richer in terms of

**10:11** · like supporting this collaboration

**10:13** · between human and agent. Um so it's not

**10:15** · going to be a long wall of text I have

**10:17** · to read through. Uh it's going to be

**10:19** · like very visually um things I can just

**10:21** · interact with.

**10:22** · >> So Lavish is a is is like a app that you

**10:24** · build to create the HTML in the format

**10:26** · that you want. Is that

**10:27** · >> Yeah. Yeah. It's a um it's a tool I

**10:30** · built. Uh so what I do is like I uh

**10:32** · every time I encounter any kind of a

**10:34** · friction in my workflow and I don't find

**10:36** · anything that can solve the problem for

**10:38** · me I just build something myself.

**10:41** · >> Yeah, Lavish is a is a tool I built. Uh

**10:43** · it's a tool for

**10:45** · >> both generating the HTML artifact and

**10:48** · also supporting the uh back and forth

**10:51** · interactive experience between human and

**10:52** · agents on that. Um because what you um

**10:55** · what we could do is I can just ask the

**10:58** · agent to generate a HTML file, right? Uh

**11:00** · and I and then I can open up the HTML

**11:02** · file in the browser and it works. Um the

**11:04** · problem with that approach is that once

**11:06** · the HTML file is open and I I look at

**11:09** · the HTML file and I see that there are

**11:12** · some things I don't like, it's very hard

**11:14** · for me to then tell the agent, hey,

**11:17** · please change this part. U please

**11:19** · iterate on this aspect. Right? So that

**11:21** · back and forth is what um Lavage Editor

**11:24** · is trying to solve.

**11:26** · >> Oh, awesome. Yeah. Really excited to see

**11:27** · what what it is. Yeah.

**11:29** · >> Yeah. Yeah. So now it's writing uh the

**11:31** · HTML. Uh it'll probably take a little

**11:33** · while because uh that's uh usually a lot

**11:35** · of content to write. Uh so uh let's see

**11:38** · what I um maybe uh one thing I can show

**11:40** · here um is that uh while the agents are

**11:42** · working uh typically agents either

**11:44** · coding or planning can spend quite some

**11:47** · time doing this work. Um so what I do is

**11:49** · I'll just spin up another parallel uh

**11:51** · terminal tab uh a window right I use

**11:54** · t-mox so this is a new t-mox window um

**11:57** · and in this window I will do something

**11:59** · else um and we can see it's in the same

**12:02** · directory the problem here is that uh if

**12:04** · I spin up another agent to work in the

**12:07** · same directory they will run into each

**12:09** · other right so what this agent does in

**12:11** · this session will like step on toes of

**12:14** · the other agents that were that's

**12:16** · already doing the work um Yeah.

**12:18** · >> So this is where people uh started using

**12:20** · work trees. So typically people uh what

**12:23** · people do is like get work tree ad and

**12:25** · give another directory uh like high bits

**12:28** · and spend like five minutes thinking

**12:30** · about the name. Uh but I'm just going to

**12:31** · say h high high bit too. Um so the the

**12:35** · thing the problem with this approach is

**12:37** · that once I create a work tree like this

**12:40** · next time I come to this work tree I

**12:42** · have to think about what is hybrid 2

**12:44** · doing uh like what is this this work

**12:46** · tree doing right is it still being

**12:48** · worked on is it like okay to like use

**12:51** · for something else it's very hard to

**12:53** · keep track of

**12:55** · >> um and the other problem is like when we

**12:56** · create a new work tree the dependencies

**12:59** · are not installed in the in the work

**13:01** · tree. So in this work tree we have

**13:03** · things like node modules right like

**13:05** · these are dependencies downloaded on the

**13:07** · fly and these dependencies won't exist

**13:10** · in the new work tree until you install

**13:13** · all of them again. Um so there were many

**13:15** · problems like that

**13:16** · >> and just for people who don't know like

**13:18** · like what's our definition of the work

**13:19** · tree is it like a copy of the codebase

**13:21** · right or

**13:22** · >> yeah yeah so a work tree is basically

**13:24** · like you can think of it as a clone of

**13:26** · your current uh git repo um in another

**13:30** · directory. So it's going to be a

**13:31** · parallel direct directory and they don't

**13:34** · directly interfere with each other. Um

**13:36** · so you can do um a different kind of

**13:38** · work different set of work in the work

**13:39** · tree and it won't affect what you were

**13:41** · doing in the main repo.

**13:43** · >> Okay. But but you're saying that there's

**13:44** · like a many issues with the work tree.

**13:46** · So what do you do instead?

**13:48** · >> Yeah.

**13:48** · >> Yeah. Basically there's a very heavy

**13:50** · like cognitive load to maintain the work

**13:53** · trees. You have to think about which

**13:55** · work tree is which uh and which ones are

**13:57** · okay to clean up etc etc. Um, so what I

**14:00** · did was I have a tool called Treehouse.

**14:03** · Uh, so Treehouse is basically like a a a

**14:06** · no-brainer like uh a a very like dead

**14:10** · simple way to manage work trees. Um, so

**14:13** · every time I have to spin up a new work

**14:15** · tree to do something new, right? I don't

**14:17** · need to think about uh do I have another

**14:19** · work tree I can use? Do I uh create a

**14:21** · new one? I just type treehouse and

**14:23** · treehouse will basically set up the work

**14:25** · tree for me and drop me into the new

**14:27** · work tree. Uh so now it you can see it's

**14:29** · set up a work tree in this directory

**14:32** · right and uh it dropped me into it and

**14:35** · the the good thing is that this

**14:37** · directory um is a is from a pool of

**14:40** · managed work trees. So um so the

**14:44** · dependencies are already installed here

**14:46** · because I have used this work tree

**14:48** · before um so I don't have to like

**14:50** · reinstall dependencies rebuild the

**14:52** · project every single time. Uh it also

**14:54** · saves on the efficiency aspect. So yeah,

**14:57** · just like reduce the mental load a lot.

**14:59** · I don't need to think about anything. I

**15:00** · just type treehouse every time I want to

**15:02** · start a new session.

**15:03** · >> That makes sense. Okay. All right, dude.

**15:05** · Well, let's go back to the other tab.

**15:07** · >> Yeah. So this is uh what's the HTML

**15:09** · looks like. Um so it's saying, hey, uh

**15:13** · redesign discussion. Uh it's basically

**15:15** · there's a tiny icon here, not available.

**15:18** · Not sure what happened there, but u

**15:20** · basically it's uh it wrote the proposal

**15:23** · in in a visual artifact, right? Um, so

**15:27** · what's going what's feeding off? The

**15:29** · screen is doing like grown-up work in

**15:31** · kids space. Exactly. Right. Um, and

**15:34** · these things uh there's uh unused space.

**15:37** · Um, yeah.

**15:38** · >> This is easier to scan and read for a

**15:41** · human basically.

**15:42** · >> Yeah.

**15:43** · >> Yeah. Yeah. And uh if if there's

**15:45** · something I uh I look at the uh this

**15:47** · artifact and I if I see something that

**15:50** · doesn't feel right, I can just annotate.

**15:52** · Um so bit has no visible body. I can say

**15:55** · I just click on this and say I don't

**15:58** · care about this. Um and give the

**16:01** · feedback to the agents this way. Um

**16:03** · >> Oh, I see. So this is your app. Okay.

**16:05** · Got it. Okay, that makes sense.

**16:06** · >> Yeah. So this is a lot more difficult to

**16:08** · do when it's a long wall of text, right?

**16:11** · Uh when it's a wall of text, you have to

**16:13** · say to the agent, hey, I I I I don't I'm

**16:16** · not happy about this part of the spec.

**16:18** · Uh and you sometimes have to copy paste

**16:20** · a lot.

**16:21** · >> Got it.

**16:21** · >> Yeah. So it basically proposed a bunch

**16:23** · of things. Uh, copy, clean up. Uh,

**16:27** · >> yeah, some of the layout things is not

**16:29** · ideal, but yeah, I I get it. It's it's

**16:31** · easier to read for sure. Yeah.

**16:32** · >> Yeah. And I I I think there's probably

**16:34** · like something that went wrong in this

**16:36** · uh page. Uh, let me let me let me just

**16:38** · check. Uh, I can just ask the agent as

**16:41** · well. Um, because uh when I look at

**16:43** · this, I think the agent is trying to

**16:44** · give me a visual representation of the

**16:47** · layout. Um, but because of the CSS is

**16:49** · not quite working or something. Um, it

**16:52** · seems the CSS styles uh not working. Let

**16:58** · me fix it. Um, so yeah, I can just send

**17:01** · feedback back to the agent uh this way

**17:03** · and um I don't have to keep switching

**17:05** · between the HTML artifact and the agent

**17:08** · uh in the terminal. Uh I can just talk

**17:10** · to the agent here. Um and I can easily

**17:13** · annotate everything uh and just point uh

**17:15** · the pinpoints exactly where I mean.

**17:18** · >> Can you show folks where they can

**17:20** · download this tool? It's it's open

**17:21** · source, right?

**17:22** · >> Uh so it's uh in my GitHub repo lavishi

**17:28** · uh in this repo. Uh and it has uh it's

**17:31** · actually very simple uh to start using

**17:34** · it. Just tell your agent use npx lavish

**17:37** · axi to write the technical plan or do

**17:39** · whatever you want.

**17:41** · >> Um and the agent will go uh invoke this

**17:43** · and everything goes on from there. And

**17:46** · uh you have to do you have to hook up

**17:47** · your own uh API key for the LM?

**17:50** · >> No, you you just use whatever agent you

**17:52** · are already using. Um this lavish editor

**17:55** · itself does not uh run another agent.

**17:58** · >> Uh it runs within your agent session. So

**18:01** · actually

**18:01** · >> Okay, got it.

**18:02** · >> Yeah. So you can see here um the agent

**18:05** · calling lavish axi uh to pull like this

**18:08** · uh this artifact.

**18:09** · >> Okay, that makes sense.

**18:11** · >> So let's come back to it. Um yeah. So,

**18:13** · so now uh it fixed the CSS problem,

**18:16** · right? This is what what is supposed to

**18:18** · look like. Uh so you can see like this

**18:20** · is a lot uh like more visual and easier

**18:23** · to understand.

**18:24** · >> Looks a lot better. Yeah.

**18:26** · >> Yeah. So this is like pointing out the

**18:27** · current layouts, current uh problems and

**18:30** · then uh it's probably like proposed a

**18:33** · new thing. Okay. So it proposed four

**18:35** · directions for using the space better.

**18:38** · Option A looks like this. This is like

**18:41** · this is so much easier to see, right?

**18:44** · Like than like the long wall of text we

**18:46** · have in the uh in the uh terminal. Um so

**18:50** · here we can see okay it's uh moved the

**18:52** · layout a little bit. Uh now this is the

**18:54** · chat this is some other area. Okay

**18:56** · that's one option.

**18:57** · >> Um and it even gave me buttons. So uh if

**19:01** · I like option A I can just click this

**19:03** · button and I get the option A. Um got

**19:05** · it. So option B looks like this. Uh

**19:08** · today's goal. Okay. Um, option C, uh, is

**19:12** · this. Okay. Option C is very simple. I

**19:14** · actually like this. Um, option D. Okay.

**19:18** · Yeah. So, let's say I like option C. I

**19:21** · can just click this

**19:22** · >> and it basically killed a uh a piece of

**19:25** · feedback to the agent saying I like

**19:27** · option C. Um, so it's just so easy to

**19:29** · interact with. Um, I don't have to keep

**19:31** · typing uh every time I want to tell the

**19:33** · agent something. Everything can be done

**19:35** · interactively.

**19:36** · >> Okay. Okay. So, and and this is uh the

**19:38** · plan phase for like building a new

**19:40** · feature on top of an existing app,

**19:42** · right?

**19:42** · >> Yeah.

**19:43** · >> I'm curious and maybe not to show this,

**19:44** · but I'm just curious like how you plan

**19:46** · something from scratch initially. Like

**19:47** · did you like spend a lot of time

**19:49** · planning like the the milestones and the

**19:51** · tech stack and that kind of stuff?

**19:53** · >> Yeah. Yeah. So, if it's something from

**19:55** · scratch, uh I usually have to spend a

**19:57** · little bit more time. Um so, what I do

**19:59** · is that I use the same lavish editor.

**20:02** · Um, I tell the agent that I I want to

**20:05** · brainstorm a new idea with you. Um, and

**20:08** · uh, I'll probably like talk through some

**20:10** · of my initial thinking for what things I

**20:13** · think um, are the core parts of my idea.

**20:16** · And then I'll ask the agent to um,

**20:18** · criticize that and uh, come up with like

**20:21** · areas of risks uh, or weaknesses I

**20:24** · haven't uh, may uh, maybe I haven't

**20:26** · thought through yet. Um, and then come

**20:28** · back with it uh, its opinion. Um and the

**20:31** · agent will then come back with a uh HTML

**20:34** · artifact like that and I can look at the

**20:36** · artifact to uh basically like work with

**20:39** · the agent to refine the idea to a point

**20:42** · where it becomes a spec basically.

**20:44** · >> Do you always like include some certain

**20:45** · sections in your spec like build it in

**20:47** · three phases or like here's the

**20:49** · milestones or like here's a tech tech

**20:51** · stack I want you to use like that kind

**20:52** · of stuff.

**20:53** · >> Yeah. Yeah. So uh for some projects, for

**20:55** · some ideas, I already have uh some uh

**20:58** · opinions on things to use and things to

**21:00** · do. Uh in those cases, I'll just write

**21:02** · them down and say these are my

**21:04** · preferences. Um but I always tell the

**21:06** · agents that it's okay for you to push

**21:08** · back if you see something that is not

**21:10** · right. Um because I want to give the

**21:13** · agents the flexibility and I want to see

**21:15** · more options as well. Um so yeah, I I I

**21:17** · basically like give my ideas to the

**21:19** · agents uh but let the agents give more

**21:21** · back. So, so then do you have like a

**21:23** · user level agent.mmd or something that

**21:25** · like uh has some of these best practices

**21:28** · like you know you can push back on me or

**21:30** · it's just more natural through the

**21:31** · conversation?

**21:32** · >> Yeah. Uh so I um I actually built a lot

**21:35** · of those instructions into uh lavish

**21:38** · editor.

**21:39** · >> Um so whenever the agent is is using uh

**21:41** · the lavish editor to work with me, the

**21:44** · agent already knows uh a lot of those um

**21:46** · like those best practices.

**21:48** · >> Got it. Okay. And how about how about

**21:50** · like uh if you're building like a userf

**21:51** · facing product, how do you think about

**21:53** · the design? Do you have like another

**21:54** · tool for design or you just you have

**21:56** · some skills?

**21:57** · >> For design uh you mean visual design?

**21:59** · >> Yes.

**22:00** · >> Yeah. So for visual design, I like cloud

**22:03** · design a lot. Um since it came out, I

**22:06** · use that a lot. Uh and uh very often I

**22:08** · I'll use a lot of the quota they have uh

**22:10** · for me. So if you look at this uh this

**22:13** · this bar where I track my quota um cloud

**22:17** · I mostly used up my weekly quota already

**22:19** · I'm waiting for the reset and cloud

**22:22** · design I used um like uh twothirds of it

**22:26** · um okay because I yeah I just find it

**22:28** · very useful to um especially for new

**22:30** · projects I use this a lot to build a new

**22:33** · design system um because once I get the

**22:36** · design system built I can apply that to

**22:39** · many many different components in my

**22:41** · project uh very easily.

**22:42** · >> Yeah. Okay. May maybe you can show that

**22:44** · later later, but why don't why don't we

**22:45** · finish this work worker first? Yeah.

**22:48** · >> Yeah. Cool. So yeah, we basically we

**22:49** · chose option C, right? Um so now we can

**22:52** · just say hey uh build option C now. Um

**22:56** · and uh because we already have the plan

**22:59** · uh written uh in the HTML artifacts, the

**23:02** · agent already has the context on what

**23:03** · that means and uh what's the choices uh

**23:06** · were made. Uh right. So, uh, the agent

**23:08** · can just like go ahead and, uh, and

**23:10** · implement that. Now,

**23:11** · >> how many like, uh, since you're just

**23:12** · like building solo now at home, like how

**23:15** · many of these agent building sessions do

**23:17** · you have going? Like, like the agent

**23:18** · actually building something for you at

**23:20** · any given time like Yeah.

**23:21** · >> Yeah. Yeah. So, I I like closed as many

**23:24** · sessions as I could before I uh started

**23:26** · this session. Uh, but uh, I typically

**23:29** · have like at least uh five different

**23:31** · sessions actively running. Um, and in

**23:34** · each session there are usually like a

**23:36** · bunch of sub agents uh or different uh

**23:38** · agents working. Uh, so in total I never

**23:41** · like really counted but I I would guess

**23:43** · on average there's like 20 to 30 agents

**23:46** · running.

**23:47** · >> Okay, got it. Okay, so you mentioned you

**23:49** · have sub agents running like you

**23:51** · actually specifically ask it to run sub

**23:52** · agents or like it just decides to like

**23:55** · when when when do you actually need a

**23:56** · sub agent versus just using one agent?

**23:58** · >> Yeah. Yeah, great question. Uh so I

**24:00** · think the u most of the models today uh

**24:02** · and the harnesses they are not very

**24:05** · great at proactively using sub aents. Um

**24:08** · there are only a few cases where like

**24:10** · cloud code or codeex will proactively

**24:12** · use the sub aent. It's when like they

**24:14** · have the their built-in agents like

**24:17** · explore. Um so when you uh ask a complex

**24:20** · question uh cloth code will often run a

**24:23** · explore sub agent right to do some

**24:25** · exploration in the codebase and come

**24:26** · back with some investigation results. Um

**24:29** · those are the cases where the models

**24:31** · will proactively use a sub agent. But in

**24:33** · a lot of cases uh because the models I

**24:35** · think they are not trained uh enough yet

**24:38** · to use sub aents in various different

**24:40** · kind of cases you often have to prompt

**24:42** · it to do so.

**24:44** · >> Got it. Okay. What are some cases where

**24:46** · you actually want to prompt it to use

**24:47** · sub aents like to for like validation or

**24:49** · >> Yeah. So um the reason uh I think the

**24:52** · main reason I would use a sub agent is

**24:54** · to avoid context um context window

**24:56** · blowing up in the main agents uh

**24:58** · session.

**24:59** · >> Oh I see.

**25:00** · >> Yeah. So uh what I uh what I do what I

**25:03** · uh I think the time when I choose to use

**25:05** · sub agents is when I realize what I'm

**25:07** · about to do uh is going to use a lot of

**25:10** · context and most of the context is going

**25:12** · to be uh like investigation kind of

**25:16** · exploration kind of uh scenario and most

**25:18** · of the exploration may be not meaningful

**25:21** · for the main session. Uh so in those

**25:23** · cases uh basically I like carve out

**25:25** · those sub agents to do those

**25:26** · investigations and only come back with

**25:28** · their conclusion. Okay. So it's like uh

**25:30** · like hey spin up a sub agent to look at

**25:33** · this codebase or do some research on

**25:34** · this topic and summarize it and give it

**25:37** · back to the main a agent like that kind

**25:38** · of stuff right.

**25:39** · >> Yeah. Yeah. Or like there are cases

**25:41** · where I have like 10 experiments ideas

**25:44** · to run and each experiment uh I each

**25:47** · experiment can be done in isolation. Uh

**25:50** · right so in those cases I also like just

**25:52** · say uh hey like spin up 10 sub agents to

**25:54** · do that. Um, if I do that all in the

**25:56** · main agent, it's going to just like blow

**25:58** · up the context window and take a lot of

**26:00** · time and uh and uh tokens as well.

**26:02** · >> When you say experiment ideas, you mean

**26:04** · like like AB testing stuff or or or what

**26:07** · like like different ways to build

**26:08** · things?

**26:08** · >> Yeah, so there are various kind of uh

**26:10** · experiments I run. Uh there's one

**26:12** · example here I can show. Um so this is

**26:14** · one uh something I'm running. Uh this is

**26:17** · the one I didn't uh kill. Um so this is

**26:20** · a this is a a benchmark I'm running to

**26:24** · evaluate the effectiveness of different

**26:26** · programming languages when given to

**26:28** · agents

**26:29** · >> and uh there was this benchmark that

**26:31** · were that was published like two weeks

**26:33** · ago called program bench uh it's called

**26:35** · program bench uh it's built by the same

**26:38** · people that built Swebench um and it's

**26:41** · their new thing and program bench

**26:42** · basically ask the agents to build uh a

**26:46** · bunch of programs like ffmpeg

**26:48** · like these tools from scratch and see

**26:51** · whether the agent can actually get all

**26:53** · the requirements done uh and pass all

**26:56** · the test cases.

**26:57** · >> So that is the that was the benchmark.

**26:59** · Um but I thought the benchmark can be

**27:01** · very useful for evaluating different

**27:04** · harness uh harness techniques and also

**27:06** · different uh programming languages. Uh

**27:08** · so right now what I'm evaluating here is

**27:11** · I'm I'm running program bench on codeex

**27:14** · and I I force codeex to use these

**27:18** · programming languages like typescript,

**27:20** · javascript, python and see when they use

**27:23** · different languages do they get

**27:25** · different results right uh is there a

**27:27** · programming language that will that will

**27:29** · lead to the agent getting uh more

**27:32** · requirements done and passing more tests

**27:34** · and use less tokens etc etc. Um so so

**27:38** · this is a very large amount of uh

**27:40** · experiments. Um basically like there are

**27:42** · um like 200 multiplied by uh eight right

**27:48** · uh so there's that that's a lot of

**27:49** · things to run and in those cases I I

**27:52** · basically like have sub agents uh

**27:53** · running and uh if I run all these in a

**27:56** · single main agent it's just going to

**27:58** · keep running compaction and uh not going

**28:00** · to be very efficient.

**28:01** · >> That makes sense. Okay cool. Let's go

**28:02** · back to the kit.

**28:03** · >> Yeah. So it looks like it's running a

**28:06** · bunch of tests right now, right? So like

**28:07** · is that just the model knows to run

**28:09** · tests or you actually you have some

**28:10** · instructions to have it built unit test

**28:12** · and stuff like that each time?

**28:15** · >> Yeah.

**28:15** · >> Uh I typically um in my um agents MD in

**28:19** · each project I I will like have some

**28:21** · instructions for how to uh perform

**28:24** · tests. Uh so uh here for example

**28:27** · uh I can show the agents MD here. So in

**28:31** · this is the agents MD for the high bit

**28:33** · project uh we were looking at. Um and in

**28:35** · here we'll just have some like high

**28:37** · level context on the structure of the

**28:39** · project. Um and then I'll have some uh

**28:41** · testing instructions. This is actually

**28:44** · super helpful. Um so previously I didn't

**28:47** · do this and I let the agent decide what

**28:49** · to do and the agent will just do the

**28:51** · like kind of do the minimum. Um and uh

**28:54** · they they they are trained to run some

**28:56** · basic testing uh but they are not going

**28:58** · to be comprehensive enough. Um so I have

**29:01** · here is like instructions for how to do

**29:03** · end to end testing. This is important

**29:05** · for like building uh front end and UI

**29:08** · kind of projects. Uh right we were

**29:11** · looking at hybrids which had a GUI. Um

**29:13** · so in this case I tell the agents hey uh

**29:18** · this is a electron app you can drive

**29:20** · this uh this app by running a browser

**29:24** · and uh and blah blah blah how to do this

**29:27** · testing how to actually test things end

**29:28** · to end. So with that instruction here

**29:31** · the agent will uh will like just once

**29:34** · it's done its work it will actually

**29:36** · validate things end to end for me. Um,

**29:38** · so that can save me a lot of time from

**29:40** · like running the app myself and visually

**29:43** · validating is that actually what I want.

**29:46** · >> Okay. So it's basically like uh using

**29:47** · browser use and checking out the app,

**29:49** · see if it looks okay. Maybe checking

**29:50** · some browser errors.

**29:52** · >> Yeah, exactly.

**29:53** · >> Yeah. And take screenshots as well. Take

**29:55** · screenshots and look at these things

**29:56** · visually and see whether it's actually

**29:58** · aligned with what we talked about. I

**30:00** · think if you use the codeex app, I I

**30:02** · think it does it by default, but like

**30:05** · let's say like I'm not very technical,

**30:06** · like how do I even know to include this

**30:08** · stuff? Should I just tell the agent to

**30:10** · run a lot of tests or

**30:11** · >> Yeah. Yeah. Yeah. So typically um what I

**30:14** · uh one thing I one thing that's really

**30:16** · interesting I found is that

**30:18** · >> uh by default the agents like to write

**30:20** · unit test like very uh purely uh code

**30:24** · based unit tests and those unit tests

**30:27** · often don't actually validate things end

**30:29** · to end. So for example uh even in codeex

**30:32** · I think codeex by default likes to use

**30:34** · the builtin uh inapp browser right?

**30:37** · >> Yeah. Um so when you work on some front

**30:39** · end changes uh it will use the inapp

**30:42** · browser to uh look at the change and uh

**30:45** · have you look at that as well. Um but

**30:47** · this is an electron app. It's a desktop

**30:49** · app. So it actually requires a different

**30:51** · set of uh yeah facilities to validate

**30:54** · that. Um so the instructions here are

**30:57** · basically how I would test this thing

**31:00** · myself.

**31:01** · >> Um

**31:01** · >> okay.

**31:02** · >> Yeah. So basically like the more um the

**31:04** · more things uh that I find myself doing

**31:07** · that I can delegate to an agent, I turn

**31:09** · them into instructions and then let the

**31:12** · agents do the work uh instead of me like

**31:14** · operating the app myself manually.

**31:16** · >> Okay. Got it. Okay. So so I guess like

**31:18** · someone who maybe is not as

**31:19** · knowledgeable as you can just like like

**31:21** · I guess a general principle is like if

**31:22** · you're doing something manually like

**31:24** · you're manually opening the app and

**31:25** · looking at the screens just ask the

**31:27** · agent, hey can you just auto automate

**31:29** · this for me, right? just just ask it and

**31:31** · hopefully it can figure some something

**31:32** · out too.

**31:33** · >> Yeah. Yeah. So yeah, if you are like not

**31:34** · trying to dig into the technical

**31:36** · details, uh then the principle the high

**31:37** · level principle is like if you find

**31:40** · yourself manually doing something, then

**31:42** · try to turn that into something the

**31:44** · agent does for you. Um and you can very

**31:47** · likely like with today's models, you can

**31:49** · very likely just ask the agent um to

**31:52** · like to do what you were trying to do.

**31:54** · Uh and the agent will figure out, oh, I

**31:56** · should do this, I should do that.

**31:57** · >> All right. Well, it looks like it's done

**31:59** · now in

**31:59** · >> Yeah, it's done now. So, uh, so now,

**32:02** · good question, right? Like it's done.

**32:04** · The agent says it's done and we can look

**32:05** · through what it did, right? It said it

**32:08** · changed this, change that. How do we

**32:10** · know this is actually, uh, a good

**32:12** · change, right? How do we know there's no

**32:14** · like bugs and everything? Um, so the

**32:16** · validation phase is where um, like I see

**32:18** · a lot of people spend a lot of their

**32:20** · time. Um so the default approach is like

**32:23** · people will open up their IDE and start

**32:25** · to review the code like they will start

**32:27** · to review the diff right. Yeah.

**32:29** · >> Um but the the thing is that uh AI can

**32:33** · write so much code. Um so if you review

**32:35** · every single line of code you become the

**32:37** · bottleneck.

**32:38** · >> Um so what I do here is I I don't even

**32:41** · review the code. Um

**32:43** · >> I don't review this uh this first pass

**32:45** · code from the agent. I use something I

**32:48** · call no mistakes. Um, so no mistakes is

**32:51** · another tool I built uh just to help uh

**32:54** · make this part of the uh my life easier.

**32:57** · Um so what it does I I'll show you. Um I

**33:00** · actually made a um alias uh so every

**33:02** · time I got some change uh like some code

**33:04** · changes done from the agent I just nm

**33:06** · and uh it will go through a few steps.

**33:09** · First it will uh ask the agent to create

**33:12** · a branch for me. Um so I don't even need

**33:14** · to think about the branch name. Um

**33:16** · otherwise I need to think about the the

**33:18** · branch name the commit message like I

**33:20** · all those things just f it's just

**33:22** · wasting time um and I get the agent do

**33:25** · that the agent basically did that fix

**33:27** · kit chat workspace that's right right

**33:30** · >> um and the agent is now analyzing my

**33:33** · session to understand my intent um so

**33:36** · the the agent here uh no mistakes is

**33:39** · reading the session uh where we did the

**33:41** · work to understand my intent uh so now

**33:43** · it's understood what I I was trying to

**33:46** · it will do the all these steps for me.

**33:48** · Uh so it will rebase my change on top of

**33:50** · the latest main branch on the remote. So

**33:53** · there's not going to be merge conflict

**33:55** · later on. Uh it's going to review my

**33:58** · change. Uh so this is where uh I

**34:00** · actually did a lot of um prompt

**34:02** · engineering to get the agents to uh

**34:05** · really scrutinize the change very very

**34:07** · hard. Um

**34:09** · >> okay. So any kind of edge case or bugs

**34:11** · uh like uh logical errors things like

**34:13** · that will get caught. Uh so this is a

**34:16** · very very high recall um uh phase. I mo

**34:21** · uh I when I initially built no mistakes

**34:23** · I did uh a lot of parallel testing where

**34:26** · I let the agents review the change and I

**34:28** · also review the change myself and see

**34:31** · how often I catch something the agents

**34:33** · uh don't right um and I use that phase

**34:36** · to uh iterate on this uh the prompts and

**34:40** · the uh the workflow within this phase so

**34:43** · eventually I got to a point where I find

**34:45** · myself never catching anything the

**34:47** · agents don't catch Um so in in this case

**34:50** · the agents act it actually didn't find

**34:52** · any uh material problems uh so it's just

**34:55** · passed but if if it found some problems

**34:58** · uh it will uh categorize that into uh

**35:01** · two categories.

**35:03** · >> One is obvious bugs. So if it's a just a

**35:06** · obvious error uh it will just autofix by

**35:09** · itself. It won't even bother me.

**35:11** · Another category is like when it

**35:13** · realized there's an error but fixing the

**35:16** · error will have some product

**35:18** · implications. Um and then it will ask me

**35:21** · instead of just autofixing that um so in

**35:24** · those cases it will escalate to me and

**35:26** · it will basically pause at this phase

**35:28** · and ask me to uh judge do I actually

**35:32** · want to make that fix or do I want

**35:33** · something else.

**35:34** · >> This is like the PR review basically the

**35:36** · agent doing PR review right?

**35:37** · >> Yeah. Yeah. a PR review between the

**35:39** · agent and the author

**35:41** · >> and this no mistakes is like a whole new

**35:43** · context window, right? It's like a new

**35:44** · agent looking at your other

**35:46** · conversation.

**35:48** · >> Yes. Uh so this is a fresh context

**35:50** · window and uh and actually did that

**35:53** · deliberately. Um I think that's an

**35:54** · important thing to do which is to use a

**35:57** · fresh context window to review the

**35:58** · change that was done. uh because uh a

**36:00** · lot of people what they do is like they

**36:02** · will just ask hey can you review the

**36:05** · change uh in the same session uh when

**36:08** · you do that the agent is very heavily

**36:10** · biased by what was already done um

**36:13** · because it it it saw all the context uh

**36:15** · it saw every every step along the way so

**36:18** · it's biased into believing that what was

**36:21** · done was correct um and it will because

**36:24** · of that it will sometimes miss something

**36:27** · um so if you uh I I I tested this a lot.

**36:30** · Um, and when you use a fresh context

**36:31** · window, you get just get a lot more edge

**36:33** · cases caught.

**36:34** · >> I guess the only problem is like uh the

**36:36** · no mistakes agent has to does it have to

**36:38** · look at your whole code base again to

**36:39** · even understand what this app is about.

**36:41** · >> Uh, that's what this intent face was

**36:43** · doing. Uh, so it basically analyzed your

**36:45** · session uh to understand what was your

**36:48** · original intent and uh some of the

**36:50** · surrounding context as well.

**36:52** · >> Um, but it's not copying the entire

**36:54** · session uh into this new context window.

**36:57** · It's like it's like you know like some

**36:59** · senior engineer builds some feature and

**37:00** · then you're asking the principal

**37:01** · engineer to come in with fresh fresh

**37:03** · eyes to look look through everything

**37:05** · right

**37:06** · >> yeah with fresh eyes but you usually you

**37:08** · will ask the senior engineer to explain

**37:10** · a little bit of context to the principal

**37:12** · right

**37:13** · >> that's right yeah

**37:14** · >> yeah so this intent phase is basically

**37:15** · that it's basically like explaining the

**37:18** · basic context of what this change is

**37:20** · trying to do

**37:21** · >> okay and why don't we walk through the

**37:23** · rest of the phases too like um

**37:24** · documenting is what is writing what is

**37:27** · obser observing.

**37:28** · >> Yeah. So, yeah. So, each phase what it

**37:30** · does is like review is just reviewing

**37:32** · the code. Um, and test is running tests.

**37:35** · Um, and the test phase is very different

**37:37** · from what the agent does by default. Um,

**37:40** · so the agent what the agent does by

**37:42** · default is running some tests. Um, and

**37:45** · uh validating locally like uh was the

**37:48** · change um was the change tested and was

**37:51** · that working. Um, but this test phase is

**37:54** · a little bit different. is more like CI

**37:56** · um it's validating did this regress

**37:58** · other things as well uh etc etc and uh

**38:02** · this test phase will actually present

**38:03** · some evidences uh evidences of uh the

**38:07** · change actually working it will paste

**38:09** · screenshots or like sometimes a video to

**38:12** · capture this thing is actually working

**38:14** · so it's easier for me to review I can

**38:16** · just look at uh the artifact and see oh

**38:20** · okay it's actually working

**38:21** · >> oh that that's actually really

**38:22** · interesting so yeah because sometimes

**38:24** · when I shift stuff with codeex like the

**38:26** · stuff I'm shipping works but then it

**38:27** · breaks some something else it breaks

**38:28** · like another core work workflow in the

**38:31** · app

**38:31** · >> so so this test base will actually look

**38:34** · through all that and try

**38:35** · >> yeah it look through all that yeah and

**38:37** · uh just like present very easily

**38:39** · digestible artifacts for me to like have

**38:42** · confidence it's actually working as I

**38:43** · expected

**38:44** · >> this is maybe a dumb question but like

**38:46** · for example I'm I'm trying to build like

**38:47** · a fitness app right and like and like

**38:49** · there's like a few core workflows that I

**38:51** · want to make sure that it tests each

**38:52** · time like creating a workout tracking

**38:54** · your workouts, you know, like so like do

**38:56** · you do you have to manually define the

**38:58** · stuff or is the AI enough smart enough

**39:00** · to figure it out

**39:02** · >> to to test the stuff each time you make

**39:03** · a change?

**39:04** · >> Yeah. Yeah. Yeah. I typically like try

**39:06** · to get AI uh the agent to turn those

**39:09** · things into an automated end to end

**39:11** · test.

**39:12** · >> Okay.

**39:12** · >> Um Yeah. Because then it will be very

**39:14** · easy to run that every single time,

**39:16** · right?

**39:16** · >> And the automated end to end test is

**39:18** · basically just like it uh lastly is like

**39:20** · a browser app. So it it just kind of

**39:21** · like actually beat the user and click

**39:23** · click through stuff, right? and see if

**39:24** · see if anything breaks.

**39:25** · >> Yes. Yes. Uh so there are various kind

**39:27** · of like end to end browser testing tools

**39:29** · like playright. Um so but but yeah you

**39:32** · can just ask the agent uh you can say

**39:34** · hey like write an end toend test uh for

**39:37** · this scenario or this user work uh this

**39:39** · user flow and make sure it's actually

**39:42** · working end to end. Uh it will typically

**39:43** · be able to figure out what kind of

**39:45** · frameworks or tools uh that needs to be

**39:46** · used. I think the trade-off here, dude,

**39:48** · is like it just takes a lot longer to

**39:51** · actually ship a feature, right? Because

**39:54** · [laughter]

**39:54** · you're running all all these stages. But

**39:56** · but I guess you have way more confidence

**39:57** · that the feature you ship actually

**39:58** · doesn't break anything. So So I guess if

**40:00** · you're like if you have a lot of users

**40:02** · because a lot of stuff I work on don't

**40:04** · doesn't have any new users. It's just

**40:05** · me.

**40:07** · >> But if you have a lot of users that you

**40:08** · ship the product, you want to make sure

**40:09** · it actually works, right? It's like

**40:11** · software engineering 101.

**40:13** · >> Yeah. So I I I would argue like even if

**40:15** · it's only for yourself, uh like probably

**40:18** · you can make the trade-off, right? How

**40:19** · much you want to u prefer just making

**40:22** · changes very fast versus making sure

**40:25** · things actually work. Um because

**40:26** · sometimes there's like a little bit of a

**40:28** · cost to you as well if things broke. Um

**40:31** · yeah, so um yeah, so this uh this phase

**40:34** · taking uh longer time is actually okay

**40:37** · because I never look at this like I I I

**40:40** · never uh just stare at this screen and

**40:42** · uh wait for every phase to pass, right?

**40:45** · Every time I uh launch no mistakes, I

**40:47** · just immediately switch to another

**40:49** · session.

**40:49** · >> Uh like I I don't even look at this. Um

**40:52** · what I uh have here um I I'll show you

**40:55** · now. I switch to another session, right?

**40:57** · I can just look at the terminal screen

**40:59** · here to see what phase uh is that no

**41:02** · mistakes pipeline uh at. So I can see

**41:05** · it's working on the linking pipeline and

**41:07** · if it's like if it's uh waiting for me

**41:10** · uh to like make a judgment or something

**41:12** · it will change the status here. So I can

**41:14** · just like very easily see do I need to

**41:16** · jump back into that session.

**41:18** · >> Do you run no mistakes after like almost

**41:20** · every change or or like if because if

**41:22** · you do that then why don't just

**41:24** · automatically run it.

**41:25** · >> Ah yeah yeah. So uh I run that on most

**41:28** · changes but not not every single one

**41:30** · because there are changes where uh for

**41:32** · example I make a very simple

**41:34** · documentation updates and I know like it

**41:37** · doesn't need like so much validation. Uh

**41:39** · it's going to use a lot of my tokens as

**41:41** · well. So I make some judgments on

**41:43** · whether the change just justifies this

**41:45** · kind of a heavy validation phase. Yeah.

**41:47** · It's kind of like Yeah. When you work

**41:49** · within a team and some of your changes

**41:52** · don't like it's not that every PR will

**41:54** · go to a QA team, right? Yeah,

**41:56** · >> only some like milestones, some

**41:58** · meaningful things will go there.

**41:59** · >> Dude, do you think it feels weird like

**42:01** · after spending you know your career in

**42:03** · big tech? Because in big tech when you

**42:05** · push a change, you have like a teammate

**42:06** · come and review your PR, right? And then

**42:08** · you run some t tests and and now you're

**42:10** · just by by yourself. So it's like

**42:12** · [laughter] so so I guess like you have

**42:14** · all these agents, but like like how do

**42:16** · you feel like do you feel like

**42:18** · unshackled or or do you feel like uh you

**42:20** · kind of miss the teammates?

**42:22** · >> I uh so it's a bit of both. Uh but I

**42:24** · would say like uh largely speaking I

**42:27** · feel liberated.

**42:28** · >> Liberated.

**42:29** · >> Yes. Uh so I I think uh teammates are

**42:32** · great uh especially in the brainstorming

**42:34** · phase. Um so when we are like thinking

**42:37** · about an idea if it's just me uh it's a

**42:41** · very like it's not a very diverse

**42:43** · perspective, right? So I may not think

**42:45** · through everything and I may not realize

**42:47** · problems others can see. Um, AI can help

**42:50** · to a degree, but I don't think AI is

**42:52** · like quite there yet to replace uh like

**42:55** · a really smart team that uh can ideate

**42:58** · together. Um, so that is like one the

**43:01** · part I miss. The part I don't quite miss

**43:03** · is like everyone is busy and if I write

**43:06** · like 20 PRs every day, no one's going to

**43:09** · reveal that. Um, so yeah, that already

**43:12** · happened before I uh left my uh last

**43:15** · company. And what I uh found myself

**43:18** · doing was like I I have to write less

**43:21** · PRs. Um Got it. And spend my time

**43:25** · elsewhere because the bottleneck is like

**43:27** · really on on the rest of the team.

**43:28** · >> Yeah. Because the your teammates aren't

**43:30** · actually reviewing the PRs. Like they

**43:32** · don't have to have a lot of things going

**43:33** · on, but like if you submit a PR to AI,

**43:35** · it's always going to start work working,

**43:37** · >> right?

**43:37** · >> Yeah. So this is something that I think

**43:39** · uh is going to like fundamentally change

**43:41** · uh as we progress on AI adoption. Um so

**43:45** · our workflows and how our teams work

**43:48** · were built uh at a time when we spent

**43:52** · most of our time coding and uh the

**43:55** · average stats of like a average software

**43:58** · team an engineer is like an engineer

**44:01** · will write 10 to 15 PRs every month.

**44:04** · That's like the velocity of an average

**44:06** · software engineer uh team. So um when

**44:09** · that's the case uh you spend like it's

**44:12** · okay for everyone else to do code

**44:14** · reviews and all these uh processes

**44:16** · because the velocity is not that that

**44:18** · massive

**44:19** · >> but when you um when you start to write

**44:21** · like 10 times more PRs we are not ready

**44:24** · for that like our processes and our um

**44:27** · like human team composition and

**44:29** · everything is not built with that

**44:31** · assumption in mind. So what's going to

**44:33** · happen is like uh things are starting to

**44:35** · break. A lot of teams are starting to um

**44:39** · change their practices in order to fight

**44:41** · that. Um so some teams es especially

**44:44** · smaller teams in startups they basically

**44:47** · stopped doing PR reviews. Um they still

**44:49** · raise a PR but mostly for like a

**44:52** · formality or for like leaving a record

**44:55** · they don't actually wait for another

**44:57** · peer to review. um they sometimes just

**44:59** · merge the PR and later on if there's a

**45:01** · problem they can go back to it. Uh

**45:03** · that's the kind of changes I'm starting

**45:04** · to see.

**45:05** · >> Yeah, they they get the agents to

**45:06** · review, right? I do think it does lead

**45:08** · to like a little bit more unstable uh

**45:10** · products. Yeah. Um but you know

**45:12** · >> uh that's because they are not using no

**45:14** · mistakes. [laughter]

**45:17** · >> Yeah, it looks like it's done.

**45:19** · >> Yeah, this pipeline just completed. Uh

**45:20** · right. So uh it went through all these

**45:22** · steps. uh and uh there was actually one

**45:25** · thing fixed in documentation phase. This

**45:27** · is uh yeah this is something I uh we can

**45:30** · look at whether uh it's actually a legit

**45:32** · change but um this is something I find

**45:34** · super useful and something both me and

**45:37** · my agents often don't do automatically.

**45:40** · Um so it's like when you make a change

**45:42** · can you actually find all the places uh

**45:45** · in our documentation that can be

**45:48** · affected by that change?

**45:49** · >> Okay, got it.

**45:50** · >> Yeah. So documentation linting uh and

**45:53** · push and create a PR. So I can just open

**45:55** · up the the PR and uh let's look at what

**45:58** · it does. So it created this PR. Uh the

**46:00** · PR summarized uh the intent uh that was

**46:03** · understood from my original session in

**46:06** · open code. Uh it summarized what

**46:08** · changed. Uh it did a risk assessment as

**46:10** · well. Um so like what this is very

**46:12** · useful as well. uh when I look at a

**46:14** · lowrisk change I spend less time when

**46:17** · the agent is flagging this is a medium

**46:19** · risk or high risk change I spend more

**46:21** · time on this PR right so I can like

**46:24** · decide where I spend my time more uh

**46:27** · intelligently um so uh and testing uh

**46:31** · yeah it did some test it had had a

**46:33** · evidence uh so let's see what this is

**46:36** · uh it renders the workspace

**46:39** · okay yeah basically like the um this

**46:42** · evidence uh is uh is about presenting

**46:44** · like actual results um from the change.

**46:48** · Uh so uh we can look at this and see is

**46:50** · that what we want.

**46:51** · >> Okay.

**46:51** · >> Um and there is the pipeline and there

**46:53** · is the documentation phase. Uh what did

**46:55** · it find? Uh it found that the design

**46:58** · system example copy was not updated.

**47:02** · Okay. Yeah. So it actually it actually

**47:04** · caught a inconsistency. Uh so that's

**47:07** · great. Yeah. So, so because it's a

**47:09** · lowrisk change, I don't even go into the

**47:12** · diff here.

**47:13** · >> I don't go there. Um, I I just merge it.

**47:16** · >> Um, okay.

**47:16** · >> And, uh, when it's a medium risk or high

**47:19** · risk change, um, then I go into the diff

**47:21** · and start to look at things myself.

**47:23** · >> Okay. But you you pretty much uh always

**47:26** · uh somewhat look at the PR, skim the PR,

**47:28** · and then you hit the button to merge,

**47:30** · right?

**47:30** · >> Yeah. Yeah. I still look at this PR uh

**47:32** · because I think looking through the risk

**47:34** · assessment and uh what the agent

**47:36** · actually did uh what was the fix uh

**47:38** · those things are actually still useful.

**47:40** · >> That's the mistake that I'm making,

**47:41** · dude. I I don't look at the PR some

**47:43** · sometimes. I just I just tell it to

**47:44** · merge. [laughter] So I just need to be a

**47:47** · little bit more thorough. Yeah.

**47:48** · >> Also after the agent made some code

**47:50** · changes, you just uh just get it merge.

**47:52** · >> Well, I actually run some tests and

**47:54** · stuff. I I don't use no mistakes and

**47:56** · then I I I I get to merge and then um

**47:59** · yeah, inherently like you know like a

**48:01** · day later I'll find something else

**48:03** · broke. So [laughter]

**48:04** · yeah, it's it's probably not the most

**48:06** · efficient way to do it. Yeah.

**48:07** · >> Uh yeah. So yeah, I think some some

**48:09** · validation and then some uh some like uh

**48:12** · review, but it's not a line by line code

**48:15** · review. I think some review on what's

**48:17** · changed and um what um kind of risks

**48:20** · exist. That's still useful. And and

**48:22** · you're probably submitting 10 15 PRs a

**48:24** · day, right? Or like doing doing this.

**48:27** · >> Yeah. So I um I I uh actually do a lot.

**48:30** · Uh so I um like [laughter]

**48:34** · 26 uh 14 27 30. Yeah, that's like the

**48:37** · average. Uh so it's uh yeah, most of the

**48:40** · time it's like 22 40 kind of PRs every

**48:43** · day. Sometimes I do more. Um like

**48:46** · >> I can I can tell I can tell when when uh

**48:48** · you became unemployed. It's like it's

**48:50** · around March. very very very clear on

**48:52** · this chart.

**48:53** · >> All right. So that so I guess we just

**48:54** · walked through the whole plan build and

**48:56** · validation process, right? Like that's

**48:57** · basically it, right?

**48:58** · >> Yeah. So uh yeah, we went through like

**49:01** · uh building a plan interactively uh

**49:03** · implementing that with the agents and

**49:05** · then going through this validation

**49:06** · pipeline. Um this basically uh if you

**49:08** · think about it, I didn't spend much time

**49:11** · in the uh coding and validation phase at

**49:14** · all. Right? Most of my time was actually

**49:16** · on the HTML artifact iterating with the

**49:19** · agent. Um so that's kind of how I um how

**49:21** · I do these things now and as soon as I

**49:24** · send the agent to do implementation I

**49:26** · just switch to something else uh and

**49:28** · work on that in parallel.

**49:29** · >> Okay so I guess we we can provide the

**49:32** · links to lavish the HTML PL planner and

**49:34** · also no mistakes the validation uh we'll

**49:37** · provide it in the description of this

**49:39** · episode. Uh I guess let dude let me ask

**49:41** · you one last question.

**49:42** · >> Yeah

**49:43** · >> I mean you you know you're like an LA

**49:45** · engineer you've been doing this for a

**49:46** · while. There's there's like a lot more

**49:47** · builders now, right? Like there's a lot

**49:49** · more people trying to get into this

**49:51** · stuff and learning how to build a AI.

**49:53** · >> Yeah.

**49:54** · >> How do you think do you have any advice

**49:55** · for people to actually ramp up the

**49:57** · technical skills and and also like what

**49:58** · kind of technical skills do they

**50:00** · actually need to learn? Like obviously

**50:02** · like testing and validating everything.

**50:04** · Uh but also there's like there's like

**50:06** · stuff like for example like if you don't

**50:07** · set up your database properly in the

**50:09** · beginning like it's harder to change it

**50:10** · later. Just like just stuff that you

**50:11** · learn over time. So, so like do you have

**50:14** · any thoughts on how people can actually

**50:16** · scale up as they build more stuff?

**50:18** · >> Yeah. Yeah, good question. Um I I think

**50:20** · there's a few things come to mind. One

**50:23** · is that uh I think just play a lot. Um

**50:26** · build a lot of things. Uh even if it's a

**50:28** · throwaway toy, uh build it and through

**50:31** · that process you will like often often

**50:33** · discover things you can do better or

**50:36** · things the agents didn't quite do very

**50:38** · well and start to reflect on that. Uh so

**50:40** · do think do a lot of things. I think

**50:42** · that's like probably the first uh step.

**50:44** · Um some people I think they uh what I

**50:47** · see at least from some people is like

**50:49** · they only they they spend a lot of time

**50:52** · trying to decide what do they do and

**50:55** · then uh they only do one thing and that

**50:57** · thing didn't work. They then they stop.

**50:59** · Um I think uh the mindset I would

**51:02** · encourage is to just like build every

**51:04** · single idea you have. Um whenever you

**51:06** · have some idea um like send the prompt

**51:08** · to the agent and see what it does. Um

**51:10** · and um whenever like you you have some

**51:13** · uh like inspiration or idea you you

**51:16** · think might be interesting um just give

**51:18** · that to the agent and have it run for

**51:20** · you. Um I think through that like

**51:22** · process uh a lot of learnings can be uh

**51:25** · derived. Um that's one. Uh another I

**51:28** · think is to um like try to challenge

**51:31** · yourself to use like more tokens and run

**51:35** · more agents in parallel. Um like I think

**51:38** · that is a forcing function for people to

**51:41** · like upgrade their workflow. Um because

**51:44** · when we by default work with one agent

**51:46** · uh at a time, we are still kind of like

**51:50** · being a bottleneck. Uh we are putting

**51:52** · ourselves into the loop too much. Um and

**51:55** · I think to really scale up um how much

**51:57** · we can get from the agents, we have to

**51:59** · like move ourselves out of the loop as

**52:02** · much as possible. Um, so that's like I

**52:05** · think using more tokens and running more

**52:06** · agents in parallel kind of forces us to

**52:09** · do that. Um, that's probably like

**52:11** · another uh thing I can think of. Um,

**52:14** · >> got it.

**52:15** · >> Yeah, maybe like the last thing is to uh

**52:17** · like try to adopt AI in every part of

**52:20** · your workflow, not only writing code.

**52:23** · Um, so what we could see there like AI

**52:25** · did a lot of validation and uh

**52:26** · documentation all those things for me,

**52:28** · right? And raising the PR and

**52:30** · everything. I don't need to do anything

**52:31** · there. Um I think um like when uh when

**52:34** · we work through a project whenever we

**52:37** · find something manual what we talked

**52:38** · about earlier like something we are

**52:40** · spending time ourselves just try to

**52:42** · think about uh can we delegate that to

**52:44** · the agent as well uh and through that uh

**52:47** · people I think we'll find a lot more

**52:49** · useful like workflows that can uh handle

**52:51** · automation and reduce our workload.

**52:54** · >> Yeah, maybe there's like some sort of a

**52:55** · skill or like some something we can

**52:57** · build where because the AI remembers uh

**52:59** · it conversations with you. Like maybe

**53:01** · the AI can actually proactively suggest

**53:03** · like hey you should auto you should

**53:04** · automate this. It's like the second time

**53:05** · we're talking about this. Yeah,

**53:09** · >> that exist that exists. So I can show

**53:11** · you um okay

**53:12** · >> so uh if I run cloud code

**53:15** · >> cloud code has this slash command called

**53:17** · insights.

**53:19** · These insights will basically analyze

**53:21** · your cloud code sessions and generate a

**53:23** · report for what uh what can be done

**53:26** · better like what can what what kind of

**53:28** · skills can you uh add what kind of uh

**53:31** · things can you tweak in your like memory

**53:33** · files etc etc to make cloud code work

**53:36** · more efficiently for you.

**53:37** · >> All right.

**53:38** · >> Oh

**53:39** · >> yeah. Yeah. So this is super cool but

**53:40** · it's going to use a lot of tokens. I'm

**53:42** · already out of tokens so I'm not going

**53:43** · to [laughter] demo that now.

**53:45** · >> Yeah.

**53:46** · >> Yeah. But this is something I definitely

**53:48** · recommend people trying. This is a very

**53:50** · cool thing.

**53:50** · >> Okay. Yeah. I'm going to write right

**53:52** · now. Um yeah, I I I think the token

**53:54** · maxing thing is kind of like a meme. But

**53:56** · I think basically like just summarize

**53:58** · your advice. Number one is like putting

**54:00** · the reps like try different things, try

**54:01** · to build different things. Number two is

**54:03** · like if you use multiple agents, you can

**54:05** · put in more reps, right? Because you

**54:06** · don't have to wait for one a agent to do

**54:07** · anything.

**54:08** · >> Yeah.

**54:08** · >> And then and and then the third one is

**54:10** · is u sorry what was the third one again?

**54:13** · >> Part of your Yeah. Not only writing

**54:15** · code. Yeah, I think the second one is

**54:17** · especially hard, dude, because like I

**54:19** · don't know like growing up as an Asian

**54:20** · person, I have like a scarcity mindset.

**54:22** · I try to save money and stuff and

**54:24** · [laughter]

**54:25** · >> and like just trying to burn our tokens.

**54:26** · It doesn't feel it doesn't feel right.

**54:29** · >> Uh but there's a so most of us uh like

**54:32** · working as individuals, we have uh the

**54:35** · subscription, right?

**54:37** · >> So at least try to make the most out of

**54:39** · the subscription and exhaust the quota.

**54:42** · >> Okay. Yeah. So, I guess it's kind of

**54:43** · like going to a buffet and like trying

**54:45** · to eat all the crab legs. [laughter] I

**54:47** · guess I can.

**54:48** · >> Yeah. But I I I I would say like uh

**54:52** · there's the token maxing thing. Uh I I

**54:54** · think uh we shouldn't just use tokens

**54:56** · for the sake of using tokens, right? We

**54:58** · want to get actual work done. Uh so I I

**55:01** · think uh it's more about pushing

**55:03** · ourselves like my my point about number

**55:05** · two was more about pushing ourselves to

**55:08** · figure out ways to scale up um and

**55:12** · really like get more done with agents

**55:14** · instead of uh finding ourselves into the

**55:16** · loop and only do one thing at a time.

**55:18** · >> That makes a lot of sense. That makes a

**55:19** · lot of sense. All right, cool. Well,

**55:21** · thank thanks so much, man. Uh where can

**55:22** · people find your like all the free stuff

**55:24** · you've been shipping and also yourself?

**55:26** · >> Yeah. Yeah. So I'm very active on uh X

**55:29** · and YouTube. I'm I plan to share a lot

**55:32** · of my workflows and tools and setups

**55:34** · over there. Um and I also uh my GitHub

**55:37** · uh is also a good place uh to uh look at

**55:40** · my projects.

**55:41** · >> Your your GitHub is just uh slashkun,

**55:43** · right?

**55:44** · >> Kungchan GUID. So I I have this uh let

**55:46** · me uh let me move my window here.

**55:48** · >> Oh, there is. Yeah.

**55:48** · >> Uh yeah, this is my uh handle almost

**55:51** · everywhere. Uh so uh YouTube X and

**55:54** · GitHub, LinkedIn, it's all this handle

**55:57** · UID.

**55:58** · >> Yeah, I think it's like a blessing to

**56:00** · all of us that you're shipping all the

**56:01** · stuff for free and like we can all try

**56:02** · it. So uh yeah, I'm definitely going to

**56:05** · try no mistakes and um you know every

**56:07** · everything else that you built.

**56:09** · >> Cool. Cool. Thanks, Peter. Yeah, if you

**56:10** · run into anything, let me know. I I I'm

**56:12** · constantly trying to improve these tools

**56:14** · as well.

**56:15** · >> Cool. All right, take care, man. Bye.

**56:17** · Fitter.
