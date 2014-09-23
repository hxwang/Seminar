Cloud Intrusion Detection and Repair
---

by *Stelios Sidiroglou-Doukos, MIT*

### Goal
- distributed anomaly detection and repair

### Diode
- input
	- dynamic execution engine until a critical point
	- then convert to bitvector
	- CWebP Vulnerability
		- WebP: source code, decode
	- LIBJPEG: full logic is left to client code

### Repair
- how do you find the protection code?
- how can you translate it back to host code


### pDNA
- variable discovery: find "="
- Patch generation
	- multiple possible patch insertion points
	- group variable expression
- Patch rewrite
- Patch validate
	- execute the patch version on error-triggering input
	- run regression tests?
	- integer overflows, verify that added patch cannot generate overflow condition
- other types of bugs?

### Discussion
- Why does this work
	- N-Version programming for free
		- multiple implementation of common specification
	

	
### Question
- regression tests?
- how to ensure the rewrite doesn't change its original function?
- test for software