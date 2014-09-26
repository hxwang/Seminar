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
- 