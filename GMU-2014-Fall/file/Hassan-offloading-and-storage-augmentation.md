## Computation Offloading and Storage Augmentation

- Speaker: Mohammed Anowarul Hassan
- Location: Engineering 4801
- Date: 11/12/2014

### Abstract
- The increasing popularity of mobile devices calls for effective execution of mobile applications. Due to the relatively slower CPU speed and smaller memory size, plenty of research has been conducted on properly splitting and offloading computing intensive tasks in mobile applications to external resources (e.g., public clouds). Prior research on mobile computation offloading has mainly focused on how to offload. Moreover, existing solutions require the application developers to specify the computation intensive segment of the applications beforehand. In addition, these solutions do not work transparently with existing applications. In this dissertation, we aim to design and implement a mobile application offloading framework by addressing these issues. For this purpose, we first design and implement a transparent offloading mechanism called FaST: a Framework for Smart and Transparent mobile computation offloading, to allow mobile applications to automatically offload resource-intensive methods to more powerful computing resources without requiring any special compilation or modification to the applications' source code or binary. We also find the key features that can dynamically impact the response time and the energy consumption of the offloaded methods and thus design Lamp, a runtime Learning model for application profiler, based on which we profile the local on-device and the remote on-server executions of the applications. To address the problem of what to offload, we design and implement an application partitioner, called Elicit, to Efficiently identify computation-intensive tasks in mobile applications for offloading in a dynamically changing environment by estimating the applications' on-device and on-server performance with Lamp.
- In addition to the offloading demand for mobile applications, the increasing popularity of mobile devices has also caused the demand surge of pervasive and quick accessing files across different personal devices owned by a user. Most existing solutions, such as DropBox and SkyDrive, rely on centralized infrastructure (e.g., cloud storage) to synchronize files across different devices. Therefore, these solutions come with potential risks of user privacy and data secrecy. In addition, the consistency, synchronization, and data location policies of these solutions are not suitable for resource-constrained mobile devices. Furthermore, these solutions are not transparent to the mobile applications. Therefore, in this dissertation, we design and implement a system Virtually Unify Personal Storage (vUPS) for fast and pervasive accesses of personal data across different devices.


### Intro
- More and more resource-intensive application for mobile phone
- How to address the insufficient computation power and storage in mobile phone

### How to offload: FaST
- Related work
	- Task partitioning
		- Drawback: 
	- VM based cloning
		- Drawback: need to synchronize, create a lot of overhead
			- e.g., large image
- Framework: Fast
	- transparent to application
	- no full cloning
	- conclusion: sometimes offloading may be worse than on device
	

### Whether to offload:LAMP
- Related work
	- offloading when thread execution time >= 2*RTT
		- drawback: 
	- threshold-based: data size > 6MB
		- drawback: may not work
	- Linear regression model of onDevice and onServer execution time
		- pros: consider bandwidth
		- drawback: too simplified, may predict wrong value
- onServerTime = transfer time + computation time
- Framework: LAMP
	- consider many factors
	- pros
		- monitor system environmental
		- predict: compute onDevice and onServer execution time 
		- make decision 
	- prediction
		- linear regression, svm, decision tree, multi-layer perceptron
	- comparison
		- with ondevice, onserver, optimal, lamp
	- summary: 
	- Question: how the methods can be identified for offloading

### What to offload: Elicit
- Related work
	- simple decision making: so far running time >2*RTT
		- drawback: no profiling to find intensive parts
	- threshold-based: 6MB
		- drawback: does not provide guideline of how to find the constraints
		- pros: reflected the dynamic nature of the environment in a simplified way
	- android partitioning	
		- method: offloading decision based on LOC
		- partition in 
- Framework: Elicit
	- Method
		- build call graph
		- keep track when a method is invoked and returns to the caller, for purpose of profiling
	- Model
		- each node represents a method
		- each edge represents the invocation cost
		- thus
			- e.g., if some nodes are accessing camera, it cannot be offload to server. We can find the constraints of other nodes as well
	- Solution
		- max-flow min-cut
		- choose the method which have flow less than capacity
		- time complexity: O(vE^2)
	- Evaluation
		- on top of Fast, Lamp


### Storage Augmentation
- commercial solution
- people own multiple device
- enough storage by passing cloud 
- Framework: vUPS
	- bypassing the cloud
	- no central point of entry

### Conclusion
- mobile device popular
- constrained by limited computation and storage

### Future work
- provide service side computation service in android VM

### Question
- computation time is proportional to energy consumption
	- But not always
- any related work do the offloading under budget constraints
	
### Comment
- offload when > 2*RTT
	- 