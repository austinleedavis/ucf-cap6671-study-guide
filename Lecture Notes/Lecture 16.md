title:: Monte Carlo Localization; Simultaneous Localization and Mapping
date:: 2023-03-20
status:: Complete
[[Lecture 15|<<prev]] | [[Lecture 17|next>>]]

# Localization techniques
- Open loop **pose estimation**
	- maintain pose estmimate based on results of motion commands (no sensing)
- Dead reckoning
	- Using sensors

# Bayes formula

uses #bayes formula

$$ P(x|y)=\frac{P(y|x)P(x)}{P(y)}= \eta P(y|x)P(x)$$
Since sensor data is essentially the same, 

We typically assume sensors are conditionally independent

## Example
Given:
$P(z|open)=0.6$ and $P(z|\neg open)=0.3$
$P(open)=P(\neg open)=0.5$

then...
$$P(open|z)=\frac{P(z|open)P(open)}{P(z|open)P(open)+P(z|\neg open)}$$

# Robot Localization 
**Robot kidnapping** (global problem) vs **Robot tracking** (local problem)

## Problem:
Localization via image processing typically failes because of noise in the data


## Monte Carlo Localization
Solves by repeatedly sensing and using bayes to update its model of its position.

$$P(p_1|S)$$

A robot moves through the map (which must be known *a piori*) and we update 

**particle filters** are assigned an equal weight and assuming 


# Simultaneous Localization and Mapping (SLAM)
#Gita likes to think of #SLAM as a big jigsaw puzzle

- Full SLAM: Estimates entire **path** and map
- Online SLAM: Estimates most recent **pose** and map


# FastSLAM
The landmarks' poses are conditionally independent, given the robot's path
In orhter 


