# cloud
# Cloud-computing-
Concepts of cloud computing, basics, related topics details 

![Screenshot_2024_0918_123427](https://github.com/user-attachments/assets/9b54d9e2-5cb2-4a28-a145-9a5e9fb7490a)

# Cloud Computing:- 

Cloud computing is the delivery of computing services—including servers, storage, databases, networking, software, analytics, and intelligence—over the Internet ("the cloud"). This allows for faster innovation, flexible resources, and economies of scale.

![Screenshot_2024_0918_123503](https://github.com/user-attachments/assets/5301d869-b3ae-46c5-9d6c-8bc54028f445)
 # Docker:-
Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.
 
 Key features of Docker include:-;
1.Containerization:
Applications run in isolated environments, which makes them portable and easy to manage.

2. Images and Dockerfile:
Docker uses images as blueprints for containers. A Dockerfile is a script that contains instructions to build an image.

3. Docker Hub:
A cloud-based registry where users can share and distribute Docker image

How Docker works:-
Docker works by providing a standard way to run your code. Docker is an operating system for containers. Similar to how a virtual machine virtualizes .containers virtualize the operating system of a server. Docker is installed on each server and provides simple commands you can use to build, start, or stop containers.

# container:-
A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

(in other and simple words )

Containers are an abstraction at the app layer that packages code and dependencies together. Multiple containers can run on the same machine and share the OS kernel with other containers, each running as isolated processes in user space. Containers take up less space than VMs (container images are typically tens of MBs in size), can handle more applications and require fewer VMs and Operating systems

Screenshot_2024_0918_124201

# Kubernestes :-
Kubernetes (sometimes shortened to K8s with the 8 standing for the number of letters between the “K” and the “s”) is an open source system to deploy, scale, and manage containerized applications anywhere.

Kubernetes has built-in commands to handle a lot of the heavy lifting that goes into application management, allowing you to automate day-to-day operations. You can make sure applications are always running the way you intended them to run. 
# Main Function/Usage:- Kubernetes manages containers, which package an application and its dependencies together to ensure it runs consistently across different environments. Containers are isolated units but lightweight compared to virtual machines.

**NODE**
A Node is the fundamental worker machine in a Kubernetes cluster. It can be either a physical machine or a virtual machine in a cloud environment. Each node runs the necessary services to support the containers it hosts, such as the container runtime (e.g., Docker), the Kubelet (which communicates with the Kubernetes control plane), and Kube-proxy (which manages networking for the pods).

TYPES OF NODES

Master Node- The master node is the brain of the Kubernetes cluster and handles scheduling, maintaining the desired state, and managing resources. It contains components like API Server,Scheduler,Controller Manager

Worker Node- Worker nodes are the machines where application workloads run. These nodes run the containers and host the pods that make up an application. They handle the execution of the actual tasks, networking, and storage management.

**PODS**
A Pod is the smallest and most basic deployable unit in Kubernetes (K8s). It represents a single instance of a running process in your cluster and can contain one or more containers that share the same network and storage resources. Typically, pods are used to run a single container, but there are cases where multiple containers need to work together closely, and in these cases, a pod will contain multiple tightly coupled containers.

Kubernetes Architecture
A Kubernetes environment consists of a control plane (master), a distributed storage system for keeping the cluster state consistent (etcd), and a number of cluster nodes (Kubelets).
![image](https://github.com/user-attachments/assets/0adc0296-4220-4d19-b0bb-a5b2807b1c9f)

# Minikube 
Minikube is a tool that sets up a Kubernetes environment on a local PC or laptop. This tool provides an easy means of creating a local Kubernetes environment on any Linux, Mac, or Windows system, where you can experiment with and test Kubernetes deployments. 

 # Orchestration
Orchestration is the automated coordination and management of complex tasks and processes, ensuring that different services and components work together effectively. In IT, it streamlines workflows and manages dependencies, especially in containerized environments.

**How to install minikube in dextop?**
Step 1: Set Up an AWS EC2 Instance
1.Log in to the AWS Management Console.
2.Launch an EC2 Instance:
Choose an Amazon Machine Image (AMI). For simplicity, a basic Ubuntu Server AMI (like Ubuntu 20.04) works well.

Select an instance type (e.g., t2.micro if you are using the free tier).

Configure security groups to allow SSH (port 22) and any other necessary ports (like 8443 for Kubernetes).

Launch the instance and download the key pair for SSH access.

Step 2: SSH into Your EC2 Instance
$ Use the key pair to SSH into your instance:

**ssh -i /path/to/your-key.pem ubuntu@your-ec2-instance-public-dns **

Step 3: Install Dependencies
Once you're logged in, update the package manager and install required packages:

sudo apt update sudo apt install -y curl wget apt-transport-https

Step 4: Install Minikube
Download Minikube
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 2. Install Minikube:

sudo install minikube /usr/local/bin/

Step 5: Install a Virtualization Driver
Minikube requires a virtualization driver to run. Since AWS does not support KVM, you can use Docker as the driver.

1. Install Docker
sudo apt install -y docker.io

2. Start Docker and enable it to run at startup
sudo systemctl start docker sudo systemctl enable docker

3. Add your user to the Docker group:
sudo usermod -aG docker $USER

Log out and back in for this change to take effect.

Step 6: Start Minikube
Now you can start Minikube using Docker as the driver:

minikube start --driver=docker

Step 7: Verify Installation
Check if Minikube is running:
minikube status

Step 8: Accessing Kubernetes Dashboard (Optional)
You can also access the Kubernetes dashboard:

minikube dashboard

Congratulations We achieved our Goal.
# Openstack :-
OpenStack is an open-source platform that lets you create and manage cloud computing services. It allows users to control computing power, storage, and networking in a data center through a web interface. Essentially, it helps organizations build their own private or public clouds, making it easier to deploy and manage applications.



 **QEMU**
QEMU is an open-source emulator and virtualization tool that allows you to run different operating systems on a host machine.



 # VPC
Amazon Virtual Private Cloud (VPC) is a virtual network that allows users to launch AWS resources in a logically isolated environment. It's a foundational service of AWS that gives users complete control over their virtual networking environment.

What is the difference between EC2 and VPC?
•EC2 is a virtual server that you can run your software on. VPC is a virtual network that you use to connect your virtual servers, and other resources.

Go to VPC and create a VPC then we have to create 4 subnets , where 2 subnets are private and other two are public .




create gateways:-
1st create INTERNET GATWAY , whic is to be connected to your VPC which is created earliy.

