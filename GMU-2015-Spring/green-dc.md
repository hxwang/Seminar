## Greening Data Centers: Past, Present and Future

- Speaker: Ricardo Bianchini
- Date: 03/27/2015

###　Main characteristic of a DC
- what is dc
  - IT equipment, power delivery, and backup
- how large are they?
  - machine rooms in commercial buildings
- what workloads
  - high-performance computing and data analytics (batch)
  - online services (interactive)
  - virtual machine

### Overview
- microsoft dc in Quicy, WA
- google DC in mayes county
- high-level view

### Energy Consumption
- aggregate DC energy consumption
  - *small and medium dta centers currently dominate* 
  - data center consumes 2% of worldwide electricity consumption
  - in 2005-2010, the consumption is not double mainly due to reception, and virtualization
- thus need renewable energy in a DC
- PUE
  - PUE = total power/IT power
  - enterprise data center PUES are not improving much over time
  - for comparison, microsoft's new data centers have an average PUE of 1.125
- where does power go in a DC
  - power delivery
  - cooling
  - IT equipment
- IT power in 2007 for google DC
  - cpu: 33%
  - dram: 30%
  - networking: 5%
  - misc: 22%
- IT power in 2012 for google DC
  - cpu: 42%
  - dram: 12%
  - networking: 5%
  - misc: 27%
- what we can see
  - as technology involves, the key tarets for optimization may change. the CPU dominate right now.
- where does the money go
  - server: 63%
  - networking equipment: 6%
  - power distribution and cooling; 17%
  - other infrastructure: 4%
  - energy: 10%
- Thus we can see that energy is significant expense (180$) but pruchasing servers dominate.
  - fewer servers reduce energy cost

### Past and present techniques for greening DC
- Conventional DC cooling: cold/hot aisles
  - temperatre of the cold aisle at 20c or below
  - significant potential for hot air recirculation
  - the cooling infrastructure consumes a lot of energy
- Three key advances in cooling
  - higher cold aisle tempretures
  - hot aisle containment to prevent recirculation
  - "free" cooling: user outside air in certain climates
- Result: larger DC operatures now achieve yearly PUEs 1.0-1.20
- free cooling; no water loop, no chiller

### Servers
- Leveraging lower power states
  - turning devices off: idle low-power states
  - slowing devices down: active low-power states
- Main concerns
  - transition overheads in terms of performance and energy
  - performance at the lower speed
- Academia and industry have proposed many states
  - CPU active low-power modes (DVFS) or ACPI "P-states"
  - CPU idle low-power states (gating) or ACPI
  - system idle low-power states or ACPI "s-states"
- Improving power proportional to its utilization
  - proportionality has improved markedly due to CPUs servers now consume much less in the 10-50% range
  - the lower power states help improve proportionality

### One future direction
- reduce tail latency via parallelism
- dc/grid interaction, demand response
  - in peak time, the utility operator will urge the dc to consume less energy. 
  - cotech?
- energy coursing, including renewables
  - renewable are not constant, defer load, scale execution
- approximate computing
  - produce a lot of data, the computation does not need to be precise
  - knowing the rough ranking is enough, thus this can save energy
  - can speed up 
- accelerators: GPUs, FPGAs, etc
- reducing high-percentile("tail") latencies of servicesh

### Reducing tail lantency
- it determines the machines you need
  - if you can use fewer servers to achieve the same performance, then you can save energy
- 99% percentile latency
  - improvement on latency of 20% percent, reduce server numbers by half
- reducing tail latency by parallelism
  - can use intra-request parallelism: reduce latency, but may overload the system
  - design few-to-many parallelism
    - parallel the long request more severesly
    - add parallism at fixed interval, but no fixed period is available
      - short period is good at low load
      - long period is good at high load
  - My idea: consider together with the SIGCOMM paper which start with full parallelism and them shrink
    - we can start from a mid point
  - comparison
    - SEQ: all request use 1 thread
    - fix-2:
    - FM: 
  - assume idle consumption is: 25%
    - fm stop parallelsim when the effects will not be improved
    - the number is preprofiles, it is 4, only 4 threads???
  
### Conclusion
- data center consumes massive amount of energy
- reducing tail latency via parallelism 
