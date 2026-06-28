---
title: "Introducing /visual-plan - rich plans for Claude Code + Codex"
source: "https://www.youtube.com/watch?v=NE0aBuQF0HA"
author:
  - "[[Steve (Builder.io)]]"
published: 2026-06-16
created: 2026-06-28
description: "Grab the skill + source here: https://github.com/BuilderIO/skills Visual MDX editor source here: https://github.com/BuilderIO/agent-native"
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=NE0aBuQF0HA)

Grab the skill + source here: https://github.com/BuilderIO/skills
Visual MDX editor source here: https://github.com/BuilderIO/agent-native

## Transcript

_Caption track: English auto-generated or provided._

**0:00** · Plan mode in Claude code is incredible,

**0:01** · but I always find my eyes glazing over

**0:03** · this huge markdown essay in my terminal.

**0:06** · And I've realized after I implement

**0:07** · things that I totally miss some

**0:08** · important small details that were not

**0:10** · clear to me at first because it was just

**0:12** · too much stuff to read, honestly. I've

**0:14** · been experimenting with this new skill I

**0:15** · made called visual plan. It's somewhat

**0:17** · inspired by that post about how HTML is

**0:19** · better than markdown, but HTML can be

**0:20** · slow and verbose to write, it doesn't

**0:22** · look good checked into a repo, and I

**0:24** · found I can make much better visual

**0:25** · plans with reusable components. So, I

**0:27** · made a skill called visual plan. It

**0:29** · generates plans as MDX with super visual

**0:32** · components, diagrams, API specs that are

**0:35** · interactive, schema design changes,

**0:37** · annotated code, and even pan and

**0:39** · zoomable wireframes. Every UI lets you

**0:41** · look at a wireframe first, comment on

**0:43** · it, iterate, answer open questions

**0:45** · visually and interactive, and then have

**0:46** · the agent work. I found this to be a

**0:48** · much more intuitive interface for me to

**0:50** · reason about what the agent's doing.

**0:52** · It's really made me feel like humans and

**0:53** · engineering is kind of entering this new

**0:55** · abstraction phase where we reason about

**0:57** · things at the plan level. As long as the

**0:59** · plan's what we want, agents are getting

**1:00** · more and more reliable executing on

**1:02** · that. Almost to the degree to which we

**1:04** · trust the C compiler to compile to

**1:05** · assembly reliably. As long as the plan

**1:07** · is good, and we make the plan clear,

**1:09** · consumable, like easy to understand,

**1:11** · easy for people to reason about, share,

**1:13** · comment, etc., more and more we can

**1:14** · trust the agents to implement it as

**1:16** · expected. I also made a skill for the

**1:17** · reverse of this. I call it visual recap.

**1:20** · What it can do is after the agent works,

**1:22** · give you a recap of everything it did.

**1:23** · The same idea. Wireframes, interactive

**1:26** · API specs and diffs, schemas, annotated

**1:28** · code, etc. So, now when you're reviewing

**1:30** · what the agent has done for you, or

**1:32** · looking at like a pull request for

**1:33** · somebody else's code, rather than

**1:34** · looking at a small summary, or a super

**1:36** · granular line-by-line mess, you can see

**1:38** · a visual recap. Interactive, easy,

**1:40** · intuitive. You can even share these with

**1:42** · others to comment, and then pass the

**1:43** · comments and feedback to the agent to

**1:45** · improve. This has let me catch stuff way

**1:47** · sooner. So, before the agent does

**1:49** · something I didn't realize, because

**1:51** · maybe the text sounded fine, but the

**1:52** · wireframe makes me realize, "Oh, wait.

**1:53** · No, that's not what I had in mind." Or

**1:54** · in just a more clear and visual way, I

**1:56** · see what types of APIs I want to create.

**1:58** · And I'd like them shaped differently.

**2:00** · I'm able to catch stuff earlier as well

**2:02** · as afterwards in recaps of my work or

**2:04** · someone else's work. I can match your

**2:06** · things that maybe aren't as obvious in

**2:07** · the code, just looking at like React and

**2:09** · Tailwind code, are actually what I

**2:11** · wanted or expected before it goes out to

**2:13** · production and I'm trying it out and

**2:14** · going, "Oh, wait a second. This is not

**2:15** · what I had in mind. That's not what I

**2:16** · thought I told the agent. That's not

**2:18** · what I thought I saw in the code." And

**2:19** · I'll be honest, it's tedious to

**2:20** · hand-test every single thing every time.

**2:23** · Having a snapshot at a glance that's

**2:24** · clear and I can interactively drill

**2:26** · into, to me has been a game-changer

**2:28** · compared to just static markdown. And

**2:29** · all of this stuff is customizable. You

**2:31** · can add your own components, customize

**2:32** · the components. It's MDX. It's a better

**2:34** · format for checking in. It can do way

**2:35** · more cool things, and there's

**2:37** · consistency, too. It's not just random

**2:38** · HTML every time. This move to MDX from

**2:41** · HTML from previously markdown, I think

**2:43** · is the full circle that at least I

**2:44** · needed. I'd much rather see MDX raw

**2:47** · files in code versus HTML. And there's

**2:49** · so much more you can do with reusable

**2:50** · components than generating honestly kind

**2:52** · of HTML slop every time, different every

**2:54** · time. It also means when you change

**2:56** · agents or models, you get consistency as

**2:57** · well. I open-sourced all of this. The

**2:59** · skills, the application that generates

**3:02** · MDX that you can fork and customize with

**3:04** · your own components. You can check it

**3:05** · out over on GitHub, install and try it

**3:07** · out with the CLI I made, and I'd love to

**3:09** · know your feedback. Not just on do you

**3:10** · like the plans or the recaps or is it

**3:12** · handy, including the fact that you can

**3:13** · install a GitHub action with the CLI,

**3:15** · but also does this new idea of like how

**3:17** · we reason as engineers make sense. I

**3:19** · really believe that the plan level is

**3:21** · really the real reasoning level that

**3:23** · we're going to be thinking in, talking

**3:25** · in, and working in. And I want to make

**3:27** · it clear and beautiful and a good

**3:28** · experience. So, as we trust agents more

**3:31** · to implement correctly and other agents

**3:32** · check the work against the plan, against

**3:34** · the implementation spec, we can work

**3:36** · faster, we can get our minds out of the

**3:37** · details. Like how people don't look at

**3:39** · assembly much anymore. They would reason

**3:41** · at the level of C and that opened up all

**3:42** · new potential and abstractions and the

**3:44** · ability to move fast relative to before,

**3:46** · but safely. And I think this opens up

**3:48** · new ways of collaborating. You can share

**3:49** · the same thing with your product

**3:50** · managers, designers, et cetera, making

**3:52** · it so you reason about it similar to

**3:54** · you. At least the areas that care about

**3:55** · like the design or the wireframe and the

**3:57** · PM about the behavior. And one more

**3:58** · thing I think is cool is there's also a

**4:00** · GitHub action I made that can run this

**4:02** · automatically on every pull request and

**4:04** · show you a snapshot of a visual plan

**4:05** · right there in the comments every time.

**4:07** · You can click in and interact with to

**4:09** · make it easier more consumable to review

**4:11** · pull requests. So again, it's not just a

**4:13** · choice between a short description and a

**4:15** · long granular line by line, but actually

**4:17** · see visuals, diagrams, interactive API

**4:19** · specs, more consumable code and even

**4:22** · annotated code. Anyway, it's all free

**4:23** · and open source you can find on my

**4:24** · GitHub. Let me know what you think.
