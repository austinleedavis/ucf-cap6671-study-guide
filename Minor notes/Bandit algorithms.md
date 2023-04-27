Introduced in [[Lecture 05#Monte-Carlo Tree Search MCTS|Lecture 05]]
Video available at[Sukthankar CAP 6671 on 1/30/2023](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=65c5369c-f361-482c-bdfb-af8100e249c4) at 12:39
On the [[Lecture 18 Final Exam Review#Planning|Final Exam]]

Given an MDP with single state and $k$ actions:
- Determine which action has best expected reward
- Can sample rewards by taking actions via simulator calls
- sampling over actions space $\{a_1,...,a_k\}$ is like pulling the arm on a slot machine with a random payoff function $R(s,a)$:
	- $s$ doesn't change, but we have one slot machine for each action. 
	- Goal is to find the arm with the highest reward

# UniformBandit Algorithm
This is the Naïve approach to selecting actions in an MDP
1. Pull each arm $w$ times (uniform polling)
2. Return the arm ($a_i$) with the best average reward

Drawback: too much exploration on actions (arms) that never return a reward

# Policy improvement via Monte-Carlo 
*Note: This section is more motivational of MCTS than anything.*
Given a **multi-state MDP** find the best action or sequence of actions $(a_1,\ldots,a_n)$
**Idea**: Assuming we have a fixed policy ($\pi$) in mind (e.g., random or a heuristic).... 
- Define a stochastic function $SimQ(s,a,\pi,h)$ that we can implement and whose expected value is $Q_\pi (s,a,h)$. 
- Then use a Bandit algorithm (e.g., `UniformBandit` to select the improved action)

To improve the policy, we try to intelligently choose the top of the tree, and then simulate the rest 
![[Policy improvement via Monte-Carlo.png]]

