---
title: "One markdown file just fixed AI coding forever."
source: "https://www.youtube.com/watch?v=NVkRkioBXQc&t=28s"
author:
  - "[[Agent Zero]]"
published: 2026-06-08
created: 2026-06-27
description: "DOX GitHub:https://github.com/agent0ai/doxDOX is a self-documenting AGENTS.md framework that makes AI coding agents more efficient, reliable, and context-aware in large codebases. Instead of dumpin"
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=NVkRkioBXQc)

DOX GitHub:  
https://github.com/agent0ai/dox  
  
DOX is a self-documenting AGENTS.md framework that makes AI coding agents more efficient, reliable, and context-aware in large codebases. Instead of dumping the entire repository into the agent’s context window, DOX gives the agent a map: a tree of local AGENTS.md files coupled directly to your code structure.  
  
The idea is simple. Your codebase is already organized into folders like API, frontend, tools, plugins, helpers, and services. DOX attaches concise documentation to those meaningful folders, so the agent can start at the root, follow the documentation tree, read only the relevant path, and understand exactly where and how to make a change.  
  
In this video, I show how DOX works, why more context is not always better context, and how a single Markdown framework can stop coding agents from creating files in the wrong place, duplicating existing functionality, breaking conventions, and slowly bloating your codebase.  
  
I also show how to initialize DOX in an undocumented repository using Codex CLI: paste the DOX AGENTS.md into the project, tell the agent to index the repo, and let it build the documentation tree automatically.  
  
No install.  
No package.  
No server.  
No database.  
No vector store.  
  
Just Markdown files, coupled to your code, maintained by the agent itself.  
  
Web:  
https://agent-zero.ai  
https://space-agent.ai  
  
Skool:  
https://www.skool.com/agent-zero  
  
Discord:  
https://discord.gg/B8KZKNsPpj  
  
GitHub:  
https://github.com/agent0ai/dox  
https://github.com/agent0ai/agent-zero  
https://github.com/agent0ai/space-agent  
  
X:  
https://x.com/Agent0ai

## Transcript

**0:00** · Welcome. Today I'm about to show you how you can leverage a single small marground file to fix your AI coding agent's biggest issue ever. My name is Yan. I'm the developer of Agent Zero and Space Agent. And today I will show you how to properly use Docs. It is extremely simple. No installation, no requirements. And the best part is that it actually fixes the issue. So now what is the issue? obviously is the reliability of coding AI agents and we all know the symptoms. You give your AI agent the task.

**0:31** · It will do the task but in a wrong place breaking your conventions duplicating functionality instead of extending a function that could have just one line addit. It will create a brand new helper module etc.

**0:46** · Your codebase will bloat and this makes things even worse for the future. And you know how this ends right? never- ending cycles of debugging, fixing one thing breaks another, your agent is confused from all the code, etc. So now I will show you what docs actually is, why is it so simple and why it works so well, why did we develop it and how can you use it in your project. So first we need to identify what is the real problem here. The issue is not intelligence, it's context awareness.

**1:21** · Because your agent is already smart enough, your LLM is smart enough to do any programming work better than you can. But where it fails is maintaining large code bases because it doesn't see behind the corner. It does not know the context of your full codebase. And that's why it makes these simple mistakes because it simply cannot see the big picture. and throwing more tokens at it. That's not a solution. The question is not how do we give it more context.

**1:53** · The question is how do we give it exactly the right amount of context it needs. Not more, not less, minimum context required to make the minimal edit and that's it.

**2:07** · Now to understand why did I develop docs, we need to take a look at space agent because this is where it started.

**2:14** · Space Agent, if you don't know what it is, it's an AI agent that runs completely in the browser runtime. It can execute code. It can generate its own UIs on the fly. It can communicate to external services. You tell it to build you something, it will build it on the fly right away in the browser. And it has a ton of advanced features like uh user management, uh groups. It is extensible in many many ways.

**2:42** · It has a large code base, a lot of layers, a lot of concepts, a lot of cool features like the time travel and it was completely developed by AI. I didn't write a single line of code on this project. And it took me about 3 weeks to completely develop Polish and publish this. And so since the very beginning, I knew that I cannot be writing code here. It's not possible in 2026.

**3:09** · You need to have a team of agents that will do this for you, but you need them to do it reliably and to write good quality code, maintain uh maintain the right principles and uh best practices etc.

