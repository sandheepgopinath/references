# Geometric Deep Learning


- Eucledian data : Datatypes in 1D and 2D.
- Eg : Images, voice etc
![](https://miro.medium.com/max/700/1*xirhQeZlClN_EZPN4RqSgw.png)
- Non-Eucledian data : We are adding an inductive bias. This is based on the intuition that, given data of an arbitrary type, format, and size, one can prioritize the model to learn certain patterns by changing the structure of that data. In the majority of current research pursuits and literature, the inductive bias that is used is relational.
![](https://miro.medium.com/max/700/1*FQfqnaHAWpk_6oLdFfBphg.png)

- Prime example of a non-eucledian data type is a graph. It contains a nodes ( entities ) and edges ( relationships)
- Graph theory : Study of graphs 

##### Graph 
- Stuctured datatype that has nodes and edges. Nodes are also called vertices.
- Each node and vertices can have labels. 
	- Types of labels 
		- Numeric labels
			- Nodes and edges have numeric data
			![](https://miro.medium.com/max/1400/0*WulbOzkKqtYwO20W.png)
        - Textual labels
        	- Labels are texts
        	- ![](https://miro.medium.com/max/1400/0*JsA-yhG2aZgfJBf6.png)
	- Labels don't have to be unique
- Graphs can have features
 ![](https://miro.medium.com/max/1400/1*NpJshvW7HlJ_6nJ69mtHAw.png)
 
- Graphs can be directed or Undirected
![](https://miro.medium.com/max/1400/1*01whFGyfYCasLLqZAVUwYg.png)
- A node in graph can have an edge that connect to itself, called Self Loop


- An analogy by Flawson Tong

	###### A node is a person, a node's label is a person's name and the node's features are the person's charachterstics. 
        


- Graphs can be 
	- Hetrogeneous : Composed of different tyes of nodes
	- Homegeneous  : Composed of same type of nodes
	- Static : Nodes and edges do not chane, nothing is added or taken away
	- Dynamic : Nodes and Edges change, deleted, added, or moved
	- Dense : Many nodes and edges
	- Sparse : Fewerr nodes and edges


- Different Graph structures
	- Wheel
	![](https://i.stack.imgur.com/v3004.gif)
	- Cycle - Single cycle
	![](https://www.researchgate.net/publication/330373946/figure/fig5/AS:715146162872328@1547515540694/a-The-squared-cycle-graph-S8-b-the-squared-cycle-graph-S9.ppm)
	- Star
	![](https://www.researchgate.net/profile/Rui-Soares-Barbosa/publication/317100713/figure/fig1/AS:497742838288384@1495682548401/Example-of-a-star-graph-G-V-E-with-V-9-The-graph-state-G-is-LU-equivalent-to.png)
   
	- Grid
	- Lollipop
	- Dense
	- Sparse
	
### Graph traversals
![](https://miro.medium.com/max/1400/1*kvqvx89SQUd5lgR_rjse4A.png)
In directed graph, we would follow the direction of edges. 

- Walk : Closed walk when destination and source node are same
- Trail : Walk with no repeated edges - A circuit is a closed trail
- Path:  A walk with no repeated nodes - Cycle is a closed path
- 







References : 

https://flawnsontong.medium.com/what-is-geometric-deep-learning-b2adb662d91d
https://towardsdatascience.com/graph-theory-and-deep-learning-know-hows-6556b0e9891b
https://medium.com/@ashes192000/graph-neural-networks-part-2-6e3a44b0d835
