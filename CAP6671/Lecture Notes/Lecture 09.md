title:: Starcraft
date:: 2023-02-13
status:: 
[[Lecture 08|<<prev]] | [[Lecture 10|next>>]]

# UAlbertaBot
University of Alberta built the *UAlbertaBot* and showed they performed well across several experiments including:
- Micro Search where various army mixes are pitted against others
	- #evaluating was done based on win percentage


![[lecture09-UAlbertaBot.png]]
UAlbertaBot specialized in Production and Planning

![[Lecture09-CommanderAlgorithm.png]]
Notice that Build-order optimization and MicroAISystem is only allowed to run for a certain amount of time. 

# Research Areas

Build order optimization
- Identify the fastest production/resource gathering strategy for building units via, e.g., #branch-and-bound search
Tactics
	- Micro-management , e.g., #uct-algorithm 
	- kiting: using mobility to avoid troop loss
- Opponent Modeling
	- identify if players are trying to rush you
	- predict their build orders
- 