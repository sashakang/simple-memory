---
title: "Harness Engineering for AI Agents (Why Every AI Business Will Need It)"
source: "https://www.youtube.com/watch?v=uAhWHu3WdUw&t=1477s"
author:
  - "[[Cyril Imhof]]"
published: 2026-03-12
created: 2026-06-27
description: "🤝 Our daily learnings engineering AI since 2023, let's connect:🇨🇭 Cyril ImhofLinkedIn: https://www.linkedin.com/in/cyril-imhof/🤖 Get $20 in v0 credits to build ANY AI SaaShttps://v0.link/cyr"
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=uAhWHu3WdUw)

🤝 Our daily learnings engineering AI since 2023, let's connect:  
  
🇨🇭 Cyril Imhof  
LinkedIn: https://www.linkedin.com/in/cyril-imhof/  
  
🤖 Get $20 in v0 credits to build ANY AI SaaS  
https://v0.link/cyril-imhof  
  
⏱️ Timestamps:  
00:00 What we're covering  
01:23 Agentic Skills and Context  
02:20 Components of Skills  
03:00 Toolkits and Skills  
06:35 Harness Engineering and MCP  
14:15 Outcome-Based Pricing  
  
📝 Referenced in the show:  
https://openai.com/index/harness-engineering/

## Transcript

### What we're covering

**0:00** · Hello everybody and welcome back to episode 45 of this AI podcast. In today's episode again with me is Schwo and we're discussing today of everything around aic engineering. We talked about harness engineering especially how you actually generate these important AI agent harnesses. And at the end of the episode today we're also deep diving in how do you actually look into the pricing of these harnessed agents? How do they actually create value? But how do you make sure you price this adequately for example with outputbased pricing?

**0:31** · But with me today again from Lisbon, how is life doing uh in the south of Europe? Uh it's good. We have good weather. We have uh time and so far things are looking pretty good. Uh however, things are not looking that good over at cloud servers. Uh but we'll get in get into it uh in a few minutes.

**0:54** · Bad weather, bad weather on cloer services. Everybody's vibe coding.

**0:58** · Everybody's using clothes code. Again, my background today. But in the episode today, let me quickly make the segue into the first topic, which is harnessed engineering. A few months ago, we actually talked about already in regard to aantic skills. So basically equipping agents with context knowledge. For example, back then it was mostly just markdown files. in a sense, how do you actually generate a great LBO model for a financial agent or an Excel model in general?

### Agentic Skills and Context

**1:26** · This was probably a little bit steamrolled and augmented in popularity when open clothes came out and pretty much the agent and actually not only took specific skills from the markdown context, but also actually also added new memory files into markdown. And this became all this like let's say a little bit loose context of this completely new Atchantic world that now we're living in.

**1:49** · But the more components that we're actually adding to the agent, the more complicated it is for the agent to really orchestrate all these markdown files and tools and and so on and so forth. So that is exactly why there is this reasoning on we need a structured approach basically giving an agent a structured harness to actually yield the best possible output.

**2:09** · So just in another way that I usually think about it is an ideal enchantic harness is really optimized for the context for the agent that it needs to perform in this multi-step uh procedures a human actually asked the agent to do. So that's a little bit the way I think about it but from your perspective show how do you look into the components of the skills and then translating that into great harness engineering.

### Components of Skills

**2:33** · We started by building tools and initially we had like two three four tools and that was good enough. uh you had a tool to search through files, one tool to go online uh and maybe if you were adding let's say a word document, you had some kind of tool to read the word document and some other tool to uh edit it, make changes, text, whatever.

**2:52** · However, as time went on, we demand more and more from the agents. And so now we're upwards of 50 60 sometimes and something tools for the agent and we're now moved into grouping these tools as toolkits as skills. skills is, I think, a better name for it because it's not just a group of tools, but also some instructions on how to use them. Uh, if you're messing up with Word, you know, how to edit the word, what the style of the document that you're writing in should be. Uh, all that kind of information is not just a tool, but also usually some markdown file.

### Toolkits and Skills

**3:24** · Markdown is a bit of a constant uh with this kind of models. and you group them together those kind of tools and those instructions and you build up the skills because we quickly realized for the things want to do especially I'd say coding agents are one of the most famous types of agents they're very welldeveloped and pretty popular by then

**3:47** · across the board in all developers you can easily have upwards ofund and something tools available to your agent that becomes extremely hard for the agent when he's trying to implement a new button implement a new feature on your site and suddenly they has to read over 100 tool descriptions and decide what tool should be best used for this kind of job. Uh maybe a sequence of tools.

