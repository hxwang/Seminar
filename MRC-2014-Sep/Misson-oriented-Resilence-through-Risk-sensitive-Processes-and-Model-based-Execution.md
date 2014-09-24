Mission-oriented Resilience through Risk-sensitive Process and Model-based Execution
---

- by *David Wang*, *Eriz Karpas*,  *MIT*

### Intro
- Planning for uncertainty, planning with change constraints

### tBurton: planning with Controllable Durations
- Planning with probability constraints, uncertainty

### Rubato: checking the consistency of Plans with Probabilistic Durations and Change constraints
- Solve controllable constraints incrementally

### Temporal Landmarks: What must have
- Landmarks in classical Planning
	- a landmark is a logical formula over the propositions which must hold in all valid plans at some point
- Temporal Landmarks
	- include the temporal information into landmark and define two types of landmark
		- a temporal fact landmark 
		- a temporal action landmark
	- instead for ordering. they maintain a set of simple temporal constraints between the time point variables of the landmark
- Valid Landmarks
	- if for any schedule, there exists a mapping...
- Non-temporal landmark
- Example Problem: Temporal Landmarks
	- The goal must hold from some point tg until the end
 
### Discovering the Temporal Landmarks
- Given a set of temporal landmarks, we can derive more temporal landmarks by reasoning over the problem description
- Trivial PDDL Temporal Landmarks
	- every action must have a start and an end
	- every event must have its condition hold when it happens
- Trivial TCA temporal landmarks

### Heuristic Based on Temporal Landmarks
- It is possible to obtain a set of actions which must occur from the landmarks, and
	- count them or sum their costs(as in ...)
	
### Extending Execution Monitoring
- Propagates temporal constraints to determine execution time
- monitor causal links to check feasibility of execution

### Resource Allocation for Vehicle Routing
- Problem: given a set of customers, and a fleet of vehicles to make deliveries, find a set of routes that services all customers at minimum costs
	- Planning implicitly allocates resource to achieve goals
	- Knowing resource limits can be critical to achieving a feasible plan 
	- e.g., it may be impossible to transfer a large video in-time
	- Negotiating with constraints
	
### Question
- similar to scheduling problem
- can be applied for insurance?
- can the goal really be achieved, or only with probability
- using the landmark, does that mean the big problems have been divided into multiple sub problems?
- what technique has been used to solve this problem


### Extension
- can the negotiate process be used in green data center
	- negotiate to decide whether still want to finish the taks?? negotiate about the quality?
