---
title: Multiagent systems
authors: Katia P Sycara
year: 1998
note: week01
pdffile:: [[sycara-mas.pdf]]
---

# Abstract
Agent-based systems technology has generated lots of excitement in recent years because of its promise as a new paradigm for conceptualizing, designing, and implementing software systems. This promise is particularly attractive for creating software that operates in environments that are distributed and open, such as the internet. Currently, the great majority of agent-based systems consist of a single agent. However, as the technology matures and addresses increasingly complex applications, the need for systems that consist of multiple agents that communicate in a peer-to-peer fashion is becoming apparent. Central to the design and effective operation of such multiagent systems (MASs) are a core set of issues and research questions that have been studied over the years by the distributed AI community. In this article, I present some of the critical notions in MASs and the research work that has addressed them. I organize these notions around the concept of **problem-solving coherence, which I believe is one of the most critical overall characteristics that an MAS should exhibit**.

# Summary
Focuses on key topics and interrelationships between topics. Emphasizes **coherence** as a key objective. 

## The characteristics of MASs are that 
1. each agent has **incomplete information or capabilities** for solving the problem and, thus, has a  limited viewpoint;
2. there is no system global control
3. data are decentralized
4. computation is asynchronous

## Key topics covered:
- **Individual Agent Reasoning**
- **Organizations**, a framework for agent interactions through the definition of roles, behavior expectations, and authority relations. Examples include:
	- Hierarchy: authority for decision making and control is concentrated in a single problem solver (or specialized group) at each level in the hierarchy.
	- Community of experts:  each problem solver is a specialist in some particular area
	- Market: Control is distributed to the agents that compete for tasks or resources through bidding and contractual mechanisms
	- Scientific community: This is a model of how a pluralistic community could operate
- **Task Allocation**: the problem of assigning responsibility and problem-solving resources to an agent
- **Multiagent Planning**: planning in an MAS environment also considers the constraints that the other agents’ activities impose
- **Recognizing and Resolving Conflicts**: The main approach for resolving disparities in an MAS is negotiation, but the paper mentions others
- Modeling Other Agents
- Managing Communication
- Managing Resources
- Adaptation and Learning

At this time, there are two major technical impediments to the widespread adoption of multiagent technology:
1. the lack of a systematic methodology enabling designers to clearly specify and structure their applications as MASs and 
2. the lack of widely available industrial-strength MAS toolkits
