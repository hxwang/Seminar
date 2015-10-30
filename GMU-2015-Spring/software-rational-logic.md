## Practical, Automatic Analysis of Mobile Software using Rational Analysis

- Speaker: Hamid Bagheri
- Date: 4/22/2015

### Summary
- Build dependable software
- Formal verification techniques
  - exploring state space
  - heavy-weight, all cases
  - require human assistance
  - not designed for software modeling
- Alloy: lightweight formal method
  - automated analysis based on SAT solving
    - simulation
    - checking assertions
  - used in certain domains
    - sanity checking 
    

### Compositional analysis of android inter-app vulnerabilities
- app markets are good malware dilivery system
  - amoung which android is the primary target
- android provide a very flexible communication model
  - components: basic building blocks of android apps
  - intents: android event messages
- anroid permission model
  - install time permission request
  - internet, acount, phone call, gps, storage
- inadequare permission model
  - enforcement of permission at the granularity of individual apps
  - not sufficient
- inter-app vulnerability example
  - priviledge escalation
  - conclude permissions
  - serveral decomposition security issue
- naive approach
  - combined apps
  - program analysis: scalability issues
- convert approach: composition analysis
  - program analysis
  - formal analyzer

### Program analysis
- four step approach to extract information for each app
  - extract the principal entities and permissions for the manifest file
  - identify intents and intent filters that are latent application bytecode
  - determine the event-driven behavior of app
  - identify the vulnerable aths with each component
- specificaiton of apps in Alloy
  - formal analyzer
  - vulnerability instances
  - vulnerability assertion
- checking assertion using Alloy Analyzer
- Alloy analyzer finds a counerexample
- how does the accuracy of CONVERT compare to other tools
  - bench mark
    - DroidBench
    - ICC-Bench
  - compare on: true positive, false positive, false negative
  - conclusion: CONVERT has better results compared with 
- experiment with practical apps
  - 60% positive
- compare on model checking time
  - check hundreds of components in minutes
- analyze scalability: better scalability compared with ...
- CONVERT in practise
  
### Analysis of the anroid permission protocol for design flaws
- software applications increasing use application development frameworks
- frameworks impose certain protocols on the applications that are developed on top of them
- framework protocol example: custom permissions
  - defines: "AddrBookRead" permission
  - protection level: signature
  - uses the permission to protect its ...
- Challenge
  - sysematic approach for analyzing protocols
- Insights
  - formal analysis is good at analyzing network protocol, but is weak in analyzing framework protocol
- android permission model
  - basic concepts: 
- subset of android permisson model 
  - basic elements
    - device: builtiinpermission, custome permission
    - application: set permission, 
    - permission: protection level
    - signature permission
- subset of android permission model system behavior
  - invoke
  - install
  - uninstall
- nounauthorization access
- bounded exhausitive analysis using Alloy analyzer
  - concept specifications
  - operation specifictions
  - goal assertion

### analysis results
- custom permission vulnerability
  - Step 1: malapp is installed, define addrbookread permission, protection level: normal
  - Step 2: vicapp is installed, define addrbookread permission, protection level: signature, use the permission 
  - then malapp is able to access the victime
- URI permission vulnerability
- permission re-delegation vulnerability

### Experiments
- Apps
  - Goole play, F-driod
  - 62.43% use custome permission

### Conclusion and future work
- beyond vulnerability detection
  - practively generate specification of possible exploits
  - e.g., intent hijacking, ....
  - hypothesis what kind of attacking is possible
  - create security pociliers that are enforced at runtime
  - apply them as perventive measures to guard against yet unknown malicious behavior
  - allow us to detect zero-day attack
- beyond android
  - ideas can be generalized to app ecosystems
- tradeoff analysis
  - analyis of android security vulnerabilities
  - tradeoff analyis and systhesis
  
