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
- `docker run -d -e MYSQL_Root_Password=secret mysql` we can also set up -e(enviornment variables while installing and running in detatched mode)
- `docker run -d --name 'Mysq-newname' mysql:8.0` e can give costum names for each image
- `docker rmi 'image name` remove one image from the device 
- `docker rm 'container name` remove any Container from the device 
- `docker run -it ubuntu` run ubuntu in interactive mode.`exit` to come out of interactive mode
- `docker ps` show all running containers
- `docker ps -a` status of all images (-a, for all images)
#### run command always creates a new container, whereas there are start and stop commands to execute existing containers.
- `docker start 'name or Id'`to start a Docker container
- `docker stop 'name or Id'`to stop a Docker container
- `docker run -d -e 'setup env' -p8080:3360 mysql` so the default port is 3360, which is binded  with the 8080 so the mysql will run on this port container
- `docker logs Cont_ID` to get the logs of a specific container
- `docker exec -it Cont_ID /bin/bash` to get the bash of a container, so that we can perform different commands specific to the container, like ls, cd, env 
- `docker exec -it Cont_ID /bin/sh` same
- `docker network create Net_workName` to make two containers to interact with each other without the need for ports or connections(suppose MongoDB has to interact with Mongo Express) 
- `docker network ls` to list all network connections
- `docker network rm <network_name>` remove networks if they're not used by any containers
- `docker network inspect <network_name>`inspect if this network is being used
-  `docker run -d -p 27017:27017 --name mongo -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=qwerty --network mongo_net mongo`Here we have set up the mongo to run in detach mode, added envs, bound ports, added a new  name, and connected with a network.
-  ``

## Docker vs VM's
| **Aspect** | **Virtual Machines (VMs)** | **Docker Containers** |
|-------------|-----------------------------|------------------------|
| **Virtualization Level** | VMs virtualize **hardware**. Each VM runs a full guest OS (including its own kernel, libraries, and applications). | Docker virtualizes only the **application layer**. Containers share the **host OS kernel**, isolating applications using kernel features.|
| **Resource Usage** | Heavier, since each VM includes a full OS, taking more CPU, memory, and storage. | Lightweight, as containers share the host kernel and only package the application and its dependencies. |
| **Startup Time** | Slower — usually takes **minutes** to boot a full OS. | Much faster — containers start in **seconds** since no OS boot is needed. |
| **OS and Kernel Dependence** | **OS-agnostic** — you can run different operating systems (e.g., Windows VM on a Linux host) because the hypervisor abstracts hardware. | **Kernel-dependent** — containers share the host OS kernel (usually Linux). They can only run systems compatible with that kernel. |
| **How It Runs on Non-Linux Systems** | No issue — the VM hypervisor handles any OS guest. | On Windows/macOS, Docker Desktop uses a **lightweight Linux VM** (via Hyper-V, WSL2, or Apple Hypervisor) to provide a Linux kernel for containers. |
| **Performance** | Slightly lower due to hardware-level virtualization overhead. | Higher performance since containers run natively on the host OS kernel with less overhead. |
| **Isolation Level** | Strong isolation — each VM runs a full OS, providing complete separation. | Weaker isolation compared to VMs (still secure), since containers share the same kernel but have process-level isolation. |
| **Storage and Portability** | VM images are large (gigabytes) and less portable. | Docker images are lightweight (megabytes) and highly portable across environments. |
| **Use Cases** | Ideal for running multiple OS types, strong isolation, or legacy applications that require full system environments. | Ideal for microservices, CI/CD, and lightweight, scalable application deployments. |


## Docker Compose
Docker Compose is a tool that lets you define and manage multiple Docker containers (services) that work together, all from one configuration file called docker-compose.yml.
### 🧠 Why Use Docker Compose?

Let’s say you have a full-stack project:

- Node.js backend
- MongoDB database
- Nginx reverse proxy

Without Compose, you’d have to run 3 separate Docker commands, configure networks manually, link containers, expose ports, and remember environment variables for each.
😫 That’s painful.

With Compose, you can define all 3 in one YAML file 
and Docker will automatically:
- Create a network for them to talk to each other
- Build and start containers
- Manage dependencies (like starting MongoDB before Node)
- Handle volumes (for persistent data)
- Simplify startup/shutdown
- Reproducibility, One config = same environment everywhere

```yaml
services:
  mongo:
    image: mongo
    ports:
    - "27017:27017"
    environment:
      MONGO_INITDB_ROOT_USERNAME: admin
      MONGO_INITDB_ROOT_PASSWORD: qwerty
  mongo-exp:
   image: mongo-express
   ports: 
   - "27017:27017"
   environment: 
     ME_CONFIG_MONGODB_ADMINUSERNAME: admin
     ME_CONFIG_MONGODB_ADMINPASSWORD: qwerty
     ME_CONFIG_BASICAUTH_USERNAME: admin
     ME_CONFIG_BASICAUTH_PASSWORD: qwerty
     ME_CONFIG_MONGODB_URL: "mongodb://admin:qwerty@mongo:27017/"
```
**Docker Compose**
- `docker compose -f fileName.yaml up -d` to deploy a yaml file config to running containers in detach mode (up: starts the file )
- `docker compose -f fileName.yaml down` to remove files from our container

## Docker File creation
### commands:
`FROM <image>` - this specifies the base image that the build will extend.
`WORKDIR <path>` - this instruction specifies the "working directory" or the path in the image where files will be copied and commands will be executed.
`COPY <host-path> <image-path> `- this instruction tells the builder to copy files from the host and put them into the container image.
`RUN <command>` - this instruction tells the builder to run the specified command.
`ENV <name> <value>` - this instruction sets an environment variable that a running container will use.
`EXPOSE <port-number> `- this instruction sets configuration on the image that indicates a port the image would like to expose.
`USER <user-or-uid>` - this instruction sets the default user for all subsequent instructions.
`CMD ["<command>", "<arg1>"]` - this instruction sets the default command a container using this image will run.

## Dockerizing our APP
Create a docker file :

example:
```yaml
FROM node
ENV MONGO_URI=mongodb://admin:qwerty@localhost:27017/usersDB?authSource=admin \
    PORT=3000 \
    MONGO_INITDB_ROOT_USERNAME=admin \
    MONGO_INITDB_ROOT_PASSWORD=qwerty
WORKDIR /testapp
COPY . .
RUN npm i
CMD ["node", "server.js"]
# WORKDIR /app

```
