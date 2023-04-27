Discussed during [[Lecture 08]]. 
Panopto video: [Sukthankar CAP 6671 on 2/8/2023 (Wed) (panopto.com)](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=f0190f35-d0db-41bf-b5dc-af8100e24a2e) starts at 17:00
This topic will be on the [[Lecture 18 Final Exam Review#Robocup|Final Exam]]


![[Lecture 08#Role allocation]]

# The Algorithm
Use a sorting-based mapping technique. Rather than thinking about each assignment as having a cost, use Lexicographical sorting each individual mapping in order from highest cost to lowest cost. (Similar to the [The Jar of Life (YouTube)](https://youtu.be/cMBM7K_yHog?t=58))

Aim of the process:
- Minimize the longest distance
- Avoid collisions
- Dynamically consistent (over time)

For position $P1$, there are 3 options: either A1, A2, or A3 gets it (see left-most column below). 
If agent A1 is assigned to position P1 ($A1\to P1$), then there are two remaining possibilities for assigning P2. So, given $f_v(A1\to P1)$, either $A2\to P2$ or $A3\to P3$ (ref column 2 below).

![[dynamic-role-assignment-table.png]]

![[dynamic-role-assignment-algorithm-pseudocode.png]]


> [!HINT] Benchmarking
> Gita also mentioned Peter Stone's team at UT Austin does very good benchmarking. 
> ![[dynamic-role-assignment-benchmarks.png]]
> ![[dynamic-role-assignment-results.png]]