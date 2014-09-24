Autonomous Collaborative Control for Resillient Cyber Defense(ACCORD)
---

- by *Scott Alexander*, Applied Communication Sciences

### Intro
- Network Path Divery Path


### Network Path Diversity Path
- from the war fighers' view, the path is a blackbox
- thus we need to "fight through" mechanims to maintain communication
	- e.g. an overlay
- Idea: utilizae intermediate (relays) 

### NPD Transition: Valiant Shield Exercise
- having path diversity can enable the source and destination communication even when there are some obstacles
- Virtual Secure Enclave(VSE)
- Control traffic
	- during demo preparation, we identified that NPD control traffic must always be diverged


### Mission-aware file transfer problem context
- database synchronization across a shared network
	- the objective is to coordinate the network acess to maximize the overall utility

### System-Level approach
- NBS dictates the rates that you would like to achieve given current knowledge of constaints and file transfer progress
- Ongoing measurements of flow behavior
- Feedback control of stack parameters reduces error between desired and actual rates

### Nash-bargaining

### Deadline-aware NBS to apportion throughput
- adapt deadline-aware NBS for comute resources to allocate achivement throughput to jobs
- given job proirities, job sizes, job deadlins and their types(hard, soft deadline), and network state, can determine job s which share them.
In order to improve job throughputs via NBS optimization.

### Inferring shared links and capacities
- can we learn bottleneck links and their capacities in the network, from observation only at the edge of the network
- Intuition, it may be sufficient to know only shared bottleneck links, their capacities and the jobs which share  them. In order to improve job
throughputs via NBS optimziation.
- Observation. We observe job throughputs that the edge via stack instrumentation.
- Hypothesis, shared links and capacities can be..

###　Experiment
- Experiment Setpup
	- construct a network with 10 nodes
	- create 6 explicite path among the nodes such that the paths share common links
	- 6 flows with different jobs are sequentially added to the network(two hard, two soft, and two no deadline)
		- each job specifies download size, target finishing time
- Experiment Result
	- improve overall utility by sacrificing performance of some no-deadline jobs and improving performance of hard and soft-deadline jobs


### Question
- how's nash bargaining be appied in the model?
- goal is to achive the overall utility, thus how it different from traditional scheduling problem. I think probably this problem is more complicated 
because you need to take into account the whole graph, such the bottle neck. From pervious, for my research, we only for single machine, but didn't consider the
whole network.
- so can max, min flow be applied?
- but since you can not get the whole graph, it is local optimality?


### Possible extension
- consider the scheduling problem in the scale of a whole network graph, rather than a single machine

	
		