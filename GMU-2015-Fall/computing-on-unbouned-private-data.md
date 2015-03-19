## Computing on unbounded private data

- Date: 3/19/2015
- Speaker:

### Intro
- Benefits for cloud data, and the privacy concern
  - Cloud: losing privacy
  - Medical data: for research, to drug discovery, disease control
  - Social networking data:
  - Financial data
- Untrusted cloud
  - insider attack
  - software bugs
  
### Work
- achieved benefit, while protect privacy via encryption scheme
- maximum privacy: cloud learn nothing except the output
- Example
  - IRS-> data -> user

### Mechanism
- Is it possible to decrypt that only reveal f(X)
  - Embeded function "in the key"
  - Functional encryption scheme

### Power of general computation
- If want to hide ouput from the cloud, then encrypt the result

### Syntax
- Step up: master secret key, public key
- Encrypt
- KeyGen: takes an input of program M -> give a new secret key

### Technic
- Goal: ensure that cloud learn nothing no more than M(x)
- Approach
  - blue box: cloud can not tell whether it is blue cloud for x or y
  - random sampling
    - bootstraping
  - two key idea
    - have two public keys
    - encrypt twice
    - proved correctness
    