**4:08** · So we have to start grouping them into toolkits or skills and then selectively let's say we have a toolkit just for browsing the web and that's just instructions on how the searches should be some tools on different APIs different places to search the web on some places to search documentation on the platform that you're using and you group them uh so that the agent does not have the hund and something tools right way available to it but it can search and activate skills accordingly.

**4:35** · So if you ask something, hey what is the best way to or what is the best framework I can use for this? It knows that it has to search somewhere. It has a skill it can activate. It sees a skill about searching the web. It activates that skill and only then it can see the four or five different tools and some instructions on how to search the web.

**4:55** · This is how you do content engineering so that you don't spam the agent with all the possible tools and all the possible buttons it can press. Um and you get the best results. Maybe just to to roll up this very briefly. So we came from prompt engineering which is basically this very simplistic form of optimizing the input of a of a large language model um to then context engineering which is then optimizing basically the input of the context window. You don't want to give the model all the trash that you can possibly find lying around.

**5:25** · Even if I see that occasionally actually happening, let's just give everything to the model and the model should figure it out itself.

**5:32** · But in context engineering, um, it's a little bit more like optimizing like a human kind of workflow as well. If you have a meeting in 30 minutes and you would want something from a CFO like we quickly talked before the podcast or you want to have something from an engineer, you don't give it everything you possibly know on finance or everything you possibly know on engineering. You curate this context aka this 30 minute slot you have with a human.

**5:56** · And very similarly in the aentic or ancient world, you would curate the context to only give it mostly relevant concepts like for example a tool description, a particular skill it needs to activate and some other components for example how to actually um maybe do an IP API call and which one you might actually need. There is also this let's say larger array that you should also not overcurate the context. there should still be some degrees of freedom that the model can somewhat have some clarity of choice as well.

**6:25** · And this is this pretty much this balance that is then um emphasized in this context engineering let's say workflow that you would want to constrain it but not too much. So you kind of have to find this middle balance. Ultimately what you're from a builder perspective want to optimize is of course both the intelligence or the output the value creation of your software of your chantic system for example but at the same time you want to minimize the cost you need to to use and to deploy to yield that intelligence.

### Harness Engineering and MCP

**6:51** · So in other words if you give too much context that is meaningless you pay basically tokens for no good reason. If you don't give enough you don't yield sufficient intelligence. So that's a little bit this like trade-off that you constantly have to do and you can give partially of this decision back to the model but not everything. So that's that's the world of context engineering. In harness engineering, it basically takes the whole world one step further.

**7:19** · And we're trying to basically enable the value creation by putting this harness around an agent around a large language model or maybe a multitude of them for it to then be optimally set up for example to be a coding agent, to be a financial analyst agent, to be a due diligence agent, a legal agent or an agent in a call center.

**7:38** · So you would basically curate the world around an agent in that particular case that might as you mentioned perfectly show include tools, include skills, include API, um include any other component that you might actually need. Is there any particular way what you would be saying for example taking financial analyst agents as an example where a harness has to have to yield a good agent?

**8:03** · Uh you can have a rundown of the usual tasks you do if you're doing the task yourself. Uh but the idea is never show the agent more than I'd say 30 tools uh at one single time. So usually for financial analysis you need something to uh search the documentation, search some files you have about the doc the company you're evaluating about the market you're uh investing or or playing around in. Uh and also some tools to go online.

**8:33** · But you also need some tools and some skill to maybe write down the report. uh if you're writing a report then some skill to actually write into a word document or it's a text document some instructions on how the document should be uh parsed how the formatting should be because it is for the best and it is somewhat simple to instruct JSON to write the way you want it to otherwise you're going to have multiple iterations and it's going to cost you extra more money and so you build up these skills and you try to group them mentally and a skill is

**9:04** · getting information is research basically and how to do research and the tools that you need to do that research either in the documents or online.

**9:12** · Another tool is another tool set is writing and creating the report. Maybe it's creating a financial model in Excel and you need some tools to actually play around with Excel. Read the Excel and how some instructions on how the Excel should be formatted, the formulas that you should be using. So, group them into these toolkits or skills and then have a brief description of the overall skill.

**9:35** · So one skill could be here's how you should interact with Axel. Uh and the another skill should be here's how you do research. And whatever task that you give the agent, you can then activate those skills. And only if it activates those skills, then it can see the tools related to it, the extractions related to it. That means you can have a 100 plus tools, but you don't have to show them all the time.

