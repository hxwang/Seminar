Policy Weaving for System Security
---

- by *Tom Reps*, University of Wisconsin at Madison

### Intro
- how to write a program interact with a unsecure environment while providing some security guarantees

### Challenge
- Sementic Gap
	- express elements of policy directly in the code
	- express policy as a seperate ...

### JAM
- input: untrusted program, security policy
- JAM: security analysis and rewrite
- JAMScript: transaction enhanced JavaScript
	- policy relevant statement are rewritten to run within transaction blocks
	- introspect function invold at closing brace
		- examine the sequences of actions that occured
- JAMScript: dynamic code mitigation
	- addiitonal rewrting enables policy enforcementover dynamic generated code
- Protecting the instrumentation
	
### Policy Weavers
- create policy weaver via a policy weaver generator
- weaving via game-solving
	- given program and policy	
		- construct a finite game G that models the possible ways 
		- then game playing
- Game construction challenges
	- need an operational semantics that faithfully models the semantics of the security system
		- solution: model as relations 
	- need a method to extract a suitable game from a program and a policy that distinguishes runs that satisfy the requirement


### AppWeave
- Motivation
	- statically rewrite Android App to obey the security policy
- Limitation of android permission model
	- all or nothing permissions
- Approach
	- forma single monilitihic app to a set of collaborating app
	- app spliting flow
	
### Reasoning about Security Policy
- CounterSat: a solver for countng problems
- application programers reasoning at a high level about a plicy and automatically obtains a secure program
- opportunities for static analysis and optimization
- Parameterized by language and enforment mechanism