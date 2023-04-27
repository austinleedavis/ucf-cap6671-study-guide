title:: MDPs and Monte Carlo Search
date:: 2023-01-30
status:: 
[[Lecture 04|<<prev]] | [[Lecture 06|next>>]]

# Discrete Markov Decision Process #MDP
**Old assumption:** In classical planning, key assumption is that actions have a single outcome, as specified in  #A2
**New assumption**: Actions can have multiple outcomes (a relaxation of #A2)

Finite state space $S$
## Components of #MDP
- Finite state set $S$ where $|S|=n$
- Finite action set $A$ where $|A|=m$
- Transition probability function $T(s_i,a,s_j)$
	- Probability that action $a$ transitions system $\Sigma$ from state $s_i$ to $s_j$  is given by: $T:S^2\times A\to[0,1]$
	- This is the relaxation of #A2 
- bounded, real-valued reward function $R(s):S\to\mathbb R^n$
	- This replaces goals from classical planning
	- can be generalized to include action costs, as in $R(s,a)$
	- can be stochastic (be replacable by expectation)

## Assumptions
- Markovian dynamics (history independence)
- Markovian reward process (reward don't change over time)
- Stationary dynamics and reward (transition probabilities don't change over time)
- Full observability of the state
	- i.e., we know what STATE we're in

## A Solution is a policy ("plans" for MDP)
Goal is to compute a **policy** ($\pi : S\to A$): a stochastic mapping from states to actions

# MDP: Simulation-based representation
Oten, we have a simulation even when we can't explicitly express the domain as an MDP
A simulation igives S, A, R, T

# Monte-Carlo Tree Search #MCTS
Simply search state space by taking all actions with equal probability. Like a Breadth First Search (BFS) over state space, but rewards are back-propagated

**Works well with trees** with relatively low branching factor

# Upper Confidence bounds applied to Trees (UCT) Algorithm

Most popular monte-carlo tree search #MCTS algorithm is #uct-algorithm
Often used in games where reward is given **at the end of play**.

Improves on #MCTS by dedicating search time toward areas of the tree that are more promising.

The algorithm is similar to a **Best First Search**, but remember rewards are back-propagated up the tree. 
The tree policy has several components:
- $Q(s,a)$: average reward received in the current trajectory (branch) after taking action $a$ in state $s$
- $n(s,a)$: number of times action $a$  taken in state $s$
- $n(s)$: number of times state $s$ encountered

UCT expands nodes according to the policy:
$$\pi_{UCT}=\text{argmax}_a \left ( Q(s,a)+c\sqrt{\frac{\ln n(s)}{n(s,a)}}\right)$$
**Understanding this formula:**
The average reward of the best action is bias toward exploration because of the additive factor. The idea here is that if a state has been encountered few times, then $\ln n(s)$ will be small. The $c$ here tells us how strong this biasing is.

#question the constant $c$: from above, can we treat it like a learning rate or the temperature in simulated annealing? Could we have it larger at the start and then decrease as time to make a decision shrinks?

## Example
Available at: [CS6700-UCT.pdf (cornell.edu)](http://www.cs.cornell.edu/courses/cs6700/2016sp/lectures/CS6700-UCT.pdf)

![[UCT vs Minimax Tree Monte-Carlo.png]]
Interestingly, in Chess, UCT can distinguish b/w good and bad moves despite shallow traps. With deeper traps, good and bad moves start looking the same to UCT. So a deep Minimax search has an advantage in the presence of traps.

# Playing Football
One of Gita's students wrote a paper to play a 2D football game. They used #SVM to identify a play, and were able to identify the offense's play by timestep 3.

