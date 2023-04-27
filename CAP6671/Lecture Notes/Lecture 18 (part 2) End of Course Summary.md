title:: End of Course Summary
date:: 2024-04-19
status:: Complete
[[Lecture 17|<<prev]] | [[Lecture 18 Final Exam Review|next>>]]

Course Summary: reference [[cap6671-conclusion.pdf]]

This lesson began with a [[Lecture 18 Final Exam Review]]


# Intelligence = Search
We want to represent the world, and we want to find a good answer.
A lot of what limits us is moving to large problems with lots of possibel answers

# Search Types
Optimal vs Satisficing

![[Pasted image 20230419183648.png]]


## Modeling Humans

- Motivation for social simulation research
- Background on SocialSim competition
- Operation of cross-platform simulations


## Human Behavior Prediction

- We can use AI to model and predict human behavior
- Why is this useful?


## Human Behavior Prediction

- We can use AI to model and predict human behavior.
- Why is this useful?
- Address HCI usability questions
- Debug social-computational systems
- MMOGs, social media platforms, crowdsourcing
- Guide public policy decisions


## Techniques for Human Modeling

- Machine learning:
- Time series prediction
- Collective classification
- Leverage network information
- Agent-based modeling:
- Complex adaptive systems
- Complexity arises from connections!
- Cognitive agent architectures
- Monolithic models that emulate human processing
- Fusion of two techniques


## Reading

- Muric et al, Massive Cross-Platform Simulations of Online Social Networks, AAMAS 2020 [[@Muric2020]]
- This paper describes research that was done under the DARPA SocialSim program which also funds my research.



PAST NOW FUTURE

### Future of Social Simulation?

How do we achieve the vision of versatile, large-scale,
high fidelity, social simulation?

- **_Bootstrap simulations with social media data_**
- **_Rigorously test and measure simulation accuracy_**


## SocialSim Challenge

n 7 teams competing:
̈ UIUC, USC, Rutgers, VTech, USF, and 2 different UCF teams
n Predict GitHub event time series 2 months into the future
after viewing 26 months


## Evaluation

Introduction Challenges Project 1 - Modeling Network Dynamics with Sampled Historical Data Proposed Work Completed Projects Publications
Data

Evaluation Protocol

```
Neda H. Bidoki Predicting Social Network Dynamics Jan 13, 2020 15 / 67
```

## Our Team’s Approach

n Creating a large set of agent-based models coded in
Netlogo and Repast HPC
n Each model attempts to capture a different social theory
̈ Diffusion of Information
̈ Complex Adaptive Systems
̈ Reputation Knowledge Economy
̈ **Data-driven User Archetypes**
n Model parameters are learned and combined using
evolutionary model discovery


## DASH Agent (USC)

