## Performance Engineering for the Internet of Things

### Abstract
Originally coined to describe networked RFID tags, the Internet of Things (IoT) now commonly refers to global systems of communicating IP-friendly objects. Even after taking into account the hype surrounding the label, proposed IoT systems are expected to require tens of billions of devices, dwarfing current Internet deployments. For these systems to reach their true potential a careful balance must be struck between producing extremely inexpensive and resource constrained devices while simultaneously designing protocols and system software that provide high levels of predictable performance. In this talk I describe recent work in IoT technologies that address this balance, including routing protocols, control plane management and
energy harvesting methods. I also discuss future applications in areas such as smart spaces, smart grids and semi-autonomous systems

### Intro
- The internet of thing is the interconnection of uniquely identifiable embedded computing devices within the existing internet infrastructure.
- Before IoT
	- protocol often proprietary
- IoT
	- global address: all devices are addressable and routable, globally reachable
	
### IOT 
##### IOT Overview 
- e.g., smart grid
	- enhance the real time prices for consumers
	- users can control devices
- reason of IoT
	- IPv6
	- multiple converging technologies
	- moore's law, bells law
- challenge
	- manage the wireless endpoints of the syste,
	- the wireless portion heavily leerages warlier work in unattended wireless sensor networks
- low power and lossy networks
	- nodes are severely resource constrained
		- limited power, memory and processing resources
- performance
	- traditional QoS
		- communication delay, throughput and reliability
	- energy expenditure
	- completing things interactions
		- sensing things all the time

	
##### How to guarantee performance
- research
	- invent precise system models to develop algorithms and implement protocols that have provable performance bounds
- Pre-planed deployments
	- smart metering, 
- basic issue
	- problem: rapidly changing routing trees break coordinated multi-hop performance control
	- example: current IPv6 LLn standard is called RPL
		- falls into a class of routing algorithms known as "gradient'
	- routes can change at any point
	- Node break Problem
		- Node break
			- nodes fails, perhaps temporately, must form new tree
		- In tree-based, can we have multiple channel
			- seems not
			

##### Example Solution: CREST
- Intro
	- CREST: coordinated routing for epoch-based stable tree 
	- design as an intentionally-incomplete LLN control plane overlay
- design idea
	- cannot have full reliability, otherwise too much overhead
- mechanism
	- designed RADIATE on IPv6-based LLN semi-reliable wireless broadcasting
	- uses automatic randomized rebroadcast with selective cancellation



### Energy Harvesting
##### Overview
- types of objectives
	- preserver energy neutrality
	- maximize aggregate energy reserves
	- maximize the energy reserves of the weakest nodes
	- meet throughput and end-to-end delay
- techniques
	- DVS
	- DMS(dynamic modulation scaling)
		- power is also a convex functions of modulation levels
		- radio is the major source of power consumption
		- DMS adjusts radio modulation to save energy

##### Basic Task Model
- a certain set of activities must occur by the end of each frame
	- workloads can be bounded worst-case or probabilistically
	- communication workload: M (bits)
	- computational workload: c (CPU cycles)
	
- problem breakdown
	- objective: maximize the minimum energy level over any node in the network
	- &Tau_i;:energy level at the node

##### End-to-end Model
- epoch-based control
- two types of LLN mode

##### Performance Evaluation
- routine versus emergency response in a water distribution system
	- compare three energy management schemes
		- CHASS: centralized solution
		- DHASS: distributed solution
		- NPM: No-power-management
	- work modes: normal v.s. emergency
	- three emergency types
		- random attack
		- area instant attack
		- spreading attack
		

### AD HOC Systems
##### AD HOC Overview
- rapidly deployed multi-room intrusion detection
	- required indoor, GPS-less relative localization to be incorporated into the routing and reporting protocol
- road monitoring system
	- required large linear self-healing network, persistent unattended operation

##### Basic AD HOC Issues
- implementing an IP protocol stack is a really good idea
- unattended sensing and processing for meaningful result is hard in an IOT node
- Geo-location is critical
- minimizing overhead is good 
- routers and sinks are mobile
- disruption-tolerant is a good idea

 
##### What if you eliminated most network management
- suppose you only require time synchronization
- each node generates its unique transmission schedule based on a symbol's pattern in a common **latin square** shared by different communication nodes

##### Mobile Ad-HOC IOT Systems
- robotic-LLN cooperation
- unattended autonomous vehicles
	- security applications
	- land management
	- ...

### Future Work
- energy management, real-time performance mobility support, geo-location all significant open issues
- security is difficult
	

### Question
- in the emergency mode
	- need to transfer more datas, i.e., the workloads increase
	- there has some central control


