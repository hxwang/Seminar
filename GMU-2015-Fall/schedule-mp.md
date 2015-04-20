## Design and modeling of Scheduler of Multi-task jobs on computer clusters

- Date: 4/20/2015

### Intro
- Massive amount of data is being generated
- Commercial adoption of big data processing
- MapReduce paradigm for processingbig data has seen impressive adoption in the IT industry.

### Challenge
- lack of robust aseessment and validation of cluster job schedulers
- lack of accurate prediction of job completion time

### System Arch
- hadoop head node
  - namenode
- hadoop compute node
  - datanode
  - tasktracker

### Problem Statement
- current modeling teechniques, whichdo not consider node contention for resources, do not allow one to perform effective scheduling of mult-task jobs running on large computer clusters

### Thesis Statement
- Is it possible to design and implement a dynamic cluster scheduler that
  - perform modeling and prediction
- Contribution
  - mapreduce jobsmodeling based on queueing network
  - model multi-core machines based on memoery contention
  - algorithm for calculating execution times for jobs streams based on finite time interval analysis
  
## Related work
- on map-reduce job modeling
- on multi-core CPU performance
- on deterministic execution simulation

### Analytic Models for Single Mapreduce
- queuing model
- m map task, c is concurrency, 
- jvm takes sometime to start, shutdown

### Modeling of multi-core machines
- share memory
  - with memory access, it is like linear, it means some cores are wastered
  - some tasks are waiting to access memory
- two models
  - application-level model
    - load independent queueing device multi core CPU
    - load independent queuing device disk
  - memory-contention model
    - delay device-core
    - load independent queueing device memory
    - load independent queuing device disk
- measuring memory access time
  - user linux tool "perf" to obtain the PMU values
  - concentrateed on "back end stakk percentage"