**3:25** · And so the very thing I did inside space agent was creating this agents.md file where back then it wasn't called docs framework. It was just the first prototype of a self-documenting framework built specifically for the space agent project.

**3:46** · But it was mostly what docs framework is now. It explained to this agent to read documentation before editing, update documentation after editing, maintain the documentation in a hierarchy corresponding to the codebase and how the documentation should look like. So like we say here, docs is a self-documenting agents.mmd framework.

**4:17** · The big difference here is that it's not a single agents.mmd file. It's not a documentation that's detached from the codebase somewhere. What we are used to a lot of projects have their documentations in a wiki somewhere or in separate folder. Here we tightly couple the documentation with the codebase. And I can show it to you here.

**4:46** · This is the code base of agent zero for example. It's a very large project, very large code base, very deep and it all starts with the top level agents.mmd file.

**5:01** · Here we have our original agent zero instructions and somewhere here starts the docs framework which is one of the beauties of it. You can simply take the markdown from the GitHub repo, copy paste it into your existing agents.mmd.

**5:17** · It does not mess up your existing instructions. It just adds the let's say responsibility to your agent for the documentation.

**5:29** · Now the agent knows that it needs to crawl the hierarchy of agents.mmd files because each agents.mmd is created in every subfolder throughout the codebase except for some temporary files and garbage etc.

**5:50** · And every agents.mmd file is responsible for a single domain, a single folder, but it contains a child docs index. And we are now in the top level agents.mmd.

**6:05** · And here we have our subfolders agents API configuration, docker, etc. Each of these have their own agents.md files inside that document that one specific domain.

**6:18** · And for example in the agents we will once again find child doc index at the end documenting individual agents inside of the system. And why this tree structure is so important is that this way the agent can always take the fastest most straightforward path to the place where it needs to make the changes.

**6:44** · So if I tell the agent uh create an API endpoint for me right in the top agents.mmd file that the agent can see at all times it can see that there is a documentation for API endpoints here is a short description http API handlers and websocket handler entry points the agent will open that file read about the

**7:12** · purpose ownership local contracts aka rules, work guidance, how to test and verify so the agent can quickly navigate to the relevant place, make the minimal edit, and most importantly after any edit, update the documentation files, which keeps the documentation in sync with the actual codebase. And I know this may seem like a simple concept. It actually is. And it may be hard to believe that this actually brings any real benefits to AI agents.

**7:43** · But the difference between the input and output, what I mean is the size of the addition to your codebase, no installation required, no manual work, and the output in terms of code quality and agent efficiency is so disproportional here that we had to release this as a standalone product.

**8:09** · I say product but of course it's open source just go and copy paste it and we can probably best see it on the space agent itself which was completely AI coded we can take a look at the top level agents MD and it will point us to the front- end application commands packaging server test we can take a look into the server documentation for example

**8:40** · And this will point us further into API endpoints, jobs, library, pages, router, runtime. You get the idea. Everything is thoroughly documented. The agent updates all the relevant documentation, not just the closest agents MD file to where the agent does the edits, but also the parents if that is relevant.

**9:07** · So if we change something about the concept, if I tell the agent that I want him to use different coding practices, different styling, formatting, whatever, it can update this in the parents files agents.mmd.

**9:26** · And this will be reflected anywhere down the tree because as the agent navigates the documentation hierarchy from top to bottom, it will keep in the context window all the information and instruction from the parents agent MD files and all the detailed instructions from the end of the tree.

**9:47** · So once we get once we get deep enough like into I don't know maybe jobs here we should have more specific instructions function names etc to the problem at hand in this folder but in the parents in the server for example we will have higher level instructions where to put stuff how to work how to organize code etc.

**10:17** · ETA and all of this compounds as the agent traverses the tree. So no information is lost. Even is even if something is in a different branch of the tree, it can still be linked in the docs index or in one of the sections above. If you have a shared functionality like helpers, they can be in a different part of the tree and the agent can still link them together using these markdown files.

**10:45** · So these markdown files are like a preview of the whole codebase. It's like a map for the agent and the agent only navigates the map until the point it needs to touch the actual code. And so we don't pollute the context window with any unrelevant information. It can see all of the documentation files on the path to the target.

**11:16** · It doesn't see any of the sibling folders unless they are manually linked because they are relevant.

**11:24** · Okay, enough talking. I guess I can show you how you can implement this into your own repository. It's it's very simple.

