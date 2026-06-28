---
title: "Anthropic, OpenAI, and Microsoft Just Agreed on One File Format. It Changes Everything."
source: "https://www.youtube.com/watch?v=0cVuMHaYEHE&t=1s"
author:
  - "[[AI News & Strategy Daily | Nate B Jones]]"
published: 2026-03-30
created: 2026-06-27
description: "My site: https://natebjones.comFull Story w/ Prompts: https://natesnewsletter.substack.com/p/your-ai-skills-fail-10-of-the-time?r=1z4sm5&utm_campaign=post&utm_medium=web&showWelcomeOnShare=true_____"
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=0cVuMHaYEHE)

My site: https://natebjones.com  
Full Story w/ Prompts: https://natesnewsletter.substack.com/p/your-ai-skills-fail-10-of-the-time?r=1z4sm5&utm\_campaign=post&utm\_medium=web&showWelcomeOnShare=true  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
What's really happening inside the skills ecosystem when agents now call skills more often than humans do?  
  
The common story is that skills are just personal configuration files from October — but the reality is that skills have become organizational infrastructure, and most teams haven't updated their approach to match.  
  
In this video, I share the inside scoop on how to build agent-readable skills that actually compound:  
  
• Why the description field is where most skills go to die  
• How agent-first design changes handoffs and contracts  
• What three-tier skill architecture looks like for teams  
• Where community repositories fill the domain-specific gap  
  
Builders who keep treating skills as glorified prompts will miss the compounding advantage — the practitioners who version, test, and share skills are pulling ahead every week.  
  
Chapters  
00:00 Skills launched in October, everything changed since  
02:30 Four big trends reshaping the skills landscape  
05:00 Skills compound, prompts evaporate  
07:00 The specialist stack pattern in production  
09:30 Real estate GP with 50,000 lines of skills  
11:30 How to build a skill that actually works  
14:00 The single-line description gotcha  
16:00 Methodology body: reasoning over procedures  
18:00 Agent-first skill design principles  
20:30 Descriptions as routing signals, outputs as contracts  
22:30 Three-tier skill architecture for teams  
24:30 The community skills repository announcement  
26:00 Skills are what persists  
  
Subscribe for daily AI strategy and news.  
For deeper playbooks and analysis: https://natesnewsletter.substack.com/  
  
Listen to this video as a podcast.  
\- Spotify: https://open.spotify.com/show/0gkFdjd1wptEKJKLu9LbZ4  
\- Apple Podcasts: https://podcasts.apple.com/us/podcast/ai-news-strategy-daily-with-nate-b-jones/id1877109372

## Transcript

### Skills launched in October, everything changed since

**0:00** · Anthropic launched skills back in October and what has changed since then in the rest of the world of LLMs and agents and open claw has shifted how we think about skills, but I don't think we've really caught up on that because most of the time when we're talking about agents, we talk about open claw.

**0:13** · What we don't realize is that skills are becoming the substrate for a lot of the correct persistent accurate predictable outcomes that businesses and frankly we people need to get stuff done.

**0:25** · But we keep thinking of skills as those individual things that launched back in the fall. And so this is really a get you up to speed on agent readable skills video. If this is a new concept to you, stick around. We're going to talk through the key changes that have unlocked since October and we're also going to be talking about practical ways you can build skills and yes, I have a skills repo. It's not just going to be my skills.

**0:50** · We're going to have folks from the community throwing skills in there and it's going to be a place where we can start to learn together how to build skills that help us all get meaningful work done. All right. What changed first? Number one, the big trend. Skills went from personal configuration six months ago to organizational infrastructure today.

**1:09** · Back in October, a skill was something you built for yourself. You typed in the prompt, you did the thing. Now, team and enterprise admins are rolling out skills workplace wide. They're treated as a single upload. They're version controlled. They're available in the sidebar and callable inside Excel, inside PowerPoint, inside Claude, inside Copilot. Your organization's methodology is no longer individuals carry skills in their head. It's now how can we start to think about skills as something that is agent readable and human readable across the entire infrastructure layer. Second, the caller of skills has changed.

**1:41** · I think we slept on this one. Humans were the caller of skills in October by and large. Now, the majority of skills are called by agents. Why? Because agents can make hundreds of skill calls over the course of a single run. We humans were calling maybe a few skills in a particular conversation. The math just doesn't math for humans. We need to start thinking about our skills as agent first. Third, skills are not a developer thing. This is something that people kind of had their minds blown by when I talked about skills when they first came out, and I'm just going to underline it.

