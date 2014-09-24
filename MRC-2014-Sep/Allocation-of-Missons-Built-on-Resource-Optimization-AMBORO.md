Allocation of Missions Built on Resource Optimization(AMBORO)
---

- by *Mark Boddy, Adventium Labs*

### Structure
- Mission Model
	- hierarchical task model with parameterizing passing, sequential/synchronous sub-tasks..
- Network Model
	
### Idea
- use replication to achieve mission resilience

### Multiple Attributes of Value
- probability of failure
- add task values to get expected utility
- extend by adding confidentiality
	- using same probabilities as for task values
	- no separate "value of the secrets" per task.
	- Note that both of these restrictions can be relaxed, should a given scenario require it.

### General Model of Redundancy
- Multiple instances of a given task, possibly but not necessarily separate in time or space, so as to reduce the task of successful attacks on availability/confidentiality/integrity.
- What's a task?
	- A single activity
	- ...

### Effects and Implications
- Replication(at east one), addressing availability
- Trading utility and confidentiality
- Trading reliability for value

### Scenario
- After generating an initial plan, AMBORO replans as three unforeseen events occur in succession
	- a new ship arrives
	- communication capacity is reduced
	- new information indicates that the JIE cloud may have been compromised.
- Replanning results
	- new ship brings additional task of values
	- reduction in resources leads to reduction in both redundancy and task value
	- reduction in reliability leads to change in task locations, and in balance between mission success and confidentiality
	
	
### Question
- how to model the problem for optimization?
- how to solve the optimization problem?
- this is a stochastic process, since current approach may not be optimal for the future, in this sense what can be done to improve the overall performance?
- can prediction be helpful?
- can machine learning approach be helpful