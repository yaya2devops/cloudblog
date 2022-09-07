# Containers, Docker | What exactly is that?

# The Innovation
It is important to understand how virtual machines work moving to containers in order to get started with docker effectively. <br>
Prior to the advent of containers, the virtual machine was the preferred technology for optimizing server capacity. Hence, let's begin with VMs.



## Virtual Machines

A Virtual Machine (VM) is a compute resource that runs programs and deploys apps using software rather than a physical computer. Because it operates an operating system and programs like a real computer does, it is sometimes known as a **software computer.**


### Why not begin with VMs first?


![VM1 (1600 × 840 px) (2).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1657573150673/s04iPcV_Z.png)
#### Oracle VM VirtualBox
[VirtualBox](https://www.virtualbox.org) is virtualization software that runs on multiple platforms. It enables users to use their existing computer to run multiple operating systems.

> To start using VirtualBox and get your VM up and running, follow these instructions.

- [Download](https://www.virtualbox.org/wiki/Downloads) VirtualBox
- [Download](https://support.system76.com/articles/install-pop/) the desired operating system's ISO file (Ubunto, Centos..)
- [Mount](https://pureinfotech.com/mount-iso-virtual-machine-virtualbox/) the [ISO file](https://www.howtogeek.com/356714/what-is-an-iso-file-and-how-do-i-open-one/) to VirtualBox

> An ISO file is a method of making all of the operating system's required files accessible and portable.


 

## Containers
Containers are portable software packages that include all of the components required to run in any environment.
Containers isolate software and allow it to operate independently across multiple operating systems, hardware, networks, storage systems, and security policies.

## From VMs to Containers

### Virtualization
A single physical hardware system can be used to create several dedicated resources or simulated environments thanks to virtualization technologies.
It is the conception of a virtual rather than actual version of something, such as a server, a desktop, a storage device, an operating system, or network resources.

### Containerization
Containerization is the process of packaging software code with all of its required components, such as libraries, frameworks, binairies, and other dependencies, so that they can be isolated in something called "container."
**Containerization allows you to deploy multiple applications using the same operating system on a single virtual machine or server.**
Thus, It enables the container-based application to move smoothly between development, testing, and production environments.

### VMs Vs Containers

On a single machine, several containers can run simultaneously as separate processes, sharing the same operating system kernel. Additionally, you must run an application on each guest operating system using the virtual machine.
 
Another notable comparison is the modest weight of containers.
 Containers can handle more applications than virtual machines, take up less space and eliminate the need for additional operating systems. 
![VM1 (1600 × 840 px).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1657560760280/Ugz-9SHtW.png)


As a result of using the same OS, containers cost less. <br>
Consequently, Code and dependencies are packaged together, an abstraction found at the application layer.

Intermodalism and the introduction of real containers changed the shipping sector.
The same is true for software containers, and docker in particular revolutionized the IT industry.


---

#  Docker


![VM1 (1600 × 840 px) (5).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1657651330340/t_vn4YJcC.png)
Docker is an open source software platform that simplifies the process of creating, running, managing, and distributing containers that hold your application. Although there are other market competitors, Docker ended up winning the containers game due to its simplicity.


As previously stated, containers are the foundation to start using docker. You'll also need a good understanding of computers and the command line. <br>Before we get into the technical stuff, let's go over the theory behind Docker and what functions it have, since, in my opinion, this is important for architectural perspective.
## Architecture

![VM1 (1600 × 840 px) (3).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1657580301789/_waVdExFP.png)
### Docker Engine
It is the foundation and the central part of the entire Docker system. Docker Engine is a client-server architecture application. It is set up on the host machine. The Docker engine is made up of three parts

- **Server** Docker is the name of the docker daemon. It is capable of creating and managing Docker images. Containers, networks, and so on.

- **API for Rest** It is used to instruct the Docker daemon.

- **CLI (Command Line Interface)**  It is a client that is used to enter Docker commands.

### Docker Client 
Docker clients allow users to interact with Docker. When a docker command is executed, the client sends it to the Docker daemon, which executes it. Docker commands make use of the Docker API. The Docker client can interact with multiple daemons.

> Docker daemon (dockerd) manages Docker objects by listening for Docker API requests.

### Docker Objets
When you work with Docker, you use images, containers, volumes, and networks; all of these are Docker objects.
## Key Components
### Docker Container
the container environment is created when you pull the Docker image to your local system and start it.

### Docker Image
Docker images serve as a template or collection of instructions for creating a Docker container. When utilizing Docker, the starting point is also a set of images. A snapshot and an image are similar concepts in virtual machine (VM) settings.<br> A docker image is a portable artifact that contains the actual application package, the configuration files and all the dependencies.

### Docker Registry
A named Docker image distribution and storage system is called a Docker registry. Multiple variations of the same image may exist and be distinguished using tags. A Docker registry is divided into Docker repositories, each of which contains every iteration of an individual image.

#### DockerHub
The official cloud-based registry for Docker images is called Docker Hub. Since Docker Hub is the official registry for Docker, it should come as no surprise that it is the default registry when you install Docker.

### Dockerfile
All the commands a user could issue on the command line to put together an image are listed in a text file called a Dockerfile. Users can design an automated build using docker build that sequentially runs numerous command-line commands.



👇Sample Dockerfile.
```
#FROM - Image to start building on.
FROM ubuntu:14.04

#MAINTAINER - Identifies the maintainer of the dockerfile.
MAINTAINER yahya@itzyahya.tech

#RUN - Runs a command in the container
RUN echo "Hello world" > /tmp/hello_world.txt

#CMD - Identifies the command that should be used by default when running the image as a container.
CMD ["cat", "/tmp/hello_world.txt"]
```

> Click For [Dockerfile Reference](https://docs.docker.com/engine/reference/builder/)

# Start With Docker
## Installation 
To get started with Docker, as with most tools, you first have to install it.<br>
For Windows, open Powershell as an administrator and run the following command.

``` Start-Process '.\win\build\Docker Desktop Installer.exe' -Wait install ```

Refer to [Get Docker](https://docs.docker.com/get-docker/) for further details regarding the installation on different OS. It's a very simple process, which is again why Docker has become so popular.
##  Frequently Used Commands
```docker
docker run   // Runs a <container> based on an <image>
docker push  // Pushes an <image> to a registry 
docker pull  // Pulls an <image> from a repository
docker ps    // Lists <containers>
docker build // Builds an <image> from a Dockerfile
docker tag   // Tags an <image>
docker images // Lists <images>
docker system prune // Remove unused <containers> and <images>
```





#  Will Containers replace VMs?

Although containerization has many benefits, some experts believe that virtual machines will still be needed in specific circumstances. <br> 👉 This is true because virtual machines and containerization both have unique features that support various solutions.

> **FunFact** I had a collision just as I was about to finish this article post, and I lost its content. So this is my second piece!

## Added to Further
Managing the container is enjoyable until you reach 213213 Containers. At this point, you require a container orchestration tool to make managing a large number of containers much easier. YES, it's the incredible Kubernetes! <br>Ladies and gentlemen, our next blog post will go over k8s in greater detail.
