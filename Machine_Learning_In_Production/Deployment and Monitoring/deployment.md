# Deployment

#### Key Challenges
- Concept Drift and Data Drfit
	- Data changes after system has been deployed
	- Eg : Change of lighting conditions in a Vision system
	- Data changes can be gradual or sudden
	- Data Drift : Input data changes
	- Concept drift : Depndency of input on target changes

---
- Software engineering issue
	- Ask these questions
    	- Do you need realtime or batch predictions?
        - Service runs in cloud or Edge/Browser
        - How much compute resources you have?
        - Latency and throughput(QPS - Queries per second)
        - Logging
        - Security and provacy ( Encryption of models to avoid model posioning )
---
<br><br><br>

#### Deployment patterns

Common deployment cases
- New Product/capability deployment
	- start with small amount of traffic and gradually ramp it up
- Automate/ assist with manual task
	- The fact that people were doing this earlier gives some deployment options
    - Shadow mode system : Go with human judgement, but run the algorithm in parallel. 
		- This allows to gather learning about how the model is performing
- Replace previous ML system

Key ideas
- Send a small amount of traffic tp model without passing the whole traffic through it. Rather do it with a smaller part of system and slowly ramp up
- Rollback : If the algorithm is not working ,roll back to previous state

#### Deployment Methods

- Shadow mode deployment
	-  Go with human judgement, but run the algorithm in parallel.  This allows to gather learning about how the model performs and what has to be improved

- Canary Deployment
	- Roll out to small % of traffic . Maybe 5%, remaining running in old method. Ramp up gradually when the performance is getting method

- Blue Green deployment
	- ![](bluegreen.png)
	- Enables easy rollback by switching the traffic to old or new version 

#### Degress or Automation

1. Human Only
2. Shadow mode
3. AI assistance
4. Partial Automation : Taking seconday human opinion to confirm prediction in certain cases and also use this as feedback
5. Full Automation : Learning algorithm makes all decisions

We can choose to stop at any degree based on use case or efficency of algorithm