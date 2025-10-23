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
