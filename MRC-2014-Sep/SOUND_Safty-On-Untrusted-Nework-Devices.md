SOUND: Safety On Untrusted Network Devices
------------
- by *Jothy Roesenberg, BAE System
- [Project Website](http://sound.cis.upenn.edu/)

### Intro
- MisBehavior is not system-centric
- Use reputation to analyse how reliable somebody is to others
	e.g., if someone is downloading a lot of videos, then decrease its reputation
		
### Reputation
- provide a heuristic for deciding whether to interact with another node
- Existing algorithm:
- IBR
	- Localized reputation
	- Single type of misbehavior
	- Local policy
- SOUND reputation algorithm
	- Centralized reputation
	- Multi types of misbehavior...
- SOUND using REGRET algorithm
	- interaction, impression, reputation 
- SOUND Extended Reputation
	- Balance between solitary and community
	- Context: multiple types of misbehavior
	- Decay function configurable for each type
	- Multi-layer identity
	- Resilence.. 
- Next step
	- Yu-Singh algorithm, machine learning

### Domain-Specific Language
- Question
	- who to be considered malicious
- Challenge
	- Specifying network policies is hard
	- Complex, ...
- Existing tools are poor
	- Primitive user-driven configuration methods
	- Usually limited to static configuration 
	- Must often fall back to ad-hoc coding
- Domain-Specific Language to the Rescue
	- design a language just for policies
		- specification, generating implementation, testing, static analysis...
	- SUPPL
		- Simple Unified Policy Programming Language
		- Event-Condition-Action Policies
		- Like Prolog, but with strong type and mode disciplines
		- Precise..
- Example: Connection Service
	- System allow or deny service
	- Service table, e.g., block IP address
- Detection Conflicts: verification formula
- [Reference](http://rwd.rdockins.name/suppl/)
	