**9:58** · The agent can actually go and search for the tools that you have available to then use them. uh you might have to wait a couple more seconds because instead of having the tools right away available they has to search for them. It's a roundway trip but it is uh usually for the best because for 100 something tools that you have available maybe five or six are actually going to be used. I mean one particular component here that I'm still struggling somewhat to kind of make sense of especially if we talk about harness engineering just overall is is this topic on MCP.

**10:29** · I mean currently we we believe MCP is the best practice to kind of have this conneure connector between the agent and let's say the outside world but I'm just like making sense more and more that it's fairly constrained what can flow through MCP's fairly structured and standardized protocol whereas if you have some more scattered markdown files fully laying around I think there is just yielding a little bit more context to perform this particular task.

**10:54** · So in other words, MCP is great, but it probably has the promise to be like a highway for data transfer, but so far to me it feels a little bit like a train. So you can only do a particular request and you have to kind of of course wait and it comes back with a particular response. And this is very limited in terms of context um depth. Whereas if you have markdown or if you have an array of markdown or this this entire harness um that is actually yielding a lot more context depth than just MCP.

**11:23** · So I'm kind of curious to see if MCP is really the protocol we're adapting into the future. Of course, if you build on financial analyst agents or finance in general or maybe some legal procedures like audit or like maybe insurance as well, you would want to have traceability. You would want to have some sort of governance structure so the agent doesn't go rogue in your organization.

**11:44** · you need to probably um customize the agent in the sense or the MCP itself.

**11:49** · Okay, the agent cannot access at will particular resources. It it needs to be some sort of logged. It's usually constraints on financial companies that that we see happening. But just overall, I think MCP might not be the best add-on in this harness engineering that we kind of would want it to be. That's a little bit my five cents and maybe Yeah. What what's your take on on this show as well? Uh I think we use MCP only to get to the level of tools.

**12:14** · So let's imagine you're building some kind of scheduling agent that you want to uh reach out to partners, reach out to colleagues and set up the meetings accordingly. The MCP, for example, Google MCP or Gmail MCP would give you the tools to read your email inbox, write some emails, uh least possible uh addresses to write the emails to. Those would be tools that you can get for MCP. However, MCP by itself is insufficient to build out this agent, right?

**12:42** · You want some instructions on how you want the meetings to be scheduled, uh how they should be scheduled, the names of the meetings, u the timing that you'd like them to have them. So, a full uh scheduling agent skill, if you want to create that for your own personal agent, should be maybe a couple tools from NCP, maybe a couple tools uh internal to your own computer, your own service, and then that uh instruction uh skill, usually a marathon file or some other file where you write down that information.

**13:13** · A lot of those, there are some market places for those skills, people write down those instructions.

**13:18** · Not a lot of them are super safe. We've been seeing I think with the rise of openclaw people created like this kind of marketplace where people would write and share skills is and and be a really good idea on for example the scheduling agent there were scheduling agent skills where it could show the agent how to do them how to be polite how it should invite people to do things the best way to actually schedule a calendar to be efficient for for people.

**13:41** · However, a lot of the skills that were on our marketplace were um malicious and so people would hide instructions there saying, "Hey, send information to uh this address or like log the the the keywords uh and basically exfiltrate a lot of valuable information from you into some other remote remote server. So, there are publicly available skills.

**14:08** · uh be very careful because you might be instructing your agent without you realizing uh to do some very nefarious things. I mean I think it's a good good perspective maybe to add on this very very briefly just in other words explained harnesses is a little bit like the component that was so far missing to yield this translation of just a technical capable model like we've seen with very advanced PhD level models

### Outcome-Based Pricing

**14:31** · didn't actually yield business value realization because so far this kind of translation was still missing while it was an incredibly intelligent large language model for example an OPUS 45 or a previous Oppus model it never really yielded material business impact because it kind of was lacking this harness to actually effectuate the business value realization.

**14:53** · So in other words, we kind of take this super intelligent model but as builders we're kind of wrapping this harness around it and now suddenly it actually yields and ongoingly will yield more and more and more business value because now it is embedded in tools. It is embedded in into skills that actually

**15:10** · are materially mattering for a particular job and are not just generally trained like you would train a transformer and then you do a reinforcement learning a little bit alignment there fine but it's not aligned into the business context because just if you rewind back some years ago we always kind of had this idea of we fine-tune the models for the company context but we never actually did that for two reasons. it was too expensive for many firms. And secondly, once you did the fine-tuning, the next best model came around and you did all this fine-tuning for no good reason.

