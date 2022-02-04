# Building container images with Docker

- Dockerfile :blueprint from which image is built
- Image : Immutable file that contain source code,libraries dependencies. They are read only. They are templates for a container or snapshots of a container
- A container is a running image
- Images are read only. A write layer is placed on top of the images in the containers to execute


- A container is like a class

### Development of a container
1. Create a docker file with details ( has details about what to include in an image )
2. Each instruction in dockerfile will create a new read onlayer in the image. As more instructions are executed more read only layers will be added. Making a change here will result in a new image. 

3. Build the image using that docker file

4. When you run that image you have a running container. Now a container layer is added. This container layer has read-write options. 


Docker can auomatically build container images using info in dockerfile.


# Dockerfile instructions

- FROM 
	- Define base image. This is often from a public repository. There are pre built images for different applications already pre-built into the application
- RUN
	- Exceute arbitary commands. EG : Bash command. Each insturction is a new layer added on top of the previous
- ENV
	- Set environment variables in image
- ADD and COPY 
	- Copy files and directories into images.
	- To put exceutable cod/ files into image
	- ADD can add remote files and repositories
- CMD
	- To provvide default to executing a container
	- Usually defines the default executable file
	- The last added CMD will take effect as there can only be one CMD command

#### Example

	FROM ubuntu:18.04
    COPY ./app # Copes files from current local directory to app directory as a new image layer
    RUN make /app # To build the app
    CMD python /app/app.py # Default instruction to run the file
    
    
   