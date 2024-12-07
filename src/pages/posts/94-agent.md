---
layout: ../../layouts/MdPostDescLayout.astro
title: 'Agent Research'
LastUpdatedDate: 2025-01-20
CreatedDate: 2024-11-20
description: 'n/a'
author: 'Jeff'
tags: []


---
***

## 11/24/2024
* [DeepGram links to papers](https://deepgram.com/learn/top-arxiv-papers-about-ai-agents) - May 2024
* [ChatBase article](https://www.chatbase.co/blog/ai-agent-frameworks): "Top 7 AI Agent Frameworks for 2024" - Nov 4, 2024
	1. Langchain
	1. LangFlow
	1. CrewAI
	1. Microsoft Semantic Kernel
	1. Microsoft AutoGen
	1. Mazaal AI
	1. CrewAI
* Pretty basic HR article by [Josh Bersin](https://joshbersin.com/2024/09/agentic-ai-ai-agents-the-new-workforce-were-not-quite-ready-for/) - Sept 2024

## Suggestions from ChatGPT on 11/27
1. Generative Agents: Interactive Simulacra of Human Behavior (August 2023) - [arXiv](https://arxiv.org/abs/2304.03442)
1. A Survey on Large Language Model based Autonomous Agents (April 2024) - [arXiv link](https://arxiv.org/abs/2308.11432)
1. AGILE: A Novel Framework of LLM Agents (November 2024) - [arXiv](https://arxiv.org/abs/2405.14751v1)


***

## 11/26/2024
### IBM 1: What Are AI Agents?
* Speaker: Maya Murad
* [URL](https://www.youtube.com/watch?v=F8NKVhkZZWI)
* Evolution from monolithic models to compound AI systems


***

### The Rise and Potential of Large Language Model Based Agents: A Survey
* Authors: Xi, Chen, Guo, He, Ding, Hong et al., Fudan NLP Group
* v3 - 19 September 2023
* [arXiv link](https://arxiv.org/abs/2309.07864)
* Overview and history of Agents in AI and through Western Philosophy
* Referenced in [DeepGram May 2024 article](https://deepgram.com/learn/top-arxiv-papers-about-ai-agents)

***

## Section 2: Background
* Breakdown into: sensing/perception, brain (LLMs for now), action/muscles
## 2.1 Origin of AI Agent
### 2.1.1 Agent in Philosophy
### 2.1.2 Philosophy and Intentional Stance: 
* Debate between researchers: Is assuming Intention useful or not useful for AI/Robotics research?
* 'we can define AI by saying that it is a subfield of computer science that aims to design and build computer-based agents that exhibit aspects of intelligent behavior. So we can treat "agent" as a central concept in AI.' 

### 2.1.3 Introduction of agents into AI
* 'Instead, researchers employ other attributes to help describe an agent, such as properties of autonomy, reactivity, pro-activeness and social ability. 
	* There are also researchers who held that intelligence is "in the eye of the beholder"; it is not an innate, isolated property. 
	* In essence, an AI agent is not equivalent to a philosophical agent; rather, it is a concretization of the philosophical concept of an agent in the context of AI. 
	* In this paper, we treat AI agents as artificial entities that are capable of perceiving their surroundings using sensors, making decisions, and then taking actions in response using actuators.

***

## 2.2 Technological Trends in Agent Research

### 2.2.1 Symbolic Agents
### 2.2.2 Reactive Agents
### 2.2.3 Reinforcement Learning-based Agents
### 2.2.4 Agents with Tranfer Learning and Meta-Learning
### 2.2.5 LLM-based Agents

## Progress
* completed quick skim of both the sensory (3.2 Perception) and motor (3.3 Action) sections

***

### LLM Multi-Agent Systems: Challenges and Open Problems
* Authors: Han, Zhang, Yao, Jin, Xu, and He 
* February 2024
* v3 - 19 September 2023
* [arXiv link](https://arxiv.org/abs/2402.03578)
* Referenced in [DeepGram May 2024 article](https://deepgram.com/learn/top-arxiv-papers-about-ai-agents)

#### Abstract
* This paper explores existing works of multi-agent systems and identify challenges that remain inadequately addressed. By leveraging the diverse capabilities and roles of individual agents within a multi-agent system, these systems can tackle complex tasks through collaboration. We discuss optimizing task allocation, fostering robust reasoning through iterative debates, managing complex and layered context information, and enhancing memory management to support the intricate interactions within multi-agent systems. We also explore the potential application of multi-agent systems in blockchain systems to shed light on their future development and application in real-world distributed systems.

***

## 12/05/2024
### YC LightCone Discussion
* "Vertical AI Agents Could Be 10x Bigger Than SaaS"
* [Page](https://www.ycombinator.com/library/Lt-vertical-ai-agents-could-be-10x-bigger-than-saas)
* [YouTube link](https://www.youtube.com/watch?v=ASABxNenD_U)
* Date posted: 22 November 2024 

#### TimeStamps
* **1:01** Jared Friedmanis Excited about Vertical AI Agents
* **1:51** Most Startup Founders (esp young ones) don't realize how big b2b SaaS is b/c it's not in their personal consumer experience
* **2:12** 40% of VC over last 20 years has gone into SaaS, produced over 300 SaaS unicorns
* **2:58** Invention of AJAX (Asynch JavaScript and XML / XMLHttpRequest) in 2004. Arguably, Google Maps, Gmail, etc led to this ability to run rich web apps without having to reload entire page for each button click
	* Software moved from being something primarily based on CDs, to something accessed purely over internet / local web browser
	* Paul Graham's ViaWeb connected Unix prompt to changes in web with minimal intermediaries; arguably invented SaaS in 1995.
* **4:16** Jared sees this as a similar invention paradigm with LLMs that allows us to do something fundamentally different.
* **4:35** In 2005, what should we do with XmlHttpRequest? Where is the value going to accrue, where are the startup opportunities in 2005?
	* Bucket 1: Obviously Good Ideas, eg. docs, photos, email, calendar, chat. Zero startups won here. Google and Microsoft and other incumbents won
	* Bucket 2: Mass consumer ideas that nobody predicted. Uber, DoorDash, InstaCart, Coinbase, AirBnB. Came out of left field. incumbents didn't even try b/c it was a weird/big jump from XMLHttpReq to renting a room
	* Bucket 3: 300 B2B SaaS unicorns.
* By # of logos, way more companies were created in Bucket 3. There is no "Microsoft of SaaS". For structural reasons, there are just different companies.
* **6:35** Harj Taggar: Talk by Marc Benioff that initially, people assumed that web apps suck. Early on, people didn't believe one could build sophisticated enterprise applications in the cloud via SaaS. Perception issue. 
	* "Serious software" had to be purchased in cardboard boxes / CD-ROMs
* **7:09** one had to be a visionary like Paul Graham in 1995 to see how the browser would keep getting better. Similar moment to LLMs now  
	* Current critiques of LLMs in an enterprise app perspective: they hallucinate, they're not perfect
* **7:30** By analogy to SaaS revolution, incumbents will win Bucket 1 LLMs products that are obvious like generalized voice assistants. Perhaps Perplexity can challenge Google in Search, but we'll see? 
* **8:30** Perhaps the reason why incumbents didn't take over Bucket 2 is b/c of classic innovator's dilemma b/c they did not want to endanger their profitable incumbent franchises. Google never launched an Uber clone or AirBnB clone.
	* Travis Kalanick talk: For the first several years of Uber's lifetime, he was convinced he was going to go to prison. No comfortable Google Exec would risk that.
* **9:15** Diana Hu: Why didn't incumbents go into Bucket 3? (JH: I'd argue that Amazon through AWS and Google as a follower in GCP did. And MS with Azure)
	* Jared: I think it's hard to manage that large a scope. Each b2b company needs to have deep domain expertise in their vertical. 
		* Example: Gusto. Hard to have an organization hyper-focused on all the various local, state, federal payroll regulations. 
		* Easier for incumbents to focus only a few huge categories
* **10:15** Harj: Why wasn't b2b SaaS just taken over by Oracle, SAP, Netsuite? 
	* Partially it's because the old distribution/ecosystem model was for the large System Integrators to offer to build custom extensions, etc. for each customer. Remember, before cloud era, there was less intermingling.
	* Knock against Salesforce at first was that it would be too underpowered for the highly custom / specific demand. But they proved that it was good enough and improved quickly enough that it worked. 
	* (JH: Helped that the horrible UI and expense/post-sales integration of incumbents were Oracle, etc as the competition. No real consumer-grade UI as competitors)
* **11:10** Diana: Oracle, SAP, all their UI was really bad. Jack of all Trade master of none b/c they have such huge portfolio across all their apps. Could build a literally 10x better UI
* **11:40** Garry: Joke about how there are only 3 prices in software per month: $5/seat, $500/seat, $5000/seat
	* These correspond to consumer, smb, and enterprise
	* Classic difference between tech buyer vs end-user
* **12:35** Garry: Is this going to change in the era of LLMs?
	* Typically, as revenue scales in YC portfolio, it's typical to see companies that reach $100m - $200m in revenue have 500-2000 employees already.
	* I'm curious; now giving advice to companies 1-2 months post YC batch to see if you'd hire this many people
	* different than the advice he might have given 1-2 years ago.
	* In the past, would make a huge priority to hire *the best of the best* sales people, product people, marketing, customer success, HR, engineering, etc. And they would build big teams.But maybe not now? Just hire great software programmers who really understand LLMs to build what you need; to buildthe solutions around your bottlenecks to growth. In the past, it was hire sales/marketing/recuriting, etc.
* **14:15** Maybe this means CEO investment decisions post PMF will be different. Dramatically changing cost structure
	* We're right at the beginning of this new era
* **14:33** Diana: We've talked about this before. See the first unicorn that can run with only 10 employees (JH: what about Instagram from 2012?)
	* Garry: and the employees all they do is run evals and prompts
* **14:45** Harj: When I was running Triple Byte, for user acquisition, after raise a Series B, you are supposed to hire a Marketing Exec and spin up a machine for sales and marketing
	* Example of an MIT / YC alum who was building a smart frying pan
