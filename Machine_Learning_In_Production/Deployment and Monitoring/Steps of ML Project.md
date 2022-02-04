# Steps of an ML Project

---

- Scoping : Define Project, What do you want to do?
	- Accuracy
	- Latency
	- Queries Per Second
	- Resources
	- Budget
	- Timeline etc
This can be very problem dependent

- Data    : 
	- Define the data and establish baseline
	- Label and Organise the data
- Modelling:
	- Select and train the model
	- Perform error analysis 
		- Retrain model
		- Or it can also be going back to collect more data
- Deployment
	- Deployment in production
	- Monitor and Maintain system 
		- Update the model if needed
		- Perform Error analysis

---
### Case study : Speech recognition
![](speech_recognition.png)
- Define data
	- Is data labeled consistently?
    - How much silence before/after each clip?
    - How to perform volume normalization?
    
- Modelling
	- Usually code and hyperparameter are varied with same data
	- Instead try keeping the code fixed and varying Hyperparameters and data
	- If error analysis can tell how to improve the data it could be effice

- Deployment
	- VAD can be useful in capturing voices
	- Microphone connected to VAD Module
