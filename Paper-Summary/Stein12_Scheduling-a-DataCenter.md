Scheduling a Large DataCenter
----

- [Paper Link](http://www.nii.ac.jp/shonan/seminar011/files/2012/02/stein.pdf)
- by [Cliff Stein](http://www.columbia.edu/~cs2035/)
- version 1.0 (last updated 09/10/2014)

### Strongness
The model they considered are more complete than the one we have.

1. They considered a data center consisting of several machines, each machine has CPU resources.
2. Users submit jobs to data center. Each job consists of several tasks. The algorithms  are evaluated on the total # of tasks completed, rather than total # of jobs. Mapped to our models, profits can be obtained proportional to the part of job completed.
3. 11 algorithms are simulated to compare the throughput.

### Weakness
1. However, the talk didn't give the evaluation on the energy cost. The intuition is to minimize the fragmentation, and to maximize the # of machines unused.  However, 
there is no simulation result on the energy cost. And the designed algorithms such as "SOS" is not based on the goal of minimize the fragmentation.

### Extension
1. For future work, we may consider energy cost in this model. Or they may have done that.