---
title: "MemoryGraphRAG (Outperforms Every RAG)"
source: "https://www.youtube.com/watch?v=RfAbsdq_b-A"
author:
  - "[[Discover AI]]"
published: 2026-06-03
created: 2026-06-27
description: "Building a Self-Adjudicating Memory Network for RAG.MemGraphRAG: Giving LLMs a Collaborative, Three-Layer Long-Term Memory.All rights w/ authors:MemGraphRAG: Memory-based Multi-Agent System for Gr"
tags:
  - "clippings"
---
![](https://www.youtube.com/watch?v=RfAbsdq_b-A)

Building a Self-Adjudicating Memory Network for RAG.  
MemGraphRAG: Giving LLMs a Collaborative, Three-Layer Long-Term Memory.  
  
All rights w/ authors:  
MemGraphRAG: Memory-based Multi-Agent System for Graph  
Retrieval-Augmented Generation  
Chuanjie Wu∗  
wuchuanjie@stu.xmu.edu.cn  
Xiamen University1, 2  
Xiamen, China  
Zhishang Xiang∗  
xiangzhishang@stu.xmu.edu.cn  
Xiamen University2, 3  
Xiamen, China  
Yunbo Tang  
tangyunbo@stu.xmu.edu.cn  
Xiamen University1  
Xiamen, China  
Zerui Chen  
chenzerui1@stu.xmu.edu.cn  
Xiamen University1  
Xiamen, China  
Qinggang Zhang†  
qinggangzhang@jlu.edu.cn  
Jilin University  
Changchun, China  
Jinsong Su†  
jssu@xmu.edu.cn  
Xiamen University1, 2, 3  
Xiamen, China  
  
#airesearch  
#aiexplained  
#retrievalaugmentedgeneration

## Transcript

**0:00** · Hello communities. So great that you are back. Yes, today we talk of 40 development on rag. You know, we had graph rag and now we have a memory graph rag. And yeah, absolutely we built a new memory graph layer with an ontological layer with three different memory layers and it will improve the performance of our system.

**0:22** · And here we have it. This is here from Xi'an Jiaotong University and Jilin University. MemGraph rag memory-based multi-agent system for the graph retrieval augmented generation and you sing back to the good old times and you said, "Where is my vanilla rag?" But forget about it. We have now this new and novel framework that introduces now a memory-based multi-agent system to ensure high-quality graph construction.

**0:50** · And if you're new to this, you say, "But why? We had graph rag. It was perfect."

**0:54** · And no, graph rag had three main problems. And they now cope with each of the problem, they found a solution to this problem. So, let's start. Graph rag had a problem of a thematic irrelevance.

**1:06** · Let's call it the noise. Because the LLM reads your chunks out of the context, it extracts sometimes irrelevant sites and side notes. So, for example, in a medical text about cancer, it might extract you the triplet the patient prefers tea over coffee. This is nice, but maybe this is not here really relevant for the analysis.

**1:28** · Second, logical inconsistency or called the lies. Different chunks of text often contradict each other, especially have multi-sources, no? One says, "Hey, Isaac Newton was born in 1643." And the other says, "No, Newton was born in 1645."

**1:44** · And a naive graph rag simply merges now both facts creating a split timeline that confuses now here the downstream retrieval. And third problem was the cracks, the structural fragmentation.

**1:57** · Without a global taxonomy, the growth becomes fragmented. And we'll show you how we can cope with this. So, the same entity might be written here as Newton in one place and Isaac Newton in another place, resulting here in disconnected islands. Think about this as a three-dimensional graph structure that prevent now a multi-hop retrieval from traversing here the complete database.

**2:20** · We are locked in here maybe to some graph islands.

**2:24** · We want to solve this.

**2:27** · So, beautiful. And in general, you can say if you have here on the x-axis the recall in percentage and on the y-axis the relevance in percentage, vanilla RAG did great, but look where it is positioned, huh?

**2:40** · So, graph RAG achieves a higher recall percentage, absolutely. So, this means it finds more potential clues, but it has a catastrophically low relevance because more or less it drowns the LLM in noisy, contradictory context. Yes, of course, we have hypo RAG and some GFM RAG and everything. And if you are new to my channel, I have a complete a playlist on YouTube here about RAG 3.0 agency. So, there's nothing about the vanilla RAG. This is already RAG 3.0.

**3:12** · So, if you want to see here S-PaRAG or whatever you like, we have a lot, a lot of RAG systems.

**3:20** · But what is the latest memory graph RAG?

**3:22** · This is here a three-layer global memory that more or less we add here to the graph RAG system.

**3:30** · So, here you have it compared to the graph RAG here on the bottom, you see MemGraph RAG. So, we have the chunking, we inject it, but we have now three different layers of memory. We build now a hierarchical graph, and we will have a good old friend from Google in the retrieval page ranking mechanisms here to extract the facts from all the text passages.

**3:53** · So, let's start.

**3:54** · At first, we have to have here the memory-based indexing of the graph construct itself.

**4:00** · So, what we have we have unstructured document where we store thousands and millions of documents, beautiful.

**4:06** · And I will show you later on we have three agents. And the first agent here is the extraction agent, guess what?

**4:12** · And takes care that it is positioned now in three different memory layers.

**4:18** · We have global memory here. And the first one is the ontology layer.

**4:22** · You know, we have here a schema, no?

**4:25** · Where we have our graphs. Either this person rule country or person native location or company create product, whatever. Now, for your particular documents, this builds now a frequency filter for this stable schema for the top K schemas. Like, I don't know, country capital city or person job profession.

**4:45** · So, the ontology layer stores schemas with the extraction frequency of your training documents.

**4:52** · And then we have the factual layer.

**4:55** · And this is where, guess what, maintains here the concrete facts, beautiful. As I showed you, we have now from two different documents here a Newton birth year birth year 1643 and Newton birth year 1645.

**5:08** · So, what's this happening? From this fact layer, we have now the second agent, our conflict detector agent.

**5:15** · And understands, okay, there is a conflict and you know, we have to keep the agents simple. Don't give them two jobs, only one job because, yeah, LLM is not that capable. And then we hands it over to the next third agent, and the third agent is now our conflict handler. Guess what?

**5:34** · This conflict handler looks now at the triplet here at the conflicting triplet, looks at the original document and says, "Okay, it can only be one true, no?" So, given here what is the documentation here, it now decides one of them is the correct one and beautiful. And this is here in the passage layer because here in the passage layer it preserves the original text passages for the evidence grounding.

**6:00** · This is here absolutely important.

**6:02** · So you see this is here where we say if we have a debugging neurological debugging what we do, we go here to the passage layer and we see exactly here what was the incoming information and why did here the conflict detect on the conflict handler agent choose here a particular document.

**6:20** · And then if we have all of this memory full of data, we build a graph. So we start here in at the bottom here with a passage graph.

**6:29** · Now here we have the entity, the documents, everything is there.

**6:32** · Beautiful. Then we build our fact graph here from the fact memory layer. We have here the entities for example coach, the relation is job and the entity is I don't know Simpson or John or whatever. And the weight is one.

**6:48** · And then we have the ontology graph in a hierarchical structure here where we have the schema. So the schema is type is person, relation is job, the second type is profession and the weight is now five in your unstructured document training data.

**7:04** · So as you see we have now three interconnected graph views.

**7:09** · So at first we have the semantic ontology graph derived here from M ontology which encodes here the schema level type relations and the structural constraint of those two, eh?

**7:21** · Then we have here second the fact graph constructed here from the memory fact factual which represents here the no, the instantiated entity relation triple for multi-hop reasoning and then we have the source evidence graph that grounds here everything in the supported text passages.

**7:38** · Now as I already showed you we have three agent, they call it a multi-agent group and for a particular reason I'm going to explain at the end of this video, they go with a GPT-4 Omni Mini. I don't know if it's available officially from OpenAI, maybe Omni, I think, is now here.

**7:55** · Yeah, whatever.

**7:57** · And they say, "Okay, we need three agent." And I showed you already what the agent do. So, check mark, beautiful.

**8:04** · Just to make sure, the memory itself is not a passive data store.

**8:08** · It is here, if you want, or it enforces here a two-way relationship. So, what we have is a schema instance alignment. So, every fact in the fact layer must be governed by a valid rule in the ontology layer.

**8:22** · And we have a fact and evidence grounding. This means every fact in the fact layer is mathematically tied up here to the exact text passage in the passage layer where it was found.

**8:35** · And if a fact is questioned, the system can instantly point to this exact source text, beautiful.

**8:43** · Now, I told you about some disconnected some island in the graphs, now. And to to prevent now this fragmentation here, the authors of this paper today of memory graph wreck bridges now here with two particular bridging mechanism here.

**8:58** · They bridge the disconnected parts of the graph using here two methods. At first, we have a type-based bridging, simple, linking here distinct entities if they share a high-level category classification in the ontology layer.

**9:13** · Beautiful. And a similarity-based bridging, this is drawn on some invisible or rather weak connection between entities whose Now, hold on to your socks, we are back here to the semantic vector embedding, are highly similar, ensuring that structural traversal can navigate here across the document boundaries. So, we still have here a good old cosine similarity.

**9:37** · This is all done offline. Now we come here to the real case real world case online retrieval. So now we come we have an incoming query for me for example, yeah?

**9:47** · So, my question is here now. Great. So, what is happening? As you see, we have more or less three steps, one, two, and three.

**9:55** · So, at first we have memory guided retrieval and reasoning now in three states. They just first multi-layer memory retrieval, yeah? Which retrieves now candidate schemas, facts, and passages from the memory.

**10:11** · Because my question is here, let's say, about physics and I have a lot of physical knowledge here in my memory and in the three different layers.

**10:20** · Beautiful. Then, second is here the structure-aware node initialization.

**10:26** · What does it mean? It simply maps the retrieved evidence to some initial node weights based on the semantic relevance and on the structural signals that we have in the network. This is classical.

**10:39** · And finally, and this is now the beauty, if you want, we have a personalized PageRank. Good old Google. Google started out with PageRank algorithm when I started here to study how does Google do its job here. PageRank 100 of years in the past. Never mind, we still use this algorithm now here in the online retrieval in the third step. So, graph propagation, which run here personalized PageRank over the heterogeneous graph to rank now globally important nodes and passages here for the LLM generation.

**11:12** · And then, all the information is coming here to an agent and then here this agent now provides the answer here to my question.

**11:19** · Great.

**11:21** · So, if you just want to have it a little bit more in an abstract notation, when a user submits a query, we have at first a parallel extraction. Now, the system retrieves the relevant schemas, the relevant facts, and the passages from the three global memory layers simultaneously.

**11:36** · So, if I have a question about physics, it knows exactly, okay, somewhere in the memory there's the physics department and just grab all the physics.

**11:43** · Then we have the smart reset weights.

**11:46** · Now, this calculates here the starting weights for the graph nodes. So, what it does, it first it has to suppress the generic hub categories, no? Like these general terms like person or particle or light or photon, no?

**11:59** · Because they don't want to drown out here in the specific notes during this research. And then they have to prioritize passages with a high information density.

**12:10** · So, documents containing rare, highly specific experimental data from my latest experiments, so I know exactly here where my data source is.

**12:20** · And then, yes, as \[clears throat\] you know, the PageRank mechanism. It simply runs a propagation walk across the entire graph to let the semantic energy flow outward from the query relevant seed nodes, and this means we really identify the most critical paths and passages in this complex graph, which are then passed on to the generator LLM to provide an answer to the user.

**12:43** · Great. So, one would say, "Hey, this sounds simple. This is straightforward.

**12:47** · There's nothing that we say we have to calculate something mathematically that is crazy." No, benchmarks.

**12:53** · So, let's have a look. We have here different benchmark Hotpot, WikiMulti, Hot Music, and on and on, and then overall. So, let's have a look.

**13:04** · The authors structured this here in a three blocks. The first is a direct zero-shot LLM inference. So, how good is a Llama 3 8 billion here on a Hotpot Q&amp;A?

**13:16** · We got a result. Or a GPT-4 Omni Mini, this is it.

**13:21** · And now compare this to the added improvement here because here at the end here this delta is now here. If you would do this with a GPT-4 Omni mini with this new methodology on this particular benchmark, we would jump here from 38.10 to plus 28.26 in addition. So, this would be a significant jump in the performance. If we have just a rag system, a vanilla rag system, you go with the top five, you see we go from 38.10 to 58.5.

**13:55** · But, if you would do it here, yes. See exactly. And then in this is beautiful.

**14:00** · Here you have all the rags, the famous rag system, yeah?

**14:04** · The Microsoft graph rag, the laser graph rag, the light rag, the hyper rag, the hyper rag two, the E-squared graph rag, the GFM rag, the logic rag, the linear rag, and my goodness, I don't know how many other rag systems we have already.

**14:17** · And then in the last line, our new memory graph rag system. And you see it almost outperforms here every other graph-based rag retrieval augmented generation methodology. Beautiful. And you see here also the added performance jump here in the green boxes. So, if we go for a hyper rag, so let's stay here, we have plus 8.27.

**14:46** · Is this percentage or percentage points?

**14:48** · I don't know. Please check in the literature, but you see it is quite a a nice and impressive jump.

**14:56** · What else?

**14:58** · I told you there's hardly any new mathematics. So, here you have not a pseudo code for coding here the algorithm. And at first, here's the memory based indexing, the graph construction.

**15:10** · So, whatever we went through, here you have it again in a simple pseudo code structure. But, I'll give you also the GitHub repo, so you don't have to code anything. And of course, the memory guided and the online retrieval.

**15:23** · And yeah, there's a little bit of filtering going on, but otherwise it's exactly like we went through, but you can have this now here. Yeah, we fall back solution to standard rag. Of course, you can implement this, but this is exactly what we went through together.

**15:39** · They are really beautifully detailed.

**15:41** · You see here in the annex then also the prompt used here for let's say the conflict resolution agent. So, you have a really the prompt that they used for the experiments. If you want to run them, if you want to modify here their prompt further and you want to see how much you can improve now on their memory graph rag methodology. They provide here all the prompts and everything. And yes, of course, here's the GitHub repo.

**16:08** · As you see three-layer memory structure.

**16:11** · And yeah, this is it. This is the address. And then if you have a look at the memory Python file, they exactly build that three-layer memory structure with inter-layer connection, schema layer, fact layer, passage layer, and yep, everything is available for you if you want to test it out.

**16:27** · Now, what I did not mention yesterday, it outperforms, but you know, there's another benefit that it did not just outperform, but we used so much effort and computer time for the indexation of this complex graph that then when we have the incoming query, this system is now fast. And remember, Google PageRank, this is a real fast system. So, here we have the data.

**16:53** · Compare this now.

**16:55** · And here you have Raptor, HyperRAG, and whatever. And at the end here, the last column is the retrieval time, the classical retrieval time. And you see, you are with this new methodology faster than any other method that we had up until now, but of course, this is only because we invested quite a lot of time in the preparation, in the indexing of the graph, in building up this complex graph with the complex memory layers, no? So, do not forget operational if you have it.

**17:26** · Absolutely ultra-fast, but you have to invest quite a lot of here for your particular training, for your particular domain knowledge indexing. Let's say you go with mathematics or theoretical physics or chemistry, biology or medicine or finance, whatever you have.

**17:43** · Yeah, and then I told you again, I thought about this. Why GPT-4 Omni Mini?

**17:49** · And I thought, why is there not the latest Claude 4.8 or I don't know whatever we have, no?

**17:56** · And it is simple.

**17:58** · And I noticed just a half sentence, but I think the intention was that the authors wanted to show us you don't need the best and the most expensive language model on this planet, because even with an old non-top-notch LLM, these new methods work. And all the data you have seen that I showed you here, all the agents were running here at GPT-4 Omni Mini LLM.

**18:26** · So, you cannot say that this has a high technological complexity or this is here that you have to have to run it in a cloud, no.

**18:34** · So, if you see it now from this perspective, I have to smile and I say, "Hey, this is great that the authors choose such an old non-all-powerful model, no? That we can run maybe locally.

**18:47** · It doesn't have to be a GPT system.

**18:50** · And the methodology is working and it is stable and it's providing you really benefits compared to the other graph rack system. And this is here something I just wanted to stress out because I get some response, "Hey, why is there not the latest? Why is this just a 4.7 and not a 4.8 LLM?" Well, sometimes it's good to know this new stuff also runs here on the good old fashion LLM's that are non-complicated at all and they are non-cloud based.

**19:19** · I hope you had a little bit of fun, some new insights, maybe you want to try out this new methodology for your particular domain, for your particular complexity level of your query, of your task. Would be great to have some feedback if you have here some improvement that you really notice that those memory layers provide here an additional benefit for your professional work. Would be great to see you in my next video.