**2:14** · They're not meant to just live in the terminal. They're not meant to just be skills to execute code with. They are meant to be things that you can use for the rest of your business life, and frankly, the rest of your personal life.

**2:25** · And big companies are agreeing, right?

**2:27** · So, Anthropic and Microsoft have a partnership to bring skills to Copilot.

### Four big trends reshaping the skills landscape

**2:31** · You have skills appearing when OpenAI makes releases because skills is now an open standard. Fundamentally, you need to start thinking of skills as a common infrastructure vehicle that is just going to underlie a lot of the way AI works for the foreseeable future.

**2:47** · Fourth, skills becoming a cross-industry standard means that we need to think about the way Alpha works in the age of AI a lot differently. We're used to the concept of Alpha being closed source, where open source stuff just isn't valuable. I talked a few days ago about the idea that one of the places where you see extraordinary value if you're an engineer right now is by open sourcing a project you're building that is in the agentic AI space because then everybody can see it, see that you're high-grade talent, it functions as a resume, then they make you a big aqua hire offer.

**3:17** · In the same way, you would think that skills as markdown would be something that a lot of people would want to keep closed source. But what you see is that people are trading skills like they're trading baseball cards at camp. We're all learning together. We're figuring out how to make skills work for our agents as a community. I don't just mean my community, I mean the internet as a whole, and we are learning how to make a lowly markdown file actually function as an agent callable context layer for the work that we want to get done.

**3:48** · We We to learn it collectively because the best practices are discoverable, not known, right? When I got a CD-ROM from Microsoft and it had the entire program printed on it back in the '90s, the program was known. You got the instruction book. With LLMs, we all discover the instruction book together, and that goes for how we use them with tools and skills as well. We all discover it together, and so it works faster if we discover it in a community.

**4:14** · And so that's what I want to talk about.

**4:15** · I want to talk about specific examples of people who are using skills today, how they're using them in ways that make sense in this adjunctive future, how you start to construct adjunctive skills, some of the things that I am seeing that no one else is talking about, and kind of why that is, and then I want to get into some concrete actionable steps, things you can do to level up your skills practice. Okay, first, just the 10-second version, a skill is a folder with a text file in it. That is it. It has one required file, just skill.markdown, and it just has two parts, right?

**4:43** · It needs to have a little bit of metadata at the top, and it needs to have your methodology and instructions below. Now, in this video, there are some gotchas, right? I'm going to get into some of the gotchas that you run into when you start to build these files, and things that we know that break based on the community of learning we've had over the last 6 months. But that's the simple version, right? That's what it does.

### Skills compound, prompts evaporate

**5:03** · And all it does is it encodes a series of plain English instructions that give an LLM context to do something useful for you with a particular set of inputs in a predictable way. So, this is a very simple primitive. It's simple, and yet it has so much power because you can make a skill about just about anything.

**5:24** · And so you might wonder, what are people making with these skills? Well, the most common production pattern in Claude right now is what I would call the specialist stack. So, a developer can drop a folder full of skills into a project. One skill might turn vague instructions into a PRD, another one decomposes the PRD into GitHub issues, another one helps you write the tests for the code. You get the idea. And the whole concept of this is that it that the skill takes a lot of the nuance and the pain out of prompting, which is something I called out at the top when skills came out is that this loosens up a lot of the requirement around strict prompting that we had in 2025.

**5:55** · Because now the developer that drops that skill package as their specialist substrate basically tells the agent in cursor, "Hey, build me this feature." And then cursor can invoke the skills with their chosen LLM and just get to work. In other words, the agent doesn't need specialist direction cuz the specialist direction is in the file. Now, you can take this right out of the developer context and do a lot of other things with it. I want to give you an example of a real estate GPE known as Texas Paintbrush on X, who built the same pattern for operations at his business.

**6:27** · He has over 50,000 lines of skills across 50 repositories covering rent roll standardization, comps analysis, cash flow handling, handoff protocols between team members, the agent running.

**6:39** · And what's beautiful about it is yes, the agent can run and call those skills and predictably do operations in his business. But it turns out that writing all that stuff down also helps the humans. When he onboards someone new, there's a fantastic context layer of skills for them to dig into and understand what the heck is going on.

