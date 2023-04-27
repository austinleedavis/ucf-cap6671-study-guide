Introduced in [Sukthankar CAP 6671 on 1/23/2023](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=bd1895e9-83de-44ff-9dee-af8100e24963) at 40:14
Will be on [[Lecture 18 Final Exam Review#Planning]]

# Take-away:
Goals cannot always be disentangled; planner **must** interleave goal achievement

# The problem

The **Sussman anomaly** is a problem in [artificial intelligence](https://en.wikipedia.org/wiki/Artificial_intelligence "Artificial intelligence"), first described by [Gerald Sussman](https://en.wikipedia.org/wiki/Gerald_Sussman "Gerald Sussman"), that illustrates a weakness of noninterleaved [planning algorithms](https://en.wikipedia.org/wiki/Planning_algorithm "Planning algorithm"), which were prominent in the early 1970s.

In the past, people typically would subdivide their plans into subgoals and plan toward their subgoals. **Sussman showed that even for extremely simple worlds, dividing into subgoals which are achieved in a sequence doesn't guarantee work in general**. 

# Example

Given 2 subgoals:
- A on B
- B on C

The agent must stack the blocks such that A is atop B, which in turn is atop C. However, it may only move one block at a time. (Note: All three blocks can be placed on the table at once; unlike the tower of Hanoi problem). The problem starts with B on the table, C atop A, and A on the table:

[![Sussman-anomaly-1.svg](https://upload.wikimedia.org/wikipedia/commons/thumb/4/44/Sussman-anomaly-1.svg/300px-Sussman-anomaly-1.svg.png)](https://en.wikipedia.org/wiki/File:Sussman-anomaly-1.svg)

However, **noninterleaved planners** typically separate the goal (stack A atop B atop C) into subgoals, such as:

1.  get A atop B
2.  get B atop C

Suppose the planner starts by pursuing Goal 1. The straightforward solution is to move C out of the way, then move A atop B. But while this sequence accomplishes Goal 1, the agent cannot now pursue Goal 2 without undoing Goal 1, since both A and B must be moved atop C:

[![Sussman-anomaly-2.svg](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2e/Sussman-anomaly-2.svg/300px-Sussman-anomaly-2.svg.png)](https://en.wikipedia.org/wiki/File:Sussman-anomaly-2.svg)

If instead the planner starts with Goal 2, the most efficient solution is to move B. But again, the planner cannot pursue Goal 1 without undoing Goal 2:
[![Sussman-anomaly-3.svg](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4d/Sussman-anomaly-3.svg/300px-Sussman-anomaly-3.svg.png)](https://en.wikipedia.org/wiki/File:Sussman-anomaly-3.svg)

The problem was first identified by Sussman as a part of his PhD research. **Sussman (and his supervisor, [Marvin Minsky](https://en.wikipedia.org/wiki/Marvin_Minsky "Marvin Minsky")) believed that intelligence requires a list of exceptions or tricks, and developed a [modular](https://en.wikipedia.org/wiki/Modularity "Modularity") planning system for "debugging" plans.**


