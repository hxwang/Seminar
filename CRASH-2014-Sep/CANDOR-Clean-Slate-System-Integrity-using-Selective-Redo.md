CANDOR: Clean-slate System Integrity using Selective Redo
---

- by *Nickolai Zeldovich*, MIT

### Challenge
- difficult to write secure system in C

### Overview
- Better Defensive infrastructure
	LXFI(SOSP'11): fine grained software fault isolation in linux
- Bug-finding
	- KINT(OSDI'12), STACK(SOSP'13): static analysis tool for finding integer overflow
- Formal verification
	- Jitk(OSDI'14): formally verfied linux seccomp security mechanism

- Encrypt computation
	- VersSum(CCS'14): efficiently verfying outsourced computations
	- Ascend: using trusted hardware to encrypt data

### Ascend Processor: Privacy in the cloud
- Structure
	- entrypt the data, send to cloud
	- get encrypted result back
- Challenge
	- the processor in the cloud could be malicious
	- potential leak of data
- Goal
	- minimize the data leakage


### Stawman Solutions
- trust the server
	- current model, fast computation, huge TCB(whole server)
- Fully homomorphic encryption
	- computation on encrypted data
	- virtually no TCB

### Structure
- 1. user share key with the chip
- 2. use send .. to server to request data
- 3. the server provide program and data to chip
- ...

### Obfuscating Memory
- any two sequence of memory access should be indigtinguishable
- minimize changes to eixsting architecture


### Oblivious RAM
- Cryptographic protocol to hide memory access pattern

### Path ORAM
- for os
- lay out memory in binary tree
- a mapping for the program's logical address to the leaf
- if a block is mapped to a path, it must be on that path 

### Recursive Path ORAM
- the Path ORAM is not efficient, position map is too large to map the chip
- thus we can use a table, recursively store position map
	- similar to page table
- after 4-5 levels of recursion, PopMap dominates overhead
	- use position lookaside buffer
- implementation: use verilog

### ORAM in Ascend
- very storng security gurantees
- significant overheads

### Malicious Server
- it could modify data etc, thus we need to add integrity
- solution
	- Option 1: Merkle Tree, but expensive, because hash chaining proportional to tree height, need to verified everything on the path
	- we can use acecss counter instead of leaf label

	
