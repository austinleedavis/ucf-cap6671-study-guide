Discussed in detail during Lecture 02  [Sukthankar CAP 6671 on 1/18/2023](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=5fa6aa84-0fd1-4c46-a8c2-af8100e2493a) at 46:00
Will be on the [[Lecture 18 Final Exam Review#Multiagent Systems]]

# Ongoing research areas per [[@Sycara1998]]:
**Discussion based on reading of [[@Sycara1998]]**

- Task allocation
	- Contract net protocol, auction-based frameworks
- Resource/communication limitations
	- Distributed constraint optimization
- Resolving sub-goal interactions in multi-agent planning
	- Decentralized MDP, team planning
- Obtaining resources (getting what you want)
	- Auctions, negotiation, coalitions
- Modeling other agents
	- Plan recognition (**Gita's group focused here**)
	- game theory
- **Adaptation and learning**
	- Multi-agent RL:  
		- Historically ran into a lot of problems because all the agents are learning at the same time. So, when one agent changes their policy, the rest of the agents would be behind.
		- Researchers developed centralized training, decentralized execution
			- During training, agents update a central repository for the policy
			- During execution, no longer have global state knowledge

# Human-Agent Collectives
**Discussion based on reading of [[@Jennings2014]]**
Discussed symbiotic interleaving of humans and computers:

>Jennings 2014:  constellations of people, resources, and information must come together, operate in a coordinated fashion, and then disband

