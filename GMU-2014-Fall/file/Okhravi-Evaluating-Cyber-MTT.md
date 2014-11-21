## Evaluating Cyber Moving Target Technique

- Engr 4201, 11/21/2014
- Speaker: Hamed Okhravi, Technical Staff @ MIT Lincoln Laboratory

### Speaker bio
Hamed Okhravi is a member of Technical Staff at the Cyber Systems and 
Technology group of MIT Lincoln Laboratory, researching in the area of cyber 
security. Dr. Okhravi received his MS and PhD in Electrical and Computer 
Engineering  from University of Illinois at Urbana-Champaign (2006 and 2009). 
During his PhD study, he also interned at Network Geographics (2007) and  Cisco 
Systems, Inc. (2008). Currently, Dr. Okhravi is working on cyber-attack 
survivable systems at MIT. His research interests are in  cyber security, cyber 
trust, science of security, security metrics, and operating systems.

### Abstract
Cyber moving target (MT) has been identified as one of the
game-changing themes to re-balance the cyber landscape in favor of defense. MT 
techniques make cyber systems less static, less homogeneous, and less 
deterministic in order to create uncertainty for the attackers. Although many 
MT techniques have been proposed in the literature, little has been done on 
evaluating their effectiveness, benefits, and weaknesses. In this talk, we 
evaluate the wide range of MT techniques using three approaches. First, a 
qualitative assessment studies the potential benefits, gaps, and weaknesses for 
each category of MT. This step identifies major gaps in this domain which can 
guide future research and prototyping efforts. We also provide the findings of 
a qualitative assessment case study on code reuse defenses. Second, for the MT 
techniques that are identified as potentially more beneficial in the 
qualitative assessment, we perform a deeper quantitative assessment using real 
exploits. Third, we perform an assessment of how information leakage can impact 
the effectiveness of MT techniques inside a larger system. Finally, we outline 
possible directions for future work in this domain.

### Motivation
- Current
	- zero-day attack
	- allow remote code execution
	- 2.8 billion Internet users, 17% use vulnerable version of IE
- Moving target
	- add diversity
	- dynamic: reduce the lifetime of the attack

### Technique
- seeks to diversify, randomize, and dynamically change properties of a machine
	- data: change data format
	- software: change application code
	- execution environment
	- operating system

### Evaluation
- qualitative assessment
- quantitave assessment
- adversarial assessment 
	- evaluate hypothese, break assumptions
	
### Qualitative assessment
- Attack procedure
	- recon: find target
	- identify: the os running, etc.
	- deliver exploit
- Defense 1
	- dynamic changes
		- address
		- protocols
		- routers
		- traffic properties 
	- Potential benefits
		- prevent recon
		- prevent deliver exploit
	- Gaps 
		- the attackers doesn't need to know the address of the machine, e.g., polo-marco
- Defense 2
	- dynamic changes
		- operating system
		- processor architecture
		- machine instance (e.g., use virtual machine)
	- drawback
		- high-cost and overhead
		- lacks of synchronization
- Defense 3
	- change the runtime environment
		- change layout of memory
		- change processor or ...
	- goal
		- prevent develop/deliver exploit
	- gaps
		- limited coverage
		- vulnerable to information leakage 
- Defense 4
	- dynamic change of 
		- application code, instruction order, code variant
	- goal
		- prevent develop/deliver exploit
	- gaps
		- lacks compatibility
		- requires source code
- Defense 5
	- dynamic data
		- change data format, syntax
	- goal
		- prevent develop/deliver exploit
	- gaps
		- lacks of automated techniques
		- low entropy

### Quantitative Assessment
- Intro
	- platform is defined as the processor architecture, operating system, machine instance, or a combination thereof
- dynamic platform techniques
	- e.g., server rotation/ VM rotation/
	- e.g., migration-based platform diversity
	- e.g., multivariant execution
		- downward/up grow stack, compare result
- Comparison
	- Diversity
		- e.g., vm rotation doesn't change 
	- multi-instance
		- more than one platform runs at a time
	- limited duration
		- one task can run on more than one platform
	- clean-up
		- inactive platforms are wiped to a pristine state: rotation 
- important question
	- which metric is more important?
	
- Experiment 
	- set-up
		- exploits are launched at random times
		- attacker's goal is to compromise the platform for the longest possible time
			- e.g., attacker wins if the platform is compromised longer than time T
		- defenders doesn't know which platform is vulnerable
	- Result
		- when attackers have higher goal, the portion of time they succeed decreases
		- more platforms is not always better, surprising, 
			- if the duration of the platform is d, and attackers success threshold is defined as Target
				- if d < T, than attackers will have no change to win
		- deversity effect
			- if T is slightly larger than d, than 2 platforms must be compromised
			- if T is slightly larger than 2d, than 3 platforms must be compromised
	- Dilemma
		- how to we know we have capture the main results?
			- incorporate the result using markov-chains 
			- the probability between state transition
		- T/d \to 0
			- attacker wins if any platform is vulnerable
			- diversity hurts security
		- T/d \to \infty
			- attackers wins iff all platforms are vulnerable
			- diversity helps security

### Adversarial Assessment
- Intro
	- diversify or randomize code to mitigate such attacks
	- proposed to mitigate code injection/ code reuse attacks
- Technique
	- in place code replacement
- Weakness
	- secrets leakage
	- one form of leakage; memory disclosure bugs
	- remote side channel
- side-channel
	- by using buffer overflow
	- any allocated location in memory
- timing attacks via dangling data pointers
	- redirecting dangling data points to arbitrary memory locations, an attacker can estimate their byte value
		- while loop to find i< pointer.value
	- output message from the victim reveals the location of "zero" bytes
		- response message of byte[index]
- accurate timing measurement 
	- network jitter make the measurement difficult
	- thus, repeat, sample, and draw the accumulated time as a line
- Course-grained ASLR
	- only library locations are randomized
- Medium-Grained ASLR
	- function locations are randomized within a library
	- attack procedure
		- scan enough bytes to fingerprint a function
		- if it has a system call, done
		- if not, skip, go to 1
	- Note: because you have the timing, you will know how long to jump to next code for inspection
- Multi-Compiler
	- layout is diversified by random NOPs
	- attack procedure
		- ...

### potential Countermeasures
- hide timing information: constant development, etc.
- ...

### What's next
- many disjoint efforts on MT techniques, analytics, and management system
- very little on architecture that effective 

### Conclusion
- study and analyze moving target
	- qualitative
	- quantitative
	- adversarial
