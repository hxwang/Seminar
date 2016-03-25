## Mining Large Graph: Patterns, Anomalies and Fraud Detection

- Christos
- Date: 03/25/2016

### Motivation
- Network security
  - Connections of machines, IPs
- Account security
  - Facebook etc, connections


### Problems
- Pattern, fraud detection
- Pattern in time evolving graph
  - tensors 
    - e.g., source, destination, time

### Problems and Solution
- S1: Facebook, friend-of-friend (FOF)
  - Heterogeous number of FOF
  - It is not right to assume everything is around the min
- S2: Ax = \lambda x
  - Power law in the distribution of values
- S3: Triangle Laws
  - double friends, triple triangles
  - Triangles computation is expensive
    - # of triangles = sum(\lambda^3)/6
    - because of the skewness in S2
  - This rule can be used to detect the anomalies

### Fraud
- Given: who like what page and when
- Find: anomalies
- Intuition
  - same anomalies like the same page at the same time, considering bots
- Mapreduce overview
  - use hadoop to search many clusters in parallel
    - start: with randomly seed
    - update: set of pages, time, users
    - end: until converge
    
### Suspicious Patterns in Event Data
- # of users, # of IPs, like # of pages, time

### E-bay Fraud Detection: Blief Propogation
- Scenarios: Sellers get your money, but not send the goods
- 3 types of users
  - green: honest
  - yellow: honest in selling goods, but give good review on the red clients
  - red: dishonest
- Intuition
  - Check the interations between users
    - yellow guy never talk to each other as it is a waste of money
    

### Malicious executables
- Polonium: The data
  - 50+ million machines
  - 900+ million executables
  - construct a bi-party graph of users and executables
- Idea
  - Use belif propogation
  
### Part 2: Graphs over time -- Tensors
- Given: who calls whom and when
- Find: anomalies
- Tensor
  - It can have more settings rather than 2
  - e.g., given subject, verbs, object facts
- Tensor factorization
  - Recall: (SVD) matrix factorizaiton, find blocks
  - Tensor can do better, it can incorparate more dimensions
    - e.g., users, object, verb


### Conclusion
- Big data can help find patterns 
- Tensor is helpful in finding patterns

