# Deployment Methods

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