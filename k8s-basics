*** Kubernetes also known as K8s was built by Google based on their experience running containers in production. ***
It is now an open-source project and is arguably one of the best and most popular container orchestration technologies out there.
To understand Kubernetes, we must first understand two things – Container and Orchestration. Containers are completely isolated environments, 
as in they can have their own processes or services, their own network interfaces, their own mounts, just like Virtual machines, except that they all share the same OS kernel.

*** let us revisit some basics concepts of Operating Systems first: *** 
If you look at operating systems like Ubuntu, Fedora, Suse or Centos –they all consist of two things. An OS Kernel and a set of software. 
The OS Kernel is responsible for interacting with the underlying hardware. While the OS kernel remains the same– which is Linux in this case, 
it’s the software above it that make these Operating Systems different.

*** Docker containers share the underlying kernel. What does that actually mean – sharing the kernel? *** 
Let’s say we have a system with an Ubuntu OS with Docker installed on it. Docker can run any flavor of OS on top of it as long as they
are all based on the same kernel – in this case Linux. If the underlying OS is Ubuntu, docker can run a container based on another distribution
like debian, fedora, suse or centos

* (you wont be able to run a windows based container on a Docker host with Linux OS on it. For that you would require docker on a windows server.)
* (The main purpose of Docker is to containerize applications and to ship them and run them.)

*** The differences between virtual machines and containers. ***
IN DOCKER: we have the underlying hardware infrastructure, then the OS, and Docker installed on the OS. Docker then manages the
containers that run with libraries and dependencies alone.

IN VIRTUAL MACHINE: we have the OS on the underlying hardware, then the Hypervisor like a ESX or virtualization software of some kind and 
then the virtual machines. each virtual machine has its own OS inside it, then the dependencies and then the application.

--> This causes higher utilization of underlying resources if there are multiple virtual operating systems and kernel running. 
    The virtual machines also consume higher disk space, whereas docker containers are lightweight and are usually in Mega Bytes in size.
--> This allows docker containers to boot up faster, usually in a matter of seconds whereas VMs we know takes minutes to boot up as it needs to bootup the entire OS.

*** Let’s understand the difference between the containers and images. ***
--> An image is a package or a template, it is used to create one or more containers.
--> Containers are running instances off images that are isolated and have their own environments and set of processes.

********** Container Advantage *********
--> Traditionally developers developed applications. Then they hand it over to Ops team to deploy and manage it in production environments. They do that 
by providing a set of instructions such as information about how the hosts must be setup, what pre-requisites are to be installed on the host and how the 
dependencies are to be configured etc. Since the Ops team did not develop the application on their own, they struggle with setting it up.

--> With Docker, a major portion of work involved in setting up the infrastructure is now in the hands of the developers in the form of a Docker file.
now easily put together a Dockerfile to create an image for their applications. This image can now run on any container platform.

--> So the Ops team now can simply use the image to deploy the application. Since the image was already working when the developer built it and 
operations are not modifying it,it continues to work the same when deployed in production.

********** we now have our application packaged into a docker container **************
--> What if your application relies on other containers such as database or messaging services or other backend services?
What if the number of users increase and you need to scale your application? You would also like to scale down when the load decreases.

--> To enable these functionalities you need an underlying platform with a set of resources. The platform needs to orchestrate(manage) the connectivity between 
the containers and automatically scale up or down based on the load. This whole process of automatically deploying and managing containers is known as Container
Orchestration.

********************* Kubernetesis thus a container orchestration technology. **********************************8
--> There are multiple such technologies available today – Docker has its own tool called Docker Swarm. Kubernetes from Google and Mesos from Apache.
Kubernetes is now supported on all public cloud service providers like GCP, Azure and AWS.

--> There are various advantages of container orchestration. Your application is now highly available as hardware failures do not bring your application 
down because you have multiple instances of your application running on different nodes. The user traffic is load balanced across the various containers. 
When demand increases, deploy more instances of the application seamlessly and within a matter of second and we have the ability to do that at a service 
level. When we run out of hardware resources, scale the number of nodes up/down without having to take down the application. And do all of these easily 
with a set of declarative object configuration files.


******************** ARCHITECTURE of K8'S ***********************8
--> When you install Kubernetes on a System, you are actually installing the following components. An API Server. An ETCD service. A kubelet service. A Container Runtime,
Controllers and Schedulers.

1. API SERVER: The API server acts as the front-end for kubernetes. The users, management devices, CLIs all talk to the API server to interact with the kubernetes cluster.
   As tha cluster starts api servers starts and start commuicating with the worker nodes.
2. ETCD Service: It stores all the data of k8's cluster in key-value format. it is like database.
3. SCHEDULER: it is responsible for distributing work or containers across multiple nodes. handling pods ceeation and management on best config nodes.
4. CONTROLLERS: The controllers are the brain behind orchestration, They are responsible for noticing and responding when nodes, containers or endpoints goes down.
   The controllers makes decisions to bring up new containers in such cases.
5. KUBELET: it is a agent which is present on worker nodes in cluster. it is responsible for making sure that containers are running on the nodes and communicating with master node. 
6. CONTAINER RUNTIME: kubelet cannot create containers, there is software which is used to create/run containers like:(docker, crio, containerd).
7. KUBE-PROXY: it is responsible for cont. to container communication within node or outside the node.  






