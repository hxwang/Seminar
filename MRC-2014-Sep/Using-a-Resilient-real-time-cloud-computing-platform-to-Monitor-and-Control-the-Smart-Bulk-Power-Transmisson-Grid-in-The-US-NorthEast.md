Using a resilient real-time cloud computing platform to monitor and control the smart bulk power transmission grid in the US northeast 
---

- by *Ken Birman*, Cornell University

### Demand
- a new security model supporting local control

### Challenge
- Real-time data capture

### Platform for GridCloud
- GridCloud file system: a file system for secure, strongly consistent real-time monitored data sharing
	- a real-time sanpshot capability 
- GridCloud Collaboration tool: a tool for creating a kind of sharable virtual iPad
- Main Components--Sprinkler, reliable geodistributed publish 
- Main Components--IronStack, a software defined network manager
	- run normal TCP/IP and UDP protocol on it 
	- guarantee secure, real-time fault tolerance
	- only allow data flow for security reason
	- encrypt data, sends it redundantly for robustness
- Main Component--DMake
	- based on the popular Unix "makefile" concept
	- but generalized to support distributed programs where their operating parameters can be modified at runtime
	- it handles systen repair for failure

### Key Future Challenge
- Habit of working on stable data versus a new world of continuously updated data


