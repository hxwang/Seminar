Bridging the Security Gap with Decentralized Information Flow Control
---

- by *David Mazieres*, Stanforad University
- [Reference](http://www.amitlevy.com/papers/hails-crash2012.pdf)


### Goal
- make it able for programmers for secure programming

### Hails Framework
- web platform framework in Haskell
	- introduces model-Policy-view-controller paradigm
- idea
	- associate policy with data
	- need to rethink client-side security
- Fact
	- losts of functinalities is client-side
	

### Browser Security Architecture
- same-origin policy
	- disallow reads from cross-origin servers
	- restrict IPC msgs to cross-origin context

- CSP: disallow write
- CORS: permit read
- Example app: mint.com
	- read-only personal finantial data
- where the status-quo falls short
	- cannot alow network acess and ensure security
	- want: only reject when it looks at the pwd

### COWL browser
- idea: allow developers to impose restrictions on the data 
- 3 new browner primitive
	- label threads:
	- label communication:
	- priviledges
- label context: context + label
	- label: use to specify sensitive data, e.g. label("chase.com")...
	- default label: inherit from parents
- label-communication
	- associate labels with message
	- targets get "tainted" when they receive the message
- priviledge
	- ues priviledge to express trust
- improving the status quo
	- use labels to confine it...

### Implementation
- DOM-level API for firefox and chrome
- extension for inspecting labels, setting CORS...
- Hails + COWL: making end-to-end information flow control accessible to the average programmer