title:: Final Exam Review
date:: 2024-04-19
status:: Complete
[[Lecture 18 (part 2) End of Course Summary|<<prev]] | [[README|next>>]]

The following sections come from Lecture 18 (Recording available on [Zoom (ucf.edu)](https://webcourses.ucf.edu/courses/1422160/external_tools/305492)), where Gita gave a review for the Final Exam. The markdown below was initially created based on Gita's slides.

When you see a topic/algorithm in **bold**, that topic will very likely have a workout problem on the Final Exam.


# Admin
## Announcements
- Class cancelled on Mon
- Grades released for the RLAgent assignments and Presentations
- Final projects
- 1 week extension possible but I recommend that you finish by this weekend.
- Final exam to be given as an open book timed Webcourses quiz
- 3 hours in duration
- To be taken some time between Apr 26 - 29
- Make sure that you have a good internet connection since I don’t allow exam retakes. 2


## Exam Material
- No material on ROS
- No material from the student presentations.
- Everything else (assignments, papers, and lecture notes) is fair game
- **Most of the focus will be on the lecture notes** but since this is open book I will ask a few detailed questions about the papers!


## Exam Format
- To be made available as a webcourses quiz.
- Can be taken between Apr 26 - 29
- Open book but no collaboration with other people!
- No ChatGPT usage
- Short answer (3-4 sentences) about a specific point in the paper
- You will have to understand how the algorithms and systems work; you will be expected be specific
- Minimal math required


## Example Question
- How does a plan differ from a policy? (**supplement your answer with definitions and examples**)
	- Answer: "A policy is a mapping between states and actions (a universal plan). A plan is one specific, temporal ordering of actions. A plan in the dock worker robots domain would be pick up crate X, put it on pad B, etc." -Gita

# Content

## Multiagent Systems
- **[[RETSINA]]** multiagent system 
	- General organization
	- Overview of internals of system
- Definitions of [[MAS coordination types]]
	- *Understand Game theoretic styles vs coalitions
		- Game theory introduced in [Lecture 06 on 2/1/2023](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=98c32ed3-2ba8-4378-be4d-af8100e249eb) at 12:33
- [[MAS Research questions]]
- Case studies of using MASs for aircraft maintenance and military planning
	- Reference [Sukthankar CAP 6671 on 1/18/2023](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=5fa6aa84-0fd1-4c46-a8c2-af8100e2493a) at 42:30

## Planning
- [[Dock Worker Robot (DWR) domain]]
- [[Planning vs Scheduling]]
- [[STRIPS notation]]
- Must know  **[[Graphplan]] #graphplan  
	- She WILL give us an example here**
- Do not need to understand internals of UCPOP
- Must understand general ideas behind #HTN planning (Summary in [[@Kelly2008]])
- Understand **[[Limitations of classical planning]]** and issues such as the **[[Sussman anomaly]]**
- [[Monte Carlo search]] #MCTS
- [[Bandit algorithms]] 
- **Upper Confidence bounds for Trees** #uct-algorithm [[UCT Algorithm]]
	- Know how to calculate UCT

## Trading Agent Competition
- This topic was discussed in detail in [[Lecture 08]]. 
- Must understand basic rules of [[TAC Classic competition|Trading Agent Competition#Rules]]
- Must understand ideas behind combinatorial valuation and **bidding** See: [[@Greenwald2012]]
- Must understand general operation of ATTac and Roxybot (See [[@Greenwald2009]])
- **[[Markov Decision Process]]** #MDP 
- General ideas behind **Sample Average Approximation** See: [[@Greenwald2009]]
- Not responsible remembering details of competition results

## Robocup
- General research questions
- Problems addressed by specific leagues
- Details of the [[CMU-United team]] (TPOT-RL, potential field mechanisms, locker-room coordination)
- UT Austin Villa's **[[dynamic role assignment and positioning system]]**
- Selectively Reactive Coordination architecture
- Urban Rescue league and HRI issues
- No need to remember the specific results from competitions

## Starcraft
- Description of the competition
- What makes RTS games interesting for AI. Answer: 
	- Imperfect information
	- Real-time requirement limits computation time
	- Opponent (e.g., exploitation of poor strategies) modeling
- Bot internals
- Unit micro strategy experiments:
	- Read Eval section of [[starcraft.pdf]]

## Reinforcement Learning
- Just watch [Q Learning Explained (tutorial) - YouTube](https://www.youtube.com/watch?v=aCEvtRtNO-M)
	- **Q-learning** "How tabular Q-learning works"
	- Exploration vs. exploitation for policy search
	- Value iteration
	- Difference between Model-free vs. model-based RL
- **Transfer learning**
	- Case study for Robocup (a paper on this)
- Multi-agent learning (TPOT-RL)



## Deep Learning Review
("Will try not to make these questions too difficult")
- Perceptron and perceptron learning rule
- **Neural network** and backpropagation
	- How Convolutional NN and max pooling layers work
	- Do not need to know recurrent RNNs and LSTMs
- **DQN** (basic algorithm "IN DEPTH", and what the purpose of those components are)
- Policy gradient and actor critic

## Robotics: Path Planning
- Terminology and Fundamental concepts of map representation 
- **A*** and real-time **A***
	- One detailed question about A*
- Wavefront planner
- Workspace vs. configuration space
- Sampling planners (RRT, PRM) (We Read a paper on RRT)
- Graph-based planning and extraction (e.g., Voronoi/visibility graphs)
- No questions on ROS

## Robotics: Localization
- Must understand **Bayesian updating**
	- "Understand how Baye's Rule works"
- Must understand the process of belief update on maps
- Must understand operation of **Monte Carlo localization**
	- "Definitely understand how MC localization works"
- Must understand general research issues behind mapping, localization and coverage
- Must understand general SLAM problem and these approaches:
	- FASTSLAM
	- Kalman filter

## Multi-robot Coordination
- Auction-based approach
- CoCOA: Mixed-integer linear programming
	- Basics behind this
- General problem: Multi-agent Path Finding
	- "No paper on this, just understand the general problem"



