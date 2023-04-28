title:: Mapping
date:: 2023-03-08
status:: 
[[Lecture 14|<<prev]] | [[Lecture 16|next>>]]

# Definitions

- **Mapping**: updating the world model with information gained from the sensors
- **Coverage**: creating/executing a plan or policy that will guarantee (to some reasonable degree of certainty) that the robot has visited all reachable areas
- **Localization**: identifying the robot’s location in an absolute coordinate frame on a map known in advance
- **Simultaneous Localization and Mapping**: localizing in an unknown region based on combining discovered landmarks with sensor data

# Mapping

## Challenges of Mapping:
- Exploration (global coverage)
- Measurement (local coverage)
- Validity (correctness, guaranteed error bounds)
- Currency (freshness vs staleness)

## Sensory-based maps
We will assume the robot has sensors (e.g., LIDAR, SONAR, RADAR)
We would like to build a map by fusing data over many iterations
We want to combine the data to create a map.

Previously, we would build a map of obstacle locations.
Now, we build a map of probabilities, e.g., we want $P(o|S)$ or $P(\overline{o}|S)$ 

![[Mapping example, occupancy of tree-lined path.png]]

# Bayesian Updating
## Bayes Rule
Bayes rule allows us to get from a sensor model to a decision model.
- Probability of two events is 
	- $P(o\wedge S)=P(o|S)P(S)$, and
	- $P(S\wedge o)=P(S|o)P(o)$
- Bayes Rule switches the conditioning event:
	- $$P(o|S)=\frac{P(S|o)P(o)}{P(S)}$$
- We will assume *conditional Independence* of events: 
	- $P(S_1\wedge S_2|o) = P(S_1|o)P(S_2|o)$

## Representation and Updating
Typically, we use odds (especially $\log(odds)$) rather than probabilities to maintain numerical stability (probabilities)

Updating means the following: Given the old occupancy odds $odds(o |S_1) = \frac{p(o|S_1)}{p(\neg{o}|S_1)}$ and a new sensor reading, $S_2$, we want the new occupancy odds, i.e., we want $$odds(\neg o |S_1\wedge S_2) = \frac{p(o|S_1\wedge S_2)}{p(\neg{o}|S_1\wedge S_2)}$$
Combining evidence involves the following steps:
![[baysian-odds-update.png]]
- This process is very fast and simple
- Pointing the sensor at the same location for long periods of time will increase resolution



> Side note: we typically know the physical characteristics of the sensor (e.g., the reliability range for the sensor). So, we typically apply a cone-shaped or distance-scaled update rule to our map.