**15:41** · That's why we mostly built and we leveraged generalpurpose large language models that are highly not accustomed to the context of the business world. But now with harness engineering or having an AI agent with a harness, it now starts to actually have this business value realization in place. as hopefully finally that we see some sort of business impact happening with all these AI agents in the months to come. And one last topic just for today's episode is pricing because now we actually have a mechanism.

**16:12** · We have a mean to take this harness. It yields business value. And we see that ongoingly now with agents being augmenting humans for example in the financial world. We've seen it for a multitude of months now in the coding world but also into customer care, customer support until transcriptions and similar services. But one question remains. How do you price in this new world where you have a harness, you have a super intelligent model and there is this this whole theory of outcomebased pricing?

**16:41** · But before we go into this rabbit hole, sure, what's kind of your maybe best idea of how would you kind of make sense of you have a harness now, but what are maybe some of the cost factors and then maybe I can add the best sense of the pricing factors? You have a harness. What are some optimization vectors that you need to do to make it as cheap as possible?

**16:59** · As a builder, as soon as you build up the harness and you have a sufficient harness that has all the tools and skills that make the agent or allow the agent to do what you want it to do, you get the idea of the minimum possible model that you can run on it that actually can use your harness. Uh for any modern hardness of skills, I I'd say coding agent, but you can think of like a personal agent. So, it has uh the ability to read emails, uh read your calendar, check something in your like smart home.

**17:29** · A personal assistant kind of agent has maybe like 10 14 tools that he needs to use. If I plug in a model like GPT4, like the standard GP4 or GP4 Turbo, which is maybe 2 years old by now, that model might 99% certainty that would fail at most assets you give it.

**17:50** · also because older models, especially simpler or dumber models, uh are not as optimized to use tools as the more recent ones. And even the more recent ones, uh you have what three or four frontier models that people usually use. But if you're really concerned about privacy and safety and you want to host your own models, is a wide variety of open- source models you can run on them.

**18:14** · But they also come in a wide variety of sizes and cost. So you cannot just choose the best possible open source model. It might not fit your hardware and you might need 50 or $100,000 hardware to run those models. And so you have to get an idea of how intelligent, how advanced must your LLM, your AI model be to use your harness. From then on, then you can have a baseline pricing because what we've been seeing is that the prices are not getting lower with newer and newer models.

**18:43** · We had it in the first couple years of genai with GBD 3.3 3.5 41 Omni like each and every model was getting better and also cheaper. Uh and now that's no longer the case. We're getting incremental increases. Models are still getting better but they're being priced accordingly.

**19:01** · I think it also relates to VC funding uh running out for these startups and for the inference and so people actually need to charge you for those tokens and if you're building uh agents around these models you also need to charge uh your clients your subscriptions whatever uh these tokens and as soon as you have that baseline you can have an idea of how it how much it costs for you to run that kind of model. uh and it is not as

**19:29** · cheap as maybe it would be in 2 years ago but you're also getting a much better model and you can build much better and higher quality agents that do real business value.

**19:40** · Okay.

**19:40** · So maybe if I translate it in other words so you would work backwards from the required harness to yield the business value. So you kind of know what is required in terms of harness and then you try to fit it in with some sort of of a large language model that fits the harness or the other way around if you think about it as well. I mean you can technically build around an LLM the harness but then the new model comes around and you're not model agnostic anymore and you have to rebuild the entire harness.

**20:04** · So that's kind of what we've seen also like there is kind of this decision um are you entirely building around an oo or a set or you have like some sort of model agnostic harness that you can simply replace fairly fastly the large language model when it comes around very similar like it was before you don't want to build your workflow and around a particular

**20:24** · model you also probably don't want to build the harness around the particular model but rather have it more modular have it more flexible once a new model comes around most of the time this is a closed model or maybe a Gemini model and you can swap swip uh swap around the models and reh harness it and then yield it into production in a fairly substantially short period of time. You might need still need to do some testing but that's kind of it's an interesting facet as well. Not only do you have the regular testing procedure, you probably also have to retest your harness that you build around the particular model, which is a very easy segue then.

**20:55** · Okay, fine, we have the harness, we have the large language model. How do we price this for the customer? And since it is now more or less derable from business value realization, you can think about it as an outcomebased pricing because the conversation in in a particular sales call or sales conversation might be with this particular large language model.

