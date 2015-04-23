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


