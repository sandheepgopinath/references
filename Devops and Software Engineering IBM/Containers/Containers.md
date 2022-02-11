# Containers

- Executable unit of software in which application code is packaged along with libraries and dependenices so that it can be run anywhere
- It makes use Operating System Virtualization
- They do not need a Guest Operating system like in a VM
- Standarization for how we package and ship codes
- They can spin up quickly
- Software can be written once and can be run in different environments / laptops
- Helps to improve CPU and memory applications
- Good match for microservices architecture


# Containers vs Virtual Machines
![](containervsvm.png)


# Docker

Application for building and running applications as containers

Docker Image : Image built using docker technology

Docker Commands
- build : building a container image, it requires a dockerfiles. Images can be tagges with names

- tag : To copy the image and give the image a new name. This will not overwrite the old tag. This will create a copy

- run : To run a container . Suited for testing a built image

- push and Pull : storing images in remote location and retrieving them

# Container runtime 
![](container runtime.png)

- containers share the operating system

Other runtimes
- container deruntime
- rocket
