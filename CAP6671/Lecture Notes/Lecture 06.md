title:: Trading Agent Competition
date:: 2023-02-01
status:: 
[[Lecture 05|<<prev]] | [[Lecture 07|next>>]]

# Roxybot Architecture 
*This is less important than understanding the SAA algorithm from [[@Greenwald2009]]*
Roxybot was a 2-part system
- Allocator
	- Used A* search with admissible heuristic
	- To levels for allocation: Allocated hotels and flights first, then alloccated entertainment prices
- Completer
	- Variable-width beam search
	- Price trajectories were learned 
	- Bidding used Sample Average approximation instead of MU

## Research problems:
- Rapid optimization
- Computational value of items
- robust strategies
- Prediction of future prices
- planning under uncertainty
- Adversarial strategies

