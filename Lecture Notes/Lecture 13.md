title:: Transfer Learning
date:: 2023-03-01
status:: Complete
[[Lecture 12|<<prev]] | [[Lecture 14|next>>]]
# Reading to Discuss
- Matthew E. Taylor and Peter Stone. Cross-Domain Transfer for Reinforcement Learning. In Proceedings of the Twenty-Fourth International Conference on Machine Learning, June 2007 (contains some of the same material)  
- Pan and Yang, Survey on Transfer Learning, IEEE Transactions on KDE, 2009  
- Transfer Learning https://www.ruder.io/transfer-learning/

# Transfer Learning
Definition: Transfer learning (TL) is the practice of recognizing and applying knowledge and  skills learned from one or more previous tasks to  more efficiently and/or effectively learn to solve  novel tasks (in new domains).  

Or: Situation where what has been learned in  one setting is exploited to improve  generalization in another setting.  

§There are many techniques that can be used to  to do the transfer; no single dominant method  has emerged yet.

![[TransferLearning1.png]]
![[TransferLearning2.png]]

DARPA did a whole program on Transfer Learning, and in all these programs they want to carefully evaluate all the teams to see how they were doing. There are a few different ways to show you achieve benefits.
![[Pasted image 20230301183257.png]]
- Compare With training vs without and achieve a **faster training rate** on a new task, but ending up at the same level (Bottom Left)
- Start at a higher starting point (Top Right)
- Goal: Achieve better asymptotic performance (Bottom right)

# Transfer Learning in RL
You have agents which are asked to do slightly different things, reducing the training time via a **jumpstart** or a **time to threshold** or a **better asymptotic performance**

# TL in Robocup
**Question:** How can we transfer learning from other types of tasks to Robocup or its subtasks like keep away?

The interesting thing is they wanted to look at transfer between very different tasks:
- **Keep away**: Keepers are given information about the angles with action state A={hold,Pass1,Pass2}, it's a game of understanding the angles, and determining which pass is the most advantageous.
- **Ring world game**: Rewarded for staying away from opponent, moving toward target 1 or target 2, when player is contrained on a ring
- **Knights Joust**: Players alternate moves on a grid, can move A={N,E,W}. Player rewarded for advancing distance from player to Goal.

Features and actions were very different. So researchers *hand-coded* translation functions between state variables and actions.

## Rule Utilization
- **Value bonus**: Give constant bonus to Q-value as recommended by the translation decision list
- **Extra action**: add action to target task such that when the agent selects the pseudo-action it floows the action recommended by D ( have exploration policy favor this action)
- **Extra Variable**: Add extra state variable to target state description that take s on the value of the indext for the action recommeneded by D (have exploration policy favor this action)

Used SARSA: "State-Action State-Reward-State Action"

Do RL on original task, then summarize RL policy using a decision tree summarizing the source task. Allows you to create a more abstract model

RIPPER comes up with an abstraction of the policy rather than raw RL policy. `GrowRule` adds conditions to an empty conjuction, `PruneRule` deletes conditions to make the rule more general

## Evaluations
Ringworld performed better by playing keepaway with best performance in Extra Action. Knights Joust and Keepaway only benefitted on its initial performance.

## Future Work
- Automatically dferive the rule translation function
- General approach for deriving translation:
	- Identify state variables that are near 0 when episode ends
	- etc. etc

# Transfer in Deep Learning
Use the representation learned by one nerual network as a starting point on a second machine learning system. (example: Pre-trained models in computer vision)

## Deep Transfer
For RoboCup, the label space is actually the action choices. So, given a source and target domains $D_S$ $D_T$ where $D=\{X,P(X)\}$ and source and target tasks $T_S$ and $T_T$ where $T=\{Y,P(Y|X)\}$ source and target conditions can vary in four ways:
1. $X_S\neq X_T$: For instance, when documents are written in different languages
2. $P(X_S)\neq P(X_T)$: Domain augmentation
3. $Y_S\neq Y_T$: Documents need to be assigned different labels across two tasks
4. $P(Y_S|X_S)\neq P(Y_T| X_T)$: Source and targets are unbalanced regarding their propability distributions

This led to a taxonomy of possible TL solutions:
![[Pasted image 20230301185441.png]]