```
Figure 2: Agents’ work￿ow
with the social media resources they produce or are associatedAgents in our simulation interact with each other by interacting
with. The nature of interactions can be various and multiple. Forexample, in Twitter we de￿ne agents as users and resources as
tweets. Users can interact with tweets by retweeting them, likingthem or replying to them.
and resourcesThe environment{A 1 n,A, then, consists of the agents 2 ,...,A<} 2 '. Agents and resources are de-{U^1 ,U^2 ,...,U=}^2
￿for agents and resources respectively.ned by their state. States include two sets of features-U 8 and-A 9
process is implemented as aAll models used agents’ decision process shown in Figure 2. ThisDASHagent and consists of modular
components that can have multiple implementations (marked 1-5).Experiments can also be con￿gured to have heterogeneous agents
using diThe major components of the agents’ decision process are the￿erent modules implementations (algorithms).
following:(1) Activation. Agents become active and ready to take an action
in one of two ways: internal self-activation by coming to thefront of the event queue as an agent or external activation via
a trigger that comes to the front of the queue. These methodscan be used simultaneously or separately. This dual queue
approach for incorporating external signal into simulationsdescribed in Section 3.4
```
```
(2) Identiand cognitively infeasible for the active agent to consider all￿cation of the visible horizon. It is both computationally
possible resources in making an action decision. The agent’svisible horizon⌘is de￿ned by a set of rules that limit the
resources the agent can possibly interact in a given timestep. The users of a social network are presented with a very
with, as illustrated in Figure 3a. For example, a Twitter usersmall subset of the resources they could in theory interact
can interact only with tweets that are displayed on theirdevice. Our attempt is to emulate this limited visibility of
with a specithe available resources by allowing agents to interact only￿c fraction of resources. The models for calcu-
lating the visibility horizonin Section 3.5 ⌘are described more in details
(3) Invoking the process of selecting a resource and action typeIf an agent makes a decision to take an action on an al-.
ready existing resource (e.g. edit or delete its tweet) then itneeds to select resources to interact with. This decision can
be translated into the following set of problems: given theagent-resource pair with the corresponding sets of features,
whether the action will be selected. These are classiproblems, where a combined set of featuresG=GU￿ 8 cationkGA 9
needs to be classideveloped for this problem are described in Section 3.2￿ed into positive or negative class. Models
(4) Starting a new information cascadecascade means creating an original resource rather than act-. Starting a information
ing on an already existing resource. Our simulation modelsuse training data to sample the roots of information cas-
cades. Information units (keywords, hashtags, URLs) are alsosampled from the training data.
(5) Reacting to an existing information cascadesimilar to (3). This decision can be translated into the follow-. This process is
ing question: given the agent-resource pair with the corre-sponding sets of features, whether the action will be selected.
Twitter and Reddit models developed for this problem aredescribed in Section 3.2
(6) Adding/Updating information unitsdate meta information of the resource (e.g. keywords, hash-. Agents can add and up-
tags, URLs). Information spread is measured per each infor-mation unit and discussed in section 4.
in the sense that they can take actions on diEach of the agents in this framework are cross-platform agents￿erent platforms. The
social platform, where the action happens, is speciagents’ activation is scheduled on the queue. Parameterization and￿ed when the
training required for each component (1-5) in Figure 2 is done foreach social platform.
whenever it is activated as illustrated in Figure 3b. To optimizeDuring the simulation, this process is repeated for each agent
the use of the resources, we sometimes pre-compute, parallelize orbundle some of the steps when possible.
3.2 Twitter and Reddit ML modelsML models predict the probability of interaction between an agent
and a resource. In the “real world” the users are presented with aset of objects they can interact with. For instance, a user on Twitter
can see a few dozen tweets in a given moment. For each of the
```
```
Research Paper AAMAS 2020, May 9–13, Auckland, New Zealand
```
```
897
```

## My Work: Cluster-based Archetypes

n Hypothesis: users will have different usage styles (“archetypes”)
which will manifest as differences in average distributions of user
monthly events.
n Use machine learning to uncover these patterns
̈ Clustering user activity histograms
̈ Clustering repo activity histograms
̈ Sequence analysis
n LSTM
n Sequence pattern mining
n Encode in an agent-based model
n Result: better performing model with a reduction in parameters that
EMD needs to optimize


## Datasets

n Calculated **averagemonthly** activity
of users per event type

n Calculated **total** activity of users

n Users with at least one activity ~ **9
million**
n Users with more than **10** total activity
~ **4 million**

n Known bots ~ **1000**

```
Dropped
```
```
Features
```
```
Clustered these users
```
```
Normalized k-means clustering
```

```
Partition
```
```
Average Monthly
Activity # Users
1 (0,10] 1.9M
2 (10, 100] 1.8M
3 (100, 1K] 48K
4 (1K, 10K] 863
5 (10K, inf) 86
```
## Rate-based Partitions


**Cluster Centroids:** 10 < Average Monthly Activity < 100

```
Average monthly activity
```
```
Example Usage Patterns
```
```
All users in this partition generate more Push events than other types of events but
the relative proportions of the events differ.
```

```
Cluster Centroids: 100 < Average Monthly Activity < 1K
```
Average monthly activity

```
Example Usage Patterns
```
```
The largest group of users generates a lot of Push events; the smallest group has
a more evenly balanced activity profile divided between Create, IssueComment, and
Push
```

```
Clustering Repos
Partition (100, 1K]
```
There also interesting differences between repos with some receiving many Push
and others with many WatchEvents.


