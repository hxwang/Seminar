## Visual Scene Understanding through Semantic Segmentation

- info: 10/09/2014
- speaker: Gautam Singh (Ph.D. Defense)

### Intro
- process of extracting semantic information from an image
- Semantic Image Retrieval: semantic label descriptor extract the information 
- Labeling
	- label scenes
	- object detection
	
### Background
- Image site features
	- location
	- color
	- texture: orientation information
	- perspective cues
- Data Item
	- discriminative classifiers, e.g., SVM, boosting 
	- data driven non-parametric approach
		- knn over highdimensional features, poor accuracy for less frequent things 

### Main work	
- Non-parametric SS(Semantic segmentation)
	- compute watershed superpixels
	- use different ranking approach
	- weighted knn 
	- get initial labeling, then use semantic context, refine the labeling
- Introspective SS
	- confidence ranking
- application of SS

### Main results
- improve of accuracy in per class: use semantic context

### Model 
- solution
	- bayes
	- rewrite maximization as energy minimization

### Dataset used
- SiftFlow Dataset
	- 2688 images
- Standford
	- 717 images
	 
### Evaluation
- evaluate the accuracy by the following two category respectively
	- per pixel
	- per class
	
### Labeling uncertainty
- Example: the learning scenes have only outdoor scene, how can you use it to label indoor scene?
- Main idea: : associate probability
	- entropy over label likelihood		
	- ...		
- Strangeness Measure
	- quantify classifier performance through estimate of uncertainty of the ...
	- ratio of distance in own class/ distance from other class
- p-value
	- the lower the p value, the better the category is a good fit for the instance	
- labeling uncertainty	
	- precompute strangeness and p-value for all instances in the source dataset
- Comparison: compare with boosting, WKNN
- Confidence ranking of dataset
	- compute uncertainty using strangeness
	- use weighted aggregate for image uncertainty score	
	
### Future work
- strangeness based uncertainty for active learning and discovering new categories
- joint learning of methods for different scenes
- utilize 3-d structure of the scene to improve semantic segmentation
	