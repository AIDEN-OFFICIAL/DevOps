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
