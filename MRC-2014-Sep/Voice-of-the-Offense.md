Voice of the Ofference(VO)
---

- by *Aaron Temin*, MITRE Corporation


### Goal
- quatitatvely measure resillience
	- the risk considers all impacts from all possible cyber attack efects against each cyber resource
- using this toll, this can be use to "right" CRT's given the systems mission context

### BackGround
- There are many definitions for resillience out there
	- dictionary, NIST, ISO, National research Council etc.
- Resillience ins the inverse of Mission risk
	- numerous factors equate resillience with aspects of mission risk, where mission risk is P(bad-thing)*value of loss
	- this has implications for making statements about resillience
		- this is alright to provide a performance based resilliency score that resports the performance of the system given specified disruptions
- There are many ways to group and categorize cyber attacks
	- CVE has over 43, 000 entries
	- Common Attack Patterns(CAPEC) has over 450 entries


### Idea
- To avoid having to think about every attack instance, we consider the attack effects
	- most people consider confidentiality, integrity and availability
	- they found that this has insufficient, and instead they choose DIMFUI
		- Degradation: an attack causes a degradation in the fperformance
		- Integration
		- Modification
		- ...
- ways cyber resillience techniques(CRTs) combat cyber effects
	- since we equate mission resillience with risk..
- different CRT's are more suited to combating different cyver attack effects
- but CRTs often apply only to specific system levels

### Mission Modeling: cyber mision impact assessment(CIMIA)
- mission levels modeling using simulation of a process model
- network diagram
- ICT process model
- [Paper: computing the impact of cyver attack of complex missions](http://ieeexplore.ieee.org/xpl/login.jsp?tp=&arnumber=5929055&url=http%3A%2F%2Fieeexplore.ieee.org%2Fxpls%2Fabs_all.jsp%3Farnumber%3D5929055)
- Custom Software allows the mission impact of cyber incidents to be esimated
- Personal recovery mission overview using combat survival Evader locator(CSEL)

### Top Level View of Process Model of PR Mission
- process model descrption captures
	- actively flows, control flows, data flows
	- which mission resource platform 
- PR locate
- Combat survival Evader locator

### Integration
- MISS can move the server if DMSS detects an unauthorized access attempt
 
### Question
- how to evaluate
- with the esimation, then how to make the protect more efficient, game theory may could be applied
- is there some uncertainty associate with this model?