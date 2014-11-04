## Heterogeneous Architectures in 3D for Next Generation Big Data Server Platform

- Speaker: Houman Homayoun, George Mason University 

### Power Concern
- power consumption
	- short-lived batteries
- power cost in US
	- 2006, $9 billion
	- 2012, 18 billion
- temperature trend
	- energy=heat
	- heat dissipation is costly
	- increasing power dissipation in computer systems
		- even increasing cooling costs
- reliability trend: reliability crisis
	- decrease lifetime reliability	
		- high power densities: high temperature
- efficiency crisis
	- Moore's law allow double transistor budget every 18 months
	- the power and thermal budget have not changed significantly
	- efficiency problem in new generation of microprocessor
	
### Where does green computing fit in
- Objective
	- achieve sustainable computing
	- understand levels of design abstraction
	- understand where power...

### Why heterogeneity
- Current design: homogeneous
	- existing general purpose design user only homogeneous cores
	- a general purpose one-size-fit-all core is not necessarily the most efficient
	- one processor optimized for each application
- Advantage of heterogeneous
	- can adapt to program with different resources needs
	- can adapt to program phases with different resource needs
	- can adapt to different operating conditions
		- thermal emergency
	- a small core uses far less power than a big core with pieces clock-gated or even power-gated
- Current heterogeneous design	
	- State of the art commercial heterogeneous architecture
		- shortage: static and not dynamic heterogeneous architecture 
	- Limit of static heterogeneity
		- limited number of distinct core designs
		- cannot adapt to all possible execution resource needs
		- must migrate between cores to adapt to program changes
		
### Big Data Benchmarking
- Big Data Cloud Computing
	- cloud is a platform to cost effectively deploy and increasingly wide variety of application
	- vast amount of data stored in a few places
- Big Data
	- volume: big data is inherently large in volume
	- velocity
	- variety
	- veracity: tendency for errors, redundancy
- Cloud Server Computing Infrastructure
	- A web server architecture includes front-end web servers and back-end DB servers
	- A load balancer routes traffic requests in to individual requests and decides which web servers receive those requests/
	- homogeneous machines
- Big data application benchmarking and characterization
	- optimize application
- Challenges in creating a benchmark
	- diversity of application
	- security
	- size and complexity of application
	- speed at which data are created, processed, stored
- Characterization
	- Performance/Watts of Spec, Parsec, Scale-out and  Big Data application
- Observation
	- big data application run on the cloud does not have good efficiency
		- it indicates more optimization is required
	- depends on the data in the application
	- depends on the type of application
	- it indicates we need heterogeneity
	- data size has a non-trivial impact on micro-architecture parameters
	
### Enabling Dynamic Heterogeneity with Resource  polling
- Application resource utilization
	- different applications could share resources
	- resource can dynamic shrink or grow up to adapt to the demand
- Why not sharing in 2D
	- access to the neighbour core may need detour, it indicates to long delay
	- thus they propose a 3D solution
- 3D integration
	- Pros
		- don't need to change the fundamental designing		
		
### My comments
- the part of power concern is useful 
- the idea of heterogeneous design may be helpful
	- can we extend to design algorithms in terms of heterogeneous workloads  