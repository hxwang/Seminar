Towards Intrusion Tolerant Clouds
---

- by Yair Amir, John Hopkins University
- [Project Webiste](http://www.dsn.jhu.edu/funding/resilient_clouds/)

### Intrusion Tolerant Clouds Infrastructure

### Intrusion Tolerant Replication
- proactive recovery and diversity for Prime

### Regular secure routing
- regular secure routing under attack
	- k node-disjoint path 
- constrained flooding 
	- if even a single good path exists, flooding will pass message from source to destination
- cutting the network
	- if the attack can cut the network, then no protocol could survive
	
### Intrusion Tolerant Messaging
- Different applications need different message type(e.g. real and delay-tolerant)
- whether you would like to pay to denfend how many attackers? or You want to optimize?

### Diversity Assignment Problem
- MIP solution quickly becomes impractical
	- Must consider (the number of variances)^{the number of nodes}
	- Good solvers use optimizations, but still exploded on graphs with tens of nodes
- Proved to be NP-hard, also APX-hard, i.e., hard even to give an approximation
- Solution
	- use related theory with existing approximation solutions
		- Steiner Tree packing: Scales well, runs much faster

### Steiner Trees
- Problem: find a tree to connect all clients using routers as necessary
- **Minimal Steiner Tree**: use minimum number of routers possible 
- Simulation: compare time, compare disconnectivity

### Prime: Byzantine Replication with Performance Guarantees under Attack
- Solution: defense across space and time

- Fine-grained Diversity
- Proactive recovery
	- periodically initiate proactive recovery in a round robin manner by rejuvenating a replica from a ...
- Proactive recovery sequence
	- replica rejuvenation
		- The replica restarts periodically from a fresh copy of OS and application
	- session of key replacement
	- state validation
	- state transfer if needed
- Theoretical Model
- Experiment: number of replica used, v.s., number of strength