**21:15** · In other words, this particular agent equipped with a harness which is business contextaware, you can then materially improve a particular process and from this process improvement, you would then yield a particular percentage um as a let's say as a return or in other words as a price for your service.

**21:34** · This is not entirely new. So if we think about which type of other businesses do some sort of having a percentage of a value creation pricing, it's usually transactions in financial services. You have a transaction. Of course, there's transaction prices that are fixed prices. So whatever the transaction is, it's just $15 for example. But most of the time in transaction prices, it's like a percentage.

**21:56** · In other words, if you have this in the aentic world, you're implementing an AI agent that yields material business benefit ideally with a harness and it's it's fully functioning within an org. You can then probably derive in a particular workflow that it it helps save a particular amount of money and from that saving, you would then actually price it back to you as an owner of of this AI software.

**22:20** · As an example, if you have a financial analyst agent just making things up, it would speed up the Excel model generation by an order of magnitude or maybe by 20x that saves a particular amount of hourly rates and from this particular amount of hourly rate saved.

**22:35** · You would then take a particular percentage and you would price it accordingly. You might still yield some sort of or actually have the necessity to have a base pricing for your infrastructure or some sort of a base price. But then ultimately if you do outcomebased pricing with a harness, you're more aligning your achantic system to the client's best possible outcome. Because ultimately what most of the salespeople, the good sales people in the world are selling, they're not selling software. They're selling outcomes. They're selling outcomes based on metrics.

**23:05** · And these metrics are ultimately on a for example deal by deal size in terms of a financial analyst or a finan or a or a call center agent ultimately. So that's a little bit this outcome based pricing. It's kind of difficult because you need to know okay how much infra cost do we actually probably more or less need to yield that particular outcome but once we do this successfully we could then materially benefit from the upside of the of the company because not only is it more aligned with the business.

**23:33** · It's just also a little bit of an easier story than you have to pay by usage like we've seen with AI. But what's your what's your take on this show? It's a new it's a new um phenomenon. I have that perspective from both being a builder but also a consumer of this AI services for the coding agent that I subscribe to. It has gotten a bit more expensive than it was in the past.

**23:55** · But that cost value um approach to it still very much applies because I've been I did the maths and the 100 and so bucks that I pay for it. If I were to not have it, uh it would take me sometimes double the amount of time just writing the code. So planning by itself, uh I can still do it my own. I might be a bit slower cuz I don't have to actually manually research every single topic I have to interact with.

**24:24** · But I could sort of do the planning by myself, but writing the code, it takes time. I mean, I I I type fast, but uh the model just can iterate through files and just go to the right file and change the lines probably much quicker than I than I can, and it won't get distracted uh by notifications or emails or whatever. And so having this kind of model saves me, I'd say, at least 4 hours every day that I would spend on doing things that are just that much faster. And four hours of every day of every single workday, uh it adds up to much more than 100 bucks.

**24:56** · And I don't want to uh say it super loud so I don't get I don't give ideas to Microsoft to increase their prices. Uh but I want to just have that kind of in mind when they increase their prices that it's still very much reasonable for me to to to pay that amount. Uh cuz the value that I get from it is uh very reasonable um in contrast to what I pay.

**25:20** · And I think as a builder, that's also like the the goal that I try to do is build a harness and have a model that's capable enough that the value that it outputs is still much bigger than whatever it costs. And it should be much bigger than whatever it costs uh the client and also much bigger than whatever it costs to run it. And uh those running costs, you can call it infra costs. It's inference plus infrastructure plus the servers plus whatever your AWS bill uh ends up being.

**25:51** · Um, and because it is, uh, as we've been seeing, increasingly higher, you have to just have a better and better agent to justify those costs.

**26:00** · I mean, it's a bit of a of a emerging topic this this pricing of agents, but I think ultimately you can decide just to make a high level summary between a usage based pricing where you basically say, okay, you have some sort of tokens or credits or you have some sort of amount of workflows you can run per month. just from my own experience in sales perspective. Hardly anybody has this concept of tokens sometimes unless you're an AI builder. So it's a difficult sell if it just if you basically say okay I give you 10,000 tokens whatever that means.

**26:29** · So you kind of have to introduce this new lingo in also on top of your product. So that's the use that's the usage world. The second component is you have a fixed price tier like you would have in a software as a service something we we used to know for many many years now.

**26:44** · cost you flat $30,000 per month and you can just use it how much you actually want. Might sound appealing, but if you have inference cost from OPOS or from some other advanced models, that's north of four figures per day per user, it's probably not the best idea. And then there's this third component that's kind of what we teased today. Maybe we can deep dive in a future episode. Once again, outcomebased pricing. something we spent a lot of thinking on.

