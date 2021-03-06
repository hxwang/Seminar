Resilient Diffusive Clouds
---

- by *Steve Taylor*, Dartmouth College
- [website 1](http://websensing.com/)
- [website 2](http://engineering.dartmouth.edu/~d1266j2/)

### Intro
- Diversified NFS(D-NFS)

### Mitigate Vulnerability Amplification
- Cloud computing: huge number of machines using the same OS
- Diversity
	- disrupt every entry point to stop invoking implants
	- disrupt every exit point to stop returning from implants
	- discrupt every block in order to disrupt inline code patching
- Use both compile and run-time diversity
	- total compiled **entropy** is 39 bits(with 550 million vriables)

### D-NFS
- load ELF Binary over the network
- data transfer initiated through user...

### loading code over NFS
- By segment
	- Pros
	- only data that is needed by the ELF loader is being transferred
	- overlapping loading with transfer
- By file
	- Pros
		- only one read operating, little TCP overhead
		- easy implementation(<100LoC)

### iPEX booting Bear in the cloud
- TFTP shown to be insecure
- iPEX supports booting via HTTPS
- iPEX via HTTP extremly fast

###　Direction for non-deterministic Refresh
- ARM: hardware hiding, system on a chip

### Hiding Kernel Structure
- No process structures visible to code running on precesors Hand-coded HDL scheduler yields 50% speeding
- Automated C-based HDL scheduler yields 30% slowdown

### Hiding Security Monitors
- FPGA based Monitors in Bear
	- 	