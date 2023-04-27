# Planning Graphs
**Planning Graphs** were introduced  in page 49-50 of [[nau-planning.pdf]]
Introduced in [Sukthankar CAP 6671 on 1/25/2023](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=2d65ec97-5a87-452a-acf9-af8100e2498d) at 13:09


# Graphplan
Gita like #graphplan because it provides great bookkeeping for plan development

The graph produced by Graphplan includes alternating layers of states and actions

Graphplan parallelizes the world:
- Instead of saying "I'm in this state and I can take this action.." 
- Graphplan says, "What are the consequences of taking all possible actions at once?"


## Graphplan algorithm:
The algorithm operates in two phases: 
1. Graph expansion
2. Solution Extraction:
![[Pasted image 20230421124532.png]]

## Example 
Example available at: [graphplan.pdf (pitt.edu)](https://people.cs.pitt.edu/~wiebe/courses/CS2710/lectures/graphplan.pdf)