**27:06** · But it's mostly this particular pricing that would align the best possible partnership with your client and also it would actually incentivize us builders to make our harness in terms of the engineering of it and the all language model that's be that's behind it powering this all as cheap as possible because this would yield a higher margin. Um ultimately to then benefit again from the value that the agent is creating.

**27:32** · Ultimately, we kind of have this conundrum that agents might augment slash replace a specific substrate of employees. So, we maybe also kind of need to start thinking about the value these agents are creating and we having a derivative of that in terms of our pricing as AI builders. But that's it more or less for for the episode.

**27:52** · Shah, anything more to add on harness engineering, skills, AI, context engineering, value based pricing? to give you a somewhat recent example of how much it can differ like a quick request, a quick hey to an agent from an actual long running agent that processes things is using your harness using tools going online for to search for things can cost you. Uh, one of the like most famous coding agents is C code.

**28:18** · I think by far it's like top three for the last year or so. um very easily in in the top three agents uh in the AI world and that's always been token based uh because people using cloud code know at least half of a concept of token so you don't have to introduce that lingo like you're saying that you'd have to do for a business world Microsoft had the GitHub copilot and does pretty much the

**28:43** · same as cloud code but their approach to pricing it was slightly different they price it by request so it doesn't matter if you say hey or if you ask for a super complex thing like build me a button um plan all the things around it and the API endpoints and everything and new database it would cost you the same to the user. It would be the same. It would cost you like one request and you'd get let's say a,000 requests per month or 5,000 requests per month. And they I think the last week or so they just quit that approach entirely.

**29:10** · Not because people were saying hey a lot but because people realized that they could just ask really complicated stuff and they always get built the same. So, might as well give get really complicated tasks right away and maybe bunch up a bunch of tasks that were um independent or that you're going to do in a row. Uh because the models are not good good enough to do them uh sequentially. You can just say, "Hey, do me this and this and this and then find uh by the end of it write me a report of everything you've done and push everything to to git or publish this website."

**29:40** · And so instead of wasting seven or eight requests, they'll do it all in one go. Microsoft caught up to that. Uh, I think they're not having the greatest of times affording that bill for the inference and so they cut that down and now you're paying for actual usage. They don't fully display how many tokens you're using. I think they're still keeping them to themselves. Ripple have realized that for longunning requests. You can see your usage bar and the bar keeps going up throughout the requests. It doesn't go up just one single time.

**30:09** · So you can see like one of the biggest companies in the world with one of the biggest agents in the world.

**30:15** · uh they're all going token by token, but it is remarkably harder to market it to business or people not in the AI world because what the hell is token for people who are not in an AI world?

**30:28** · Exactly.

**30:28** · I mean, I think it's a good good point to wrap up the episode. I think ultimately if you're a hyperscaler or a large lab, it's probably more selling towards engineers currently. At least that's what we've seen. But if we more and more customized harnesses, you as a builders in the audience are I think it's more and more and more moving and shifting into this outcome based pricing where you can basically go in steer the sales conversation in the sense that your achantic system might yield saving X or augmenting of revenue

**30:56** · Y and you have taken kind of a share then you have an incentive again to make your input that it needs to actually execute that as cheap as possible as effective and efficient as possible and at the same time maximize and use that leverage that you're creating for the client because ultimately this seems to be the most win-win situation. You seem to have the biggest margin. They seem to be having the biggest impact based on your chantic system on your AI agent with harnesses basically.

**31:21** · Whereas if you basically just say this is a flat fee, I think that's mostly that in AI and or usage base because what if you kind of approach the end of the month and you have 7 10 or 15 employees that still want to use the system but they kind of used their usage. I think there's a tendency that they would rather use a competitor for a few days that actually pay more usage or augments their usage budget. So that actually drives away probably great retention of of your software as opposed to actually yielding a material benefit financially.

**31:52** · But that's it for episode 45. It was a deep dive on agentic engineering. It was a deep dive on harness engineering, context engineering, AI agent harnesses and their benefit and their pivot also to outcomebased pricing in this new world of achantic artificial intelligence. It was a pleasure to have you on episode 45. We're approaching the 50s. And for everybody in the audience, new episodes out every single week.

**32:21** · We're active mostly on YouTube, but also sometimes on Tik Tok and LinkedIn. So, feel free to connect, drop a comment, and see you in episode 46.