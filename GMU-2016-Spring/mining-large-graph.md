## Mining Large Graph: Patterns, Anomalies and Fraud Detection

- Christos

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
    