```
Clusters
Count
```
```
Stability Scores
0 - 10 10 - 100 100 - 1000 100010000 -
3 0.931 0.996 0.920 0.685
4 0.949 0.988 0.928 0.671
5 0.912 0.919 0.841 0.557
6 0.825 0.989 0.867 0.604
7 0.795 0.934 0.751 0.594
8 0.791 0.974 0.796 0.577
9 0.769 0.973 0.617 0.571
● The best scores
● The second best scores
```
## Cluster Stability Analysis

● To find the number of clusters (k) that
makes the most stable clusters
● In a stable clustering, we expect to
observe similar clusters from month to
month
● To measure month to month stability,
we computed similarity between
clusterings of consecutive months
● We computed Adjusted Rand Index
(ARI) to measure similarity between
clusterings
○ ARI is 1.0 when clusters are
identical and close to 0.0 for
random labeling.
● The stability score is the average
similarity score of all consecutive
months


## Netlogo Agent Behavior

n User agents select a behavior to perform based on
the event frequency defined by their archetype
n User agents maintain a list of familiar repositories
n If watching or forking:
̈ Select a fixed number of repositories at random
̈ From this subset, choose the repositories with the
most number of watches and forks to watch/fork
̈ Add repo to list of familiar repositories
n If contributing:
̈ Select a repository from the familiar repositories
list


34 4/19/23

# Experiments on ABM Archetypes

```
Rate
Partitions Cluster based on Select k
cluster
stability
```
```
Translate
centroids into
relative event
frequencies and
population
distribution
Improves
Ginicoefficient of
event distribution
over simple mean
model
```

## Course Summary

- We surveyed:
- Software agents
- Robots
- Human-agent-robot interaction
- Discussed semi-applied case studies of systems:
- What has been implemented?
- What is still lacking?
- But what do these systems have in common?


## Intelligence=Search

- Search is an integral part of AI!
- Some would argue that AI consists of only 2
fundamental concepts:
- Knowledge:
- Representation and manipulation of factual and
probabilistic knowledge
- Search:
- Explore knowledge alternatives to find the best
quality answer
- To be truly intelligent you must be able to find a
good answer within a reasonable length of time!


## Search Types

- Optimal
- Best possible solution
- Might not be achievable in a reasonable time
- Satisficing
- Come up with the best quality decision within given
resource constraints
- Solution quality can be significantly worse than an
optimal solution
- Stop search and approximate the result


## Search Approaches

- Search plus heuristics (A* and others)
- Dynamic programming (solve and cache subproblems)
- Reinforcement learning (value iteration)
- Bayesian MAP (maximum a posteriori)
- Parallel search
- Graphplan
- Stochastic search techniques
- UCT, RRTs and SSA are examples of this
- Genetic algorithms
- Optimization techniques (maximize a function)
- Mixed-integer linear programming
- Gradient-based
- Deep learning


## 3 Different Approaches

- Classical AI
- Represent the problem
- Search for solution
- Machine learning
- Use data or world experience to guide search
- Knowledge represntation=metric
- Search=optimization on metric
- Robotics
- Satisficing search---reasonable solution quickly!
- Robust control—make stability guarantees


## Future Research

- Solve problems with bigger search spaces
- Multi-agent problems often fall into this category!
- Handle search spaces with lots of local minima
- Reduce the amount of specialized data and domain
knowledge required; increase the amount of general
common-sense knowledge all systems have access to
- Handle dynamic, rapidly changing problem spaces
- Robot problems often fall into this category!
- Using deep learning to handle other types of AI
problems


## Create a General Intelligence

- Many AI systems that can be trained to solve a specific
problem in a narrow range of scenarios (a sandbox)
- Goal: create an intelligent system that can robustly
handle a wide range of problems
- Be able to acquire data online and adapt to changing
circumstances


## Current State of AI/HRI

```
https://youtu.be/rDyTsGtk5BY
```
A humorous look at the present state of AI, robotics, and
HRI:


## 2023 AI Predictions

- LLMs running out of high quality language data
- Greater availability of autonomous robotaxi rides
- More research on humanoid robots
- Foundation models for robotics
- AI changing the nature of search
- LLM operation jobs availability
- More research on AlphaFold
- More semiconductor suppliers enter the market

```
(Forbes)
```

## Final Thoughts

- Thank you for taking the course
- I really enjoy hearing your presentations and
seeing your final projects; they give me research
ideas for the future.
- If you want publishing suggestions about where
you could submit your final project to, please
contact me after the semester.


