# What is Docker?
found to solve the problem "It's working in my computer"
Reasons :
- One or more files are missing
- software version mismatch
- different configurations across different machines
- suppose think like Docker is a package, and it consists of your applications  nodejs, MongoDB and the whole app with a fixed version
- docker-compose up: to add an  application into the container (isolated environment, where we can run any number of application versions)
- We can easily remove any app vversion without causing any issues in one go.
- Suppose we have the tension of unknowingly delete any dependencies that we think would be used in one version that we would like to remove, but at the same time we are afraid that it's something that shouldn't be removed. In such a situation Docker helps us sort out the dependencies specific to different versions of apps and remove those
docker-compose down --rmi all
- A virtual machine is an abstraction of a machine (physical hardware)

## Docker Daemon
The brain of Docker.

The Docker Daemon is the background service that runs on your host machine and manages all Docker objects — containers, images, networks, and volumes.

## 🧱Docker Images

- Think of images as blueprints or templates.
- They  contain everything needed to run an app — code, libraries, dependencies, and environment settings.

Example:

node:18 → an image with Node.js preinstalled

mongo:7 → an image with MongoDB setup
 
## 📦Docker Containers
- A container is a running instance of an image.
- You can create, start, stop, or delete containers anytime.
- Multiple containers can be created from the same image.
  
Example:

docker run -d --name myapp node:18

→ runs a container based on the node:18 image.

## ☁️ Docker Hub
Docker Hub is a public repository for Docker images (like GitHub for code).

You can:
- Pull images from Docker Hub → docker pull node:18
- Push your own images → share with others or reuse later.

### Docker Tags: Just like versions.

## Docker commands:
- `docker pull 'image name'` to pull an Image from Docker Hub to the local (pulling latest version)
- `docker pull 'image name':'version'`
- `docker images` gives the list of images present in the device
- `docker run 'image name'` to run a specific image. If not found then downloads from the Docker hub
- `docker run -d 'Image_name'` Runs the image in the Background in detach mode .
- `docker rmi 'image name` remove one image from the device 
- `docker rm 'container name` remove any Container from the device 
- `docker run -it ubuntu` run ubuntu in interactive mode.`exit` to come out of interactive mode
- `docker ps` show all running containers
- `docker ps -a` status of all images (-a, for all images)
#### run command always creates a new container, whereas there are start and stop commands to execute existing containers.
- `docker start 'name or Id'`to start a Docker container
- `docker stop 'name or Id'`to stop a Docker container
- 
