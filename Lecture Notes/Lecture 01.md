title::  Introduction
date:: 2023-01-09
status:: Compelete
[[README2|<<prev]] | [[Lecture 02|next>>]]

- Despite course reaching capacity, we can likely attend in-person. 
- "Do not need an exam proctor for this course."
- Publication presentations will occur in ~March

Homework assignments: 
- Writing assignment discussing multi-agent competitions
	- Write a short literature review on one of these topics

**Agents** are entities which exist in and interact with their environment. **Intelligence** implies an ability to observe/sense the environment, execute a course of action, and adapt to changes in the environment. There are many other dimensions of intelligence (e.g., abstraction, planning, emotion, social, coordination). Commonly mentioned desiderata are: deliberative, reactive, learning, adaptive, social, creative, and rational. 

A **robot** is an intelligent agent embodied within a physical system, which implies specialized vision/localization abilities plus the ability to reason about uncertainty.

We have developed several computational approaches toward intelligent behavior: search, numerical optimization, machine learning, and inference.

Approaches to intelligence has changed over time, originally focusing on knowledge representation and search. Machine learning uses (sample) data to minimize a penalty function (combining error metrics and optimization). Robotics is concerned with developing satisficing solutions quickly; thus, robotics emphasizes control, estimation, and bounded errors.

Adding AI/ML to a system comes as a tradeoff: it reduces human-written lines of code and *can* be more flexible/general, but it's very difficult to debug and might be impossible to guarantee a desired performance/safety metric.

AI does not generally need to mimic human intelligence. Broadly speaking if an AI operates in coordination with or alongside humans (e.g., self-driving cars, automated call handling systems, explainable/interpretable systems), it's typically important to mimic human behavior. On the other hand, when there is a very clearly specified objective (e.g., maximizing profits in online digital trading), these systems would typically favor rational decision making over human mimicry.