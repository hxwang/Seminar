Defending Mobile Apps Through Automated Software Diversity
---

- *Michael Franz*, UCI

### Intro
- Booby trapping and link table randomization as a defense against Blind ROP
- ROP is still dangerous

### ROP attack
- verify that gadgets are each preceded by a call instruction
	- but there are sufficient many gadgets available to adversary that meet this constraint
- do not allow long sequence of short gadgets
	- ROPecker heuristic, gadgets sequence of <20 instruction. 
	- but the attack can defeat any such mechanisms

### Attackers keep innovating
- blind ROP attack previewed right here
	- can be conducted remotely or locally
	
### Defending Against Blind ROP
- an attack requires multiple gadgets: defensive objective is satisfied if the attack gadgets just a single booby trap
		
### Side Channel Attack
- side-channel attacks attempt to extract information such as cryptographic keys by observing properties of a shared system executing in virtual...
- cached-based attack
	- 
- cache-based SC attack on AES
	- by observing the cache, we can inter which elements of the table were accessed, which leaks information about the encryption keys
	- e.g., how long does it take to load my data
	- thus we could assemble the information by performing the same computation
- Solution: dynamic control flow diversity
	- switch to different version of the program 
		- e.g. d-0 program could have diversity version d-01, d-02, d-03, thus the adversary may not be able to use the access time information of d-01
	- side channel mitigation strategies
		- confuse the attacker
	- every time you have a branch, you randomly just to one, or you can modify the synchronization
	
- Technical challenge: performance
- Solution 2: cache noise insertion
	- insert random loads into the program to disrupt cache channels
		- needs to be a valid address
	- problem: not cheap

### Future work--Deployment
- diversified firefox for windows using LLVM
- self-randomized binaries

### Summary
- Booby trapping discourages brute force attacks 
	- is effective against Blind ROP attack
- Dynamic Control flow diversity is effective against side-channel attack

### Question
- 
		