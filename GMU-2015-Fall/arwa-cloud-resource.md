## Automatic, Optimal, and Near-Optimal Resource Allocation in Cloud Computing

- Arwa Aldhalaan
- Date: 04/23/2015

### Background
- SaaS
  - pay as they use
- IaaS

### Intro
- Cloud computing is based on large distributed system
- resource management in cloud is very challengeing

### Problem Statement
- management their resource in dynamic environments
- how to process customer's requirements by allocation machines
- number and types of machines to run services
- challenge
  - dynamic
- automaic, optimization techniques to meet QoS reqirements

### Arch
- users make request to SaaS
- SaaS require IaaS
- IaaS requires migraiton

### Live virtual machine migration
- pages of the address of the virtual machine is copied when the VM is running
- dyanmic migrate the dirty pages
- advantage: very low downtime
- optimal value of alpha
  - non-linear optimizer decides alpha
  - tradeoff between alpha and network utilization
  - alpha is high, then long downtime, low network utilization
- heuristic solution to this problem

### Problem Description
- The cloud provider has to make an optimal decision where to send the request
- constraints
  - SLA constraints: weighted average of ...
- Heuristic search
  - hill-climbing, determine neighborhood
  - reuse virtual machine that is already in the cloud
- Better revenue than Best-fit strategy

### Cloud
- two virtual machine in the same physical machine
  - take into account of commmunication costs
  - communication strength 
- problem statement: 
- consumers make request of a group of virtual mahines
- dynamic find the allocation of virutla machines to maxmize the cloud provider revenue


  