**6:55** · The methodology doesn't live in someone's mind anymore, it lives in a repository. And it gets more sophisticated than that. You can have orchestrator skills, and more sophisticated teams are building them now. So, a good example, this one's documented all over Reddit. You can have a skill called something like orchestrator for lack of a better term that analyzes any incoming request, and then spawns different sub agents to take care of that request based on skills that it learns to call from that master orchestrator skill, right? It might tackle research, it might tackle coding, it might tackle UI or docs.

### The specialist stack pattern in production

**7:26** · And so a single high-level request for an agent can get reliably sort of phone treed out to a bunch of sub agents to get work done because the orchestrator skill makes that predictable. And the beautiful thing about skills becoming a substrate is that when you start to work with them, you get the benefit of the entire ecosystem coalescing around them.

**7:47** · So, they work the same way in Excel as they work in PowerPoint, as they work in Copilot, as they work in Claude, as they work in ChatGPT. Everybody uses them.

**7:54** · And so, it's worth it. Now, if we circle back to the prompt pattern, I talked a little bit earlier in this video about the idea that in October, prompts were something that became somewhat less important for individual tasks because we could get predictable results by taking our best work and packaging it into skills. Still today, people will take examples of their best work, and they will say, "Please turn this into a skill so I can produce this output reliably." I've done it myself. I showed you examples, etc. Well, here's the thing that I want to underline for you.

**8:23** · We have had 6 months of this. The people who have been building with skills have been compounding them, right? Because you can improve your skills. You can say, "Okay, this this isn't right.

**8:32** · Please update your skill file with X or Y because I don't like this." And you're honing and you're refining what that skill can produce. And the people who have been prompting all along are just copying and pasting the same stuff. In other words, skills compound for you.

**8:47** · Skills compound by the weight of industry investment in the ecosystem, and by the weight of your own commitment to having a predictable pattern for doing something and writing it down.

**8:56** · Prompts don't compound in the same way.

**8:59** · Prompts are excellent. There is still value in learning how to prompt well, no doubt about it. But, prompts are becoming the basic 4x4 building block of LEGO for the rest of the world. You still have to have the specialized LEGO blocks to build the rest of the castle that you want to have. In the same way, you're going to need to figure out how to go from just prompting to skills that you can reuse.

**9:21** · And so, if this is something that's a new concept for you, we're going to just leapfrog you through and get you to agent-readable skills and some of the common pitfalls along the way. So, how do you build a skill that works? Number one most important thing, the description is where most skills go to die. What makes a bad description is vagueness. If you write, it helps with competitive analysis, that tells Claude absolutely nothing useful. It's too diffuse to match anything very specific, and it triggers on anything tangential.

### Real estate GP with 50,000 lines of skills

**9:51** · It's just not very helpful. A good description names the document types or the artifact types it produces. It includes actual trigger phrases like, "Analyze our competitors." or "Who are the players in this market?" It states what the output should look like.

**10:05** · Anthropic's own guidance is actually very explicit here. On average, skills tend to under-trigger versus over-trigger, and so they want you to write descriptions that make the skill pushy, so Claude is confident to use it.

**10:19** · Now, this is where I list one of those gotchas I was talking about. A technical constraint worth knowing is that a skill description must must must stay on a single line. If a code formatter were to break the skill description into more than one line, Claude will not read that correctly. Claude will not read the second line, and you're going to be in trouble. Now we come to the next part, the methodology body, right? This is where you say, "Once you invoke the skill, what are we going to do with it?"

**10:46** · It needs five things. First, it needs reasoning, not just steps. So, give Claude your frameworks, give it your quality criteria, give it the principles behind your decisions. A skill that only has linear procedures is a very very brittle skill. It's going to break when it hits a case that it doesn't recognize. Reasoning helps Claude generalize in this domain. Number two, you need a specified output format. Not "Produce a summary." That's too vague.

**11:13** · Is it markdown? Is it an Excel? Is it a PDF? Does it have exact fields or sections you want to cover? Be specific here, or else you're going to regret it.

**11:22** · Three, please please please give explicit edge cases to Claude.

