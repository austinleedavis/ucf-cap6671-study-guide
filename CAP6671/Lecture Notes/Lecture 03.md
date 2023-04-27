title:: Planning
date:: 2023-01-23
status:: Complete
[[Lecture 02|<<prev]] | [[Lecture 04|next>>]]

# Overview on multiagent systems
- Purpose of this paper: Introduce research problems that we are going to discuss in this course
- Ground Everyone in the same terminology
- Outline components of a multi-agent system case study of multi-agent systems
- How to build a multi-agent system

## Multiagent systems come from several places:
- Control theory
- Economics, organization theory, and sociology (How things organize)
- Psychology
- Software Engineering


## Agent Characteristics:
- Situatedness: they receive sensory inputs from environment
- Autonomy: Goal-directed and has control over its internal state
- Interactivity/Sociability
- Adaptivity

## Belief-Desire-Intention (BDI) Agent (Bratman, 1987)
- Belief: Current state of the world
- Desire: preferences over future world states
- Goals: consistent subset of desires that an agent might pursue
- Intention: selection of goals the agent has **committed** stance toward
- Plans: mechanism for achieving intentions

# Agent Architectures:
- **Deliberative** (e.g., STRIPS (Fikes)):AI Planner focused on coming up with a sequence of actions to attain a goal
- **Reactive** (e.g., subsumtion (Brooks)): Stimulus/response paradigm w/o internal representation of state so that "intelligence" occurs as an emergent property of the way the system is connected
- **Hybrid** (e.g., 3T (Bonasso), [[RETSINA]]): Agents contain both deliberative and reactive components
- **Cognitive** architectures (SOAR, ACT-R): Derived from cognitive psychology, based on human models of memory, thought, information processing

Anatomy of an agent: Differentiate research groups emphasize (or exclude) various components below:
- Sense-cognition-action loop
- Communication protocol/language
- Representation of world state
- Deliberative component/planner
- Reactive behaviors (more important for robots)

# RETSINA Architecture:
- from Sikara's group) 
- Used a knowledge query machine language (KQML) to communicate
- Rather than all agents being homogenous, agents fell into one or more categories. 
- The middle agent (Matchmaker or Broker) would service requests for service between requester agents and providers.
	- Matchmakers act like a yellow pages
	- Brokers on the other hand receive service requests and delegate the requests to the providers; maintaining privacy of providers
- Included visualization tool on the system

Characteristics of a Multi-Agent System (MAS): original vision is to mimic human-based systems
- Incomplete information
- No global control
- data is decentralized
- Computation is asynchronous

MAS Coordination: There are many ways in which coordination can work. Sometimes agents have different motivations, especially in an open system that allows agents to join/leave at will.
- Teamwork: agents share a common set of goals
- Coalitions (e.g., price negotiation/fixing): Agents seek to maximize individual utility (c.f. coalition stability issue)
- Coordination (e.g., traffic): Agents pursue their individual goals and utilities; coordination is only done to avoid harm
- Negotiation: Agents maximize individual utility but are willing to compromise because 
- Game Theoretic Interactions: Agents take others' options into consideration
- Adversarial Interactions/Zero Sum Games:  Max-my/min-your utility


Applications of Planning
- Space Exploration
- Games
- Manufacturing
- Robotics

Planning vs Scheduling
- Scheduling: Deciding when and how to perform a given set of actions; typically NP-Compl ete
- Planning: Deciding what actions to use, can be much worse than NP-complete: worst case is undecidable

Planning assumptions
- Finite system
- Fully Observable
- Deterministic
- Static

Plan Definition Language (PDDL)

# Classical Planning Assumptions
These are covered in detail on page 48-49 of [[nau-planning.pdf]]
- #A0 Finite system ($\Sigma$)  
	- finitely many states, actions, and events
- #A1 : Fully observable $\Sigma$
	- the controller always knows what state the system ($\Sigma$) is in
- #A2: Deterministic $\Sigma$
	- Each action or event has only one possible outcome
- #A3: Static $\Sigma$
	- No exogenous events: no changes except those performed by the controller
- #A4: Attainment goals
	- a set of goal states $S_g$
- #A5: Sequential plans
	- a plan is a linearly ordered sequence of actions $(a_1,a_2,\ldots,a_n)$
- #A6: Implicit time
	- No time durations
	- Linear sequence of instantaneous states
- #A7: Offline planning
	- Planner doesn't know the execution status