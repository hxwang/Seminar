Modular Research-based Composably trustworthy Mission-oriented Resilient Clouds(MRC2)
---

- by Simon Moore, Cambridge University
- [Project Website](http://www.cl.cam.ac.uk/research/comparch/research/mrc2.html)

### SDN Security
- Challenge
	- consistent and enforceable SDN security policies
	- New threats to infiltrate
- Rosemary: Security in a network-OS(NOS)
- Policy Synchronization
	- ONOS...

### Trustworthy DSN Switches
- Trustworthy platform for switch control
	- Formal grounding for configuration consistency and hardware/software interaction
	- CHERI capability-based security...
- Blueswitch
	- Compliant with OpenFlow switch protocol
	- Parameterized design configuration
	- Transactions...
- Challenge: Blueswitch + CHERI on NetFPGA

### Resilient High-dimensional Datacenter switching
- Approach: high-dimensional structure with a switcher for every compute node
- R2D2: Resilient Realtime Data Deliverys
	- Problem: insufficient network isolation among datacenter applications
	- Solution: R2D2 implements prioritized distribution admission control on unmodified, commodity, hardware

### SELENA: faithful SDN experiments
- Xen-based framework supporting all VM-types
- Fidelity: real-scale experiments

### Dual-core CHERI: freeBSD on FPGA
- inter-thread memory sharing
- Cache coherency comparison
	- L3 formal model simulates faster than Bluespec
- Formal dual-core model
	- The L3 model
		- enables trace comparison with Bluesim simulations
		- enables rapid design cycle to track down software bugs
	
### Direction
- can multithreading be used to do more efficient capability domain crossing?
- how does memory consistency impact security of capabilities?
- integrate verified CPU with verified switch	
	
### MirageOS
- MirageOS is a libarry OS built in OCaml
	- OCaml has been ported to CHERI
- Irmin distributed storage





	