**11:26** · Everything that a human handles through common sense, you need to write down. Do not Do not assume the Claude is going to work like an experienced human and just know those edge cases. Claude will not do that. You need to write your edge cases down. Number four, make sure that you give Claude an example to pattern match against so it knows what good looks like. That's why you can have more than one file in the skills folder. And I know this is going to sound counterintuitive because I just listed a bunch of things, keep the skill lean.

### How to build a skill that actually works

**11:54** · A short skill that fires reliably is going to out perform a long skill with competing instructions. And so you also need to be disciplined to recognize when enough is enough. And I'm going to give you some tips like I've written a lot of skills, you should not under most circumstances be spending more than 100 or 150 lines in your core Claude skills file.

**12:19** · Like and you can have a couple of examples in in other files in the folder, but it should not be a big folder that Claude has to get into and blow it up its context window with. And you should be investing 80% of your attention in that description field to make sure it triggers right and then the other 20% in being very very clear with the general purpose reasoning and making sure that Claude understands what to do and how to reason across this body once it accurately triggers. And then everything else, I mean that can go into the last few percentage points. Like you can say, "Okay, here's some edge cases, here's a good example." And don't overdo it.

**12:52** · Because those are the things that cause Claude to accurately trigger. And by the way, I say Claude because it's native to Claude, but that's the same for chat GPT, it's the same for co-worker, it's the same. Anywhere you're going to invoke it, you need to be clear in your trigger and you need to be clear in the general purpose reasoning so that the LLM knows how to reason across the space. Now, here's the thing that people aren't paying attention to. Remember how I said one of the biggest changes for skills is that they are now more agent callable than human callable. Well, that means failures are different now.

**13:24** · Because in the past, when you saw something drift as a human, you could correct it right then and adjust the skill. I actually talked about that earlier in this video. Now, the agent is going to try to use the skill to get a job done, and there may be no recovery loop if the agent gets it wrong, and that can be very expensive. And so, one of the things that you need to do, especially if you are considering using agents to drive skills, is that you need to start quantitatively testing the performance of your skills to make sure they are ready for agents.

**13:54** · You need to have a test suite that you run against your skill. You need to change it. You need to have a basket of tests. The more seriously you take your agent pipeline, the more seriously you should take the ability of your agents to call useful tools. And skills are king among useful tools. You should be able to give your agents skills that are battle-hardened.

### The single-line description gotcha

**14:17** · They should be tested, and they should be quantified. And if you don't know what that means, I'm kind of describing it for you. You need to run a basket of tests, quantify the results, change the skill like a version number, and then come back and see if it does a better job. Skills don't always change in predictable ways. The wording in skills triggers certain parts of a transformer model's latent space and enables it to respond in ways that are hard to predict.

**14:45** · And so, when you start to mess around with how do I say beautiful for a PowerPoint, for example, you may need to run through three or four different wordings to get the exact response set that matches your company's aesthetic, even with examples. And you know what?

**15:03** · Take the time to do it, because if you get it right and you're producing 100 PowerPoints a week as a company, it's going to save you a lot of time. Now, I want to go a little bit farther on agent-based design, because I don't think we named this enough. If you're designing skills specifically for agents, you're not just testing them.

**15:18** · You're starting to think about agents as the primary caller, and that changes how you think about the structure of the sections of the skills. The description becomes a routing signal, not a label.

**15:29** · You are basically telling the agent through that little description where it should go in the workflow. So, your description should contain wording that matches the outcome the agent has been given to look for in its goal, right?

**15:40** · You need to tie that together more specifically. Number two, agents need contracts. They're gold against contracts. They think in terms of contracts. You need to frame the output of the skill as a contract. And think of this, if you're a developer, as an API contract, where it's like, this is the SLA, this is what this particular thing gives you, uh these are the controllable fields, etc.

### Methodology body: reasoning over procedures

**16:01** · In the same way, the agent needs to look at the skill and says, this is what I'm going to get with this skill, this is what I won't get, and this is what this skill will allow me to accomplish, and this is where I can go against a particular goal with this skill. That is what I mean by a contract. It's essentially a declarative agreement that the agents can easily discover about the skill that allows the agent to make a correct choice confidently. Third, and we didn't think about this in October cuz we didn't have agents the same way. Composability needs to be at the core of agent-first skills.