**11:34** · All you need to do is open the agents.mmd from the docs repository.

**11:39** · Simply copy the file and let's go to terminal.

**11:46** · All right, I am in my terminal. I have cloned our agent zero connector that is a repository that is not yet documented.

**11:54** · So I will now simply start codeex here and I will tell codeex add this at the end of agents MD here or create.

**12:12** · I don't know if there's already agents MD in this repo. I don't really care.

**12:17** · Codex will take this add it at the end of the agents MD and then I can tell it now initialize the docs index.

**12:33** · Okay, I'm put this to Q.

**12:37** · And so now agents.mmd is either created or edited with the docs framework appended at the end. And so now codeex will understand what docs means because agents.mmd is always included in the system prompt or in the context window.

**13:00** · And now that I have told it to initialize the doc index, it knows what to do. It will start reading through the codebase and creating this agents.mmd documentation points throughout the repository and linking these files together. It will probably take a few minutes because the LLM needs to read through all of the codebase or most of the codebase and manually write these documentation files.

**13:30** · But in a bit we should be able to see the first result.

**13:36** · Okay. So it took about 5 minutes to index the existing codebase. This is not a particularly large one. These are the agents MD files created in the subfolders for dev tools documentation for the source for different screen styles etc. So let's see how it went.

**13:59** · Okay. So this is the top level agents MD. There were some instructions and links previously. So docs will start somewhere here.

**14:11** · Here we have it.

**14:13** · And here we have the child docs index.

**14:17** · So we can take a look into let's say source screens.

**14:22** · And here we have the ownership parent package rules control app integration commands protocol screens should return typed results data classes or none and no children under screens.

**14:38** · We can enhance this.

**14:42** · I can tell I want to enhance the documentation of screens. I want all the Python files in the screens folder to have their own documentation. the same file name with markdown appended at the end. And they will document individual screens and they will be listed as child docs indices in their parent documentation file.

**15:11** · And just like that, if we have something in our project that is not separated enough, like in agent zero, we for example have a helpers folder which contains maybe 100 scripts by now. We can do it like this.

**15:28** · We don't need to separate it into subfolders. We can simply tell the agent we want to change the documentation structure for this particular folder. We want to document each of these files individually and it will simply put the rule into this agents.mmd file which will make it be applied only for this folder and this folder can have its individual files documented separately.

**15:55** · We can do this for any folder throughout the repo. We can tell the agent we want to do this for every single folder for the repo and in that case the agent would put it into the top level agents MD. It's up to us. The framework is really simple and customizable. You can simply tell the agent that you want to do something differently and it will apply it to the correct agent MD files.

**16:20** · And we can see the update here. So the agent MD in screens was updated somewhere here.

**16:29** · It tells that every Python module in this folder must have a sibling markdown document. And just like that, every file in this folder is now documented. And uh let's do some edit. Uh what do we have here?

**16:45** · We have installed plugins.

**16:50** · Okay, I'm going to tell the agent that I want to change something in the plugins view.

**16:56** · I want to change the plugins view to have a different background color than the others. Once the user opens that screen, I want the background to change from black or whatever we use now to red.

**17:14** · And obviously I I have no intention in in keeping this edit. I just want to demonstrate how will codeex proceed.

**17:27** · I will update the installed plug-in screen styling. I will reread the applicable doc chain. This is the important part that the agent will read the doc chain because it may have been changed. So it will start from the top read through all the documentation find the right documentation file for the plugins screen.

**17:49** · I am looking at the existing installed plug-in selectors. Now the likely change is in a screen scoped TCSS rule. I have no idea what it's talking about but now it has all the documentation. I don't need to worry about it.

**18:07** · All right. So, we have changed the installed plugins screen backdrop to red. The inner plugin stays dark.

**18:15** · Updated the markdown documentation and verify the syntax.

**18:24** · And of course, this is compatible with any AI agent that supports agents.mmd.

**18:28** · In agent zero, you can do this in project. For example, when you create a new project, you can put it directly to the project instructions or you can create it as an agent.mmd file inside that project. The agent will see it or you can simply tell your agent to clone agent0/docs repository into your current workspace.

**18:53** · It will do it for you.

**18:55** · So, this is the life-changing markdown file you've been looking for. You can thank me later. You can give us a star.

**19:00** · We only have 41 of these by now. It's really fresh. You can subscribe to our channel if you like what we do. And see you next time.