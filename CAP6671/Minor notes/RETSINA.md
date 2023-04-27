RETSINA was discussed in detail during Lecture 02 [Sukthankar CAP 6671 on 1/18/2023](https://ucf.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=5fa6aa84-0fd1-4c46-a8c2-af8100e2493a)

Will be on the [[Lecture 18 Final Exam Review#Multiagent Systems]]

Reusable Task-Structured Intelligent Networked Agent Architecture ("RETSINA", which happens to also be a Greek Liquor) is an example of a **Hybrid architecture**, where the agents contain deliberative and reactive components.
- Originally implemented in Perl in 1995; later converted to Java

# General organization
![[RETSINA Agent Diagram.png]]
- Each RETSINA Agent had four modules:
	- **Communications handler**
		- Each Agent primarily gains information from other sources. 
		- Thus communication was very important 
		- Comms conducted via [[KQML]] (roughly similar to human dialogue, i.e., KQML is human-readable) 
	- **Planner** which used task structures (i.e. pre-planned recipies) to complete certain goals
	- **Scheduler**: Decided how to schedule actions in the plan
	- **Execution monitor**: Determined how it was progression toward goal
- Diagram above shows flow of information as either a **Control Flow** and **Data flow**

# Main idea
The **main idea of RETSINA is** to have different categories of agents. 
The idea is to create a single program, you would select a group of agents suitable to your task.

![[Pasted image 20230421112559.png]]
Those categories of agents are:
- **Interface** Agents: Specialized in dealing with people
- **Task Agents**: special purpose for solving specific problems (e.g., route planning)
- **Middle (Matchmaker) Agents**: "Glue behind the system" -Gita (See [[RETSINA#Types of middle agents]])
- **Information Agents**: knew about information sources

## Types of middle agents

### Matchmaker
![[Pasted image 20230421113102.png]]
When an agent needed something, it would send requests for a service to the middle agent (Matchmaker) which would contact other agents individually.
### Broker
![[Pasted image 20230421113325.png]]
