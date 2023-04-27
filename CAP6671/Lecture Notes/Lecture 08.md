title:: Robocup Research Overview
date:: 2023-02-08
status:: 
[[Lecture 07|<<prev]] | [[Lecture 09|next>>]]

- Determine which **zones** players are playing in
- Analyze player **failures**, understand from a coordination graph *why* something failed
- Learning from demonstration
- Camera-based systems where we're trying to recognize plays based on video footage

# Multi-robot coordination
- Roles
- Spatial position (since positioning is very important given slow speed)

## Role allocation
> 
> Do understand the dynamic programming solution for the [[Lecture 18 Final Exam Review#Robocup|final exam]]
> 
- from: UT Austin Villa 3dD Simulation RoboCup 2011, Peter Stone's research group
-  The authors then solved this using **dynamic programming** (since suboptimal positioning between two robots would be suboptimal in the full team. and conversely optimality in sub-solutions implies full-solution optimality)
- Do not change position mapping before the robots reaches the target position
- Authors used lexicographic ordering to minimize longest distance travelled while, avoiding collisions and remain dynamically consistent
	- Lexicographical ordering here means we're not minimizing **total cost**
		- if 9 players are in position, but 1 player must walk across the entire field, then we're wasting time. Instead, have all 10 players walk a little bit.
	- Seems like it would've been sufficient to just use $L^2$, $L^3$ sor $L^n$ norm for distance, but okay.
-  Voting coordination used to resolve conflicts

#final-project Peter Stone's group from UT-Austin does a good job #evaluating & benchmarking
- Compares against not only other teams, but also other versions of their algorithm

# CM Dragons Team
From the small robots competition; this team won all their games, scored 48 points. 
This team focused in part on computing probabilities that robot players are:
- near the ball
- open for a pass
- likely to receive a pass


# Robocup Rescue Research Issues:
- Autonomy
- Coordinating multiple robots
- Mobility (climb ing ramps, obstacles)
- Perception
	- Fusing multiple sensors
- heterogeneous capabilities
- Human-robot interactions

# HCI Human Computer Interaction
To measure goodness of UI/UX and HCI-teaming behavior, often use a **Wizard of Oz** approach:
- Human thinks they're issuing commands to the robot
- In fact, the robot is controlled by another user who's tipped-off by the UI/UX responses
- This saves much time in development because you can text UI/UX without having to build a robot that responds to it in that particular way.