**16:35** · In other words, don't think of the skill as solving a problem per se. Think of the skill as needing to produce an output that will need to be handed off down the chain to an agent or sub-agent that's doing something else with it. If you're going through a business process where ticket is having to go through multiple steps and an agent is having to process it, you need to think about it each step.

**16:54** · If the agent calls a skill, is the output generated by the agent working with that skill something that is correct to hand to the next agent, or correct to hand down the process for the agent to then read, understand, and call another skill if necessary? Think through the end to end experience of agents and skills, because if you don't, if you just think about it as one output, you're likely to have breaks in your hand-offs. Last but not least, and I say this a lot, hardwiring matters.

**17:22** · If you are trying to hardwire agentic behavior, please use scripts. Don't use skills. Skills are just plain English.

**17:34** · Agents will respect them. Agents will often follow them. But if you really want to hardwire, go more deterministic.

**17:40** · Go into the scripting world. And don't be shy about it. It doesn't mean you're bad at AI. It just means you know what AI can do. Part of why agents are powerful is they are general-purpose tools to solve larger sets of problems.

**17:52** · That doesn't mean we can't invoke deterministic tools along the way as a part of our overall solution. So, that's how we think about agents and skills.

**17:59** · How do we think about teams and skills?

### Agent-first skill design principles

**18:01** · And this is actually important because we're doing teams with humans and agents together now, right? Our teams are now composed of a mixture of artificial intelligence and humans for a lot of our business process. In that world, what skills do is they act as immediately actionable context. I am not the person who's going to sit here and tell you your whole context layer needs to be skills. That's obviously incorrect because so much context isn't skill-shaped.

**18:26** · But, where you need stuff done, and so much of work is about processing and going on to the next thing, skills are often a really handy way to document that as long as you do so in a way that an agent can call in a context-efficient way a particular correct skill and get a particular correct result. And as long as humans can also read it, which is one of the powerful things about Markdown. It's both agent and human-readable. I want to suggest for you that high-performing teams have three tiers for the way they handle skills.

**18:56** · Tier one are what I call standard skills. They're pretty consistent across the organization.

**19:01** · Brand voice goes in here. Formatting rules, approved templates, you get the idea. The thing we do the same all the time. Those skills are very consistent in team and enterprise accounts in a lot of AI including Claude. I think Copilot does this. You can provision those skills widely, right? You can say our brand voice is this. This is our brand voice skill. Everybody use it. Makes perfect sense. A lot of people are doing it. If you're not doing it, think about doing it. Number two, methodology skills. That's the second tier.

**19:28** · This is how your org or your team performs high value work and you want to do it predictably. It's like how you structure your client deliverables or how the senior practitioners tend to get their work done. What makes their craft tick?

**19:42** · Think of tier two skills. Think of these methodology skills as what are the things you would want to communicate to a new hire that would take them months to learn otherwise. That's a good example of something that should be a tier two skill. And by the way, that is not something that is easy for an enterprise admin to roll out because enterprise admins do not tend to be privy to the kinds of skills that are tier two high craft methodology skills.

**20:07** · Those tend to live inside senior practitioners' heads on individual teams across your company. And they need to get out of those heads and into something that is more shareable.

**20:16** · Because that is often where there's a lot of alpha, right? If you can have the practitioner skill from the most skilled product person on the team, the rest of the PM team would benefit. Ditto engineering. Ditto ditto customer success. You get the idea. Now, tier three, and this is something that a lot of us are doing, it's personal workflow skills. Things that we do that are sort of under the desk that help us with our day-to-day. We need something that is maybe team legible at best, but we're not actually surfacing this for org productivity.

### Descriptions as routing signals, outputs as contracts

**20:42** · One of the things I want to caution you about when you come to tier three skills, is that it will be tempting to keep them just on your laptop, right? Just under the desk, just in a downloads folder somewhere. Please try not to do that. And the reason why is that you don't know when you're going to be on vacation or you're going to be sick or something's going to happen at work and you're going to wish somebody could use the tool the way you designed it to be used and get the job done. And instead, they're going to have to dig around and swear and ask for your password and who knows what to get the skill work.

**21:12** · And you want to think more and more and more systemically. Think of your world as essentially actions or processes that skills can capture reliably that humans or agents can read.

