---
title: RoxyBot-06: Stochastic prediction and optimization in TAC travel
authors: Amy Greenwald, S Lee, Victor Naroditskiy
year: 2009
note: week04
pdffile:: RoxyBot06.pdf
---

Will be on the [[Lecture 18 Final Exam Review#Trading Agent Competition]]
Discussed in [Sukthankar CAP 6671 on 2/1/2023 (Wed) (panopto.com)](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=98c32ed3-2ba8-4378-be4d-af8100e249eb) at 43:18
This paper was discussed during  [[Lecture 06]] 

# Sample Average Approximation
Like the expected value method, sample average approximation is an intuitive way of approximating the solution to a stochastic optimization problem.
## General Idea
The idea is simple: 
1. generate a set of sample scenarios $S$, and
2. solve an approximation of the problem that incorporates only the sample scenarios

For Sample Average Approximation, over the sample $S$, the authors write:
> Ahmed and Shapiro (2002) establish the following result: as S → ∞, the probability that an optimal solution to the sample average approximation of a stochastic program with integer recourse is an optimal solution to the original stochastic optimization problem approaches 1 exponentially fast. Given hard time and space constraints, however, it is not always possible to sample sufficiently many scenarios to infer any reasonable guarantees about the quality of a solution to a sample average approximation. Hence, we propose a modified SAA heuristic, in which SAA is fed some tailor-made “important” scenarios, and we apply this idea to the bidding problem.


