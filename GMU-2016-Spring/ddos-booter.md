## DDoS Booter

- PHD Defense by Mohammad Karami

### Booter Service

- Use the interface 
- Techniques
  - Direct attacks
    - TCP SYN, UDP flood etc
  - Reflexive Attacks
    - DNS, NTP, SSDP ...
    
### Amplification Attacks
- Booter's preferred attack technique
- Most frequently abused protocol for amplification
  - NTP: 603
  - DNS: 30x
  - SSDP: 26x
  

### Payment
- botcoin
- ebay
  - Collaborated with Paypal to limit access of booters

### Attribution of Booter Amplification Attacks
- Jaccard index to measuring the similarity of attack instances
  - use a similarity threshold value to account for unknown attack instances (how to decide the threshold?)
- "leave one out" cross validation (discuss with Xi)

### Evasion Attempts
- Randomizing the set of abused amplification per attack
- Masquerading as a different booter service

### EDoS
- Motivation
  - Target public cloud consumers
  - The goal is to increase the cost for a victim
  - Do not cause service distruption
  - Carrided out using botnets
  - Need to run over an extended period of time
- Defense
  - Cryptographic puzzles
  - CAPTCHA
  - Anomaly detection based on request metrics
    - number fo session, number of requests, etc. (Discuss with Xi)
- Anomaly detection
  - assign relative cost value to user request
  - use the sequence of request costs of benign users to learn the resoruce consumption behavior of normal users
    - hidden semi markov model (HsMM)
  - detect malicious users participating in EDoS attacks
  - Questions? How to verify there is a trend for nomarl users? (Use CS GMU data)
  
### Experiment
- Attack strategies
  - Attack parameters
    - Attack rate
    - Requested resources
  - Focused on high cost requests
    - Request rate: normally distributed
  - Focus on high number of requests
  - Experiments based on the same number of normal and malicious sequences






  