**21:25** · And then what is the level of access you want for that expertise? Skills essentially encode expertise. Now, you might be wondering when there's so many skills marketplaces when there's lots of skills GitHubs, why should Nate start another one? It's a fair question. I think the simplest answer is this. We have lots and lots of skills if you are a technical engineer. We have lots and lots of sort of domain starter pack skills. What I think we're missing is domain specific skills for solving real problems.

**21:52** · So when I give examples of like that the Texas property guy who's doing rent rolls analysis, that is a domain specific skill. That is something that you are not likely to find kicking around a random GitHub repo.

**22:05** · And so I think that one of the interesting opportunities because we have such a wide variety of domains represented inside the community is to say, let's all get together and let's share the skills that we are finding useful that really add extraordinary amount of value for us and then let's all trade our baseball cards, right? And get the skills that we need and start to learn from each other. This is exactly the approach that we took when we put Open Brain over on GitHub. And this is actually going to live as a section of Open Brain.

### Three-tier skill architecture for teams

**22:35** · So if you use Open Brain, this is going to integrate right into Open Brain for you. And it's going to be super easy. It'll be in the same GitHub repo and you can call it in. Not going to be a problem. You know, Simon Willison wrote back in October that he thought skills would be were going to be a bigger deal than MCP. I think that he may be right, but right now, I don't think we have the fluency to make that happen.

**22:55** · And part of why I'm making this video is I think that we are in particular sleeping on where skills need to evolve to, where our fluency of creating skills needs to evolve to in order to get to a point where we have skills that are a truly actionable context substrate for agents and humans.

**23:13** · That's where I want to go, and that's why I'm creating a community skills repository. It's It's just a practitioner library. It has knowledge work. It's organized by workflow type.

**23:21** · You'll have an agent readability bar that's applied consistently for every skill in there, so they'll be vetted.

**23:26** · And we're going to get into stuff like competitive analysis, like financial model review, like deal memo drafting, like research synthesis, like meeting synthesis, stuff that's very, very specific, and we're going to be as widespread in our coverage as possible, so that you can invoke from the command line the skill that you care about, so that you can add from that skill pack only the skills that you need, and feel confident that you've got something that has some of that agent readability bar built into it. Now, I want to leave you with a few actionable tips. I think it's often easy to get lost here.

**23:54** · Number one, if you are struggling with where you start on skills, if all of this GitHub repo stuff feels over your head, look at something that you have repetitively done and ask yourself, if I do this once a week, twice a week, three times a week, can I get this turned into a skill? And then talk with your AI, your preferred AI, honestly, they can all do skills now, and ask it to help you make a skill.markdown from the conversations you've had and feed it that info from those conversations, what you thought what went well, what you thought you didn't, and be off to the races.

**24:25** · Now, if you're a little farther along, if you're like, "No, I get it. I'm at the GitHub repo. I can't wait." Think on your terms about your agent readable skills and ask yourself, are you thinking through those hand-offs? Are you thinking through the eventual output? Are you structuring your skills more around the idea of a contract? Those are things that I think we are sleeping on right now for skills, and I think we need to take them more seriously. If you are looking at the teams or enterprise level, think about the tiering I talked about, right? Is this an individual skill? Is this something that represents the expertise of the best person on your team?

### The community skills repository announcement

**24:53** · Is it more something that is just a brand standard that needs to be there everywhere in the org? That shapes how you deploy it and how you think about it. I am going to come back to something I mentioned earlier in this video. The thing that matters about skills is that they compound. Skills essentially represents a learned record of successful execution of a workflow that an agent or human can follow.

**25:15** · And if you continually evolve it as you get better at doing that thing, you are going to have a rememberable way for future smarter agents and for your team in the future to execute that skill along the way. To execute and build without going back to prompting. You are going to free yourself from copy-paste hell. And that's really what skills do, right?

**25:40** · Prompts just sort of evaporate. Once they're gone from the conversation, they're gone. You have to repaste them.

**25:44** · You have to dig in the prompt library.

**25:46** · Skills are what persists. And so getting them right, especially in a world where agents are now calling skills more than ever, that matters. Good luck. I hope these tips on skills are useful. I did not find a lot I dug around for this and so many of the tips on skills are focused on individual productivity. I wanted to cover the whole gamut here. I wanted to get into teams. I wanted to get into agents. I wanted to get into specific things that people are finding break and things that people are finding work. So, stick this transcript into chat GPT if it's been a lot. Parse it through and then come back with something actionable you can take away this week. Cheers.