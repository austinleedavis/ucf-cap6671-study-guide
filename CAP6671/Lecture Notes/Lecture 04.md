title:: Planning Systems; AI in Games
date:: 2023-01-25
status:: Complete
[[Lecture 03|<<prev]] | [[Lecture 05|next>>]]

In planning, we assume we have a set of states, actions and dynamics

"Always have a question about graphplan on the exam" - Gita, Slide 15/47

# Iterative deepening search
![[Pasted image 20230309181251.png]]
Works well on **pathfinding problems**, but ... 
- state space explodes and 
- doesn't detect parall
- There's a lot of annoying actions you can take, that are useless to take.

# Graphplan #exam
States are represented by circles
Each action creates true and false propositions
NO-OP implies all things stay the same

**Authors found that while you can track all kinds of interactions, pairwise interactions typically are sufficient to produce a plan.**

![[Lec04-slide15-Graphplan.png]]
During **graph expansion**: from current state, you take all possible actions, and you'll find yourself in a new state at the next timestep.
Repeat until a plan exists in the graph.


![[Lec04-Slide16.png]]


![[Lec04-Slide17-Ex.png]]
There are four types of interferences that need to be resolved:
![[Pasted image 20230309180616.png]]
Then you just need to go back apply these to our graph
![[Pasted image 20230309180559.png]]
There was no legal path... Notice all states are carried forward by the NO-OP. 
- Once we have a state, it will persist forever. 
- **Stopping condition:** Once we have all the states we desire, we can stop and begin extracting the plan. 
- If extraction fails, apply another action level. (it's possible for this to )
![[Pasted image 20230309180815.png]]


Comparison with PSP:
CPU time for Graphplan is constant vs UCPOP

# AI in games

## Applicable in games
- Reinforcement learning
- Navigation
- Decision trees

## Problems
How do we crea te long-lasting bots that act autonomously over days in games?
Answer: #HTN Planning

## HTN Planning
Rather than compoising plan by actions, the planner write recipes that are composed.

**Intuition:** Since we already know how to do things, so we can just assemble a few recipies together to accomplish our goal.

HTN is Opposite of *Control rules*:
- control rules write rules to prune every action that *doesn't* fit the recipe
- HTN: descripbes actions and subtasks that *do* fit the recipe

**Recipes** typically include parameters that must be determined at runtime

### Example:
![[Pasted image 20230309181848.png]]

![[Pasted image 20230309181923.png]]

#FSM Finite State Machine can be written as an HTN planner


How many nodes are visition #metric
Computation time #metric 
in-game performance compared to others #metric 


#classical-planning performs poorly in: 
- Dynamic worlds
- Multiple Agents
- Imperfect/uncertain information

MDPs Relax #A2 (Deterministic $\sum$ )
- Actions have more than one possible outcome
- Seek policy or contingency plan
- With probabilities
	- Discrete Markov Decision Processes #MDP
- Without probabilities
	- Nodeterministic transition systems
