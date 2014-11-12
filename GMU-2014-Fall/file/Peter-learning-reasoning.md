## Learning and Multiagent Reasoning for Autonomous Robots

- speaker: Peter Stone
- location: RH163
- data: 11/12/2014

### Abstract
Over the past half-century, we have transitioned from a world with just a handful of mainframe computers owned by large corporations, to a world in which private individuals have multiple computers in their homes, in their cars, in their pockets, and even on their bodies. This transition was enabled by computer science research in multiple areas such as systems, networking, programming languages, human computer interaction, and artificial intelligence. We are now in the midst of a similar transition in the area of robotics. Today, most robots are still found in controlled, industrial settings. However, robots are starting to emerge in the consumer market, and we are rapidly transitioning towards a time when private individuals will have useful robots in their homes, cars, and workplaces. For robots to operate robustly in such dynamic, uncertain environments, we are still in need of multidisciplinary research advances in many areas such as computer vision, tactile sensing, compliant motion, manipulation, locomotion, high-level decision-making, and many others. This talk will focus on two essential capabilities for robust autonomous intelligent robots, namely online learning from experience, and the ability to interact with other robots and with people. Examples of theoretically grounded research in these areas will be highlighted, as well as concrete applications in domains including robot soccer and autonomous driving.

### Biography:
- Dr. Peter Stone is an Alfred P. Sloan Research Fellow, Guggenheim Fellow, AAAI Fellow, Fulbright Scholar, and University Distinguished Teaching Professor in the Department of Computer Science at the University of Texas at Austin. He received his Ph.D in Computer Science in 1998 from Carnegie Mellon University. From 1999 to 2002 he was a Senior Technical Staff Member in the Artificial Intelligence Principles Research Department at AT&T Labs - Research. Peter's research interests include machine learning, multiagent systems, robotics, and e-commerce. In 2003, he won a CAREER award from the National Science Foundation for his research on learning agents in dynamic, collaborative, and adversarial multiagent environments. In 2004, he was named an ONR Young Investigator for his research on machine learning on physical robots. In 2007, he was awarded the prestigious IJCAI 2007 Computers and Thought award, given once every two years to the top AI researcher under the age of 35. In 2013 he was awarded the University of Texas System Regents' Outstanding Teaching Award and in 2014 he was inducted into the UT Austin Academy of Distinguished Teachers.



### Introduction
- PC progress
	- 2008: an estimation one billion PCs in the world
	- 2014: two billion PCs
- Robot progress
	- Amazon uses robots to archive goods
	- Towards ubiquitous robots
		- many products: iRobot
	- Goal of AI: create full autonomous in the real world
		- how: break the problem into small pieces
	
### Layer learning
- Learning in one year feeds into next year
- First applied in simulated robots	
	- individual: ball perception
	- multiagent: decision tree
	- team: pass selection
- Overlapping layer learning
	- freezing some previous layers
- Learning
	- fast walking
	- ball control
- Robotcup champion 2011, 2012
	- humanoid walk learning via layered learning and CMA-ES
		- parameterized double linear inverted pendulum model
		- stochastic, derivative-free, numerical optimization method
		- candidates sampled from multidimensional Gaussian
			- mean maximizes likelihood of previous success
			- covariance update previous search step sizes
		- Pros: transition smoothly, otherwise will fall down

### Robot vision
- great procession in computer vision
	- shape modeling, object recognition, face detection
- but robot vision
	- mobile camera, limited computation, color features
- Autonomous color learning	
	- learn color map based on known object locations
	- recognize reacts to illumination challenge

### Other good AI challenges
- trading agents
- autonomic computing
- ...

### Robot learning
- supervised learning mature [WEKA]
- but for robots, reinforcement learning most appropriate
- state, reward, action, agent, environment, agent, policy
- reinforcement learning
	- foundational theoretical results
	- ...

### Selected RL Contributions
- human interaction
	- active, demonstration
	- positive/negative feedback
- transfer learning for RL
- adaptive/hierarchical representations
- TEXPLORe for robot RL
	- sample-efficient,real-time 
	- continuous states, delay effects

### Multiagent Reasoning
- once there is one, there will be many
- to coexist, agents need to interaction
	- e.g., autonomous vehicle
	
### Ad Hoc Teams
- Ad hoc team players in an individual	
	- unknown teammates (programmed by others)
- Teammates likely sub-optimal, no control
