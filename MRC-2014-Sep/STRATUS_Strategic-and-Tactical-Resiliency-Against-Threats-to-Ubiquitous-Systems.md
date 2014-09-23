STRATUS: Strategic and Tactical Resiliency Against Threats to Ubiquitous Systems
---

- by *Mark Burstein*, Smart Information Flow Technologies
- [Related article](http://ieeexplore.ieee.org/xpl/articleDetails.jsp?arnumber=6498378)

### Mission Model
- Purpose
	- Evaluate Expected Mission resilience given, i.e., degree of mission completion under attack
- Model
	- Utility/Aggregation Function
		- And-Nodes: multiplication
		- OR-Nodes: summation
	- Utility of single task

### Approach to Partial Observability
- Don't use HMM, CRF or other statistical model
	- because many actions in the security domain are not partially observable so you would paying a price
- Pre-process rewrites the plan grammar to ...
	
### SPAR: simple probabilistic Attack Recognizer
- Alternative approach to plan-based threat recognition
- calculate **the probability of an attack on every resource in the network**
	- these probability are sensitive to the utility of those ...

### MFID: Sensor Fusion for STRATUS
- Fusion: the process or result of joining two or more things together to form a single entity
- Three mechanisms implemented in MFID
	- Retrospection, go back and find evidence that now seems relevant
	- Actively engage sensor exercises that are too expensive to use indiscriminately
	- *Gisting*--trigger a complex hypothesis, to guide gathering of relevant information

	