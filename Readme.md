# Cloud-computing-
Concepts of cloud computing, basics, related topics details
![image](https://github.com/user-attachments/assets/f63ac0e9-d0c6-4a68-a4e2-ae53cbf03be3)


# Cloud Computing:-
Cloud computing is the delivery of computing services—including servers, storage, databases, networking, software, analytics, and intelligence—over the Internet ("the cloud"). This allows for faster innovation, flexible resources, and economies of scale.

![image](https://github.com/user-attachments/assets/8d666a8a-875d-417e-9483-307a594a32ab)


# Docker:-
Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.

![image](https://github.com/user-attachments/assets/8f0c5250-9cc1-4ac2-a55b-1764a57fefb2)


# Key features of Docker include:-;
# 1.Containerization:
Applications run in isolated environments, which makes them portable and easy to manage.

# 2. Images and Dockerfile:
Docker uses images as blueprints for containers. A Dockerfile is a script that contains instructions to build an image.

# 3. Docker Hub:
A cloud-based registry where users can share and distribute Docker image

# How Docker works:-
Docker works by providing a standard way to run your code. Docker is an operating system for containers. Similar to how a virtual machine virtualizes .containers virtualize the operating system of a server. Docker is installed on each server and provides simple commands you can use to build, start, or stop containers.

![image](https://github.com/user-attachments/assets/599e459e-b17e-4dc7-9ea0-1f2167898403)


# What is the structure of a Docker image?:-
A Docker image is composed of multiple layers stacked on top of each other. Each layer represents a specific modification to the file system (inside the container), such as adding a new file or modifying an existing one. Once a layer is created, it becomes immutable, meaning it can't be changed.16 May 2023

![image](https://github.com/user-attachments/assets/2630141a-f853-42dd-a628-39d70f937ec1)


# HOW TO INSTALL DOCKER:-
To install Docker on a remote server using PuTTY, you'll first need to ensure you have access to a Linux server (like Ubuntu, CentOS, etc.) via SSH. Here's a step-by-step guide:

## Step 1:Connect to Your Server
## Step 2: Update Your Package Index
 Before installing Docker, it’s a good idea to update the package index:

sudo apt update
## Step 3:Install Prerequisites
# For Ubuntu, install the required packages:

sudo apt install apt-transport-https ca-certificates curl software-properties-common
# For CentOS, run:

sudo yum install -y yum-utils
## Step 4: Add Docker’s Official GPG Key
For Ubuntu:

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
For CentOS:

sudo rpm --import https://download.docker.com/linux/centos/gpg
# Step 5: Set Up the Stable Repository
For Ubuntu:

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
For CentOS:

sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
# Step 6: Install Docker
For Ubuntu:

sudo apt update
sudo apt install docker-ce
For CentOS:

sudo yum install docker-ce
# Step 7: Start Docker
Enable and start the Docker service:

sudo systemctl start docker
sudo systemctl enable docker
# Step 8: Verify the Installation
Check if Docker is running:

sudo systemctl status docker
You can also run a test container:

sudo docker run hello-world
# Step 9: (Optional) Manage Docker as a Non-Root User
If you want to run Docker commands without sudo, add your user to the

# Docker group:

sudo usermod -aG docker $USER
After running this command, log out and back in for the changes to take effect.

# Conclusion
You’ve successfully installed Docker using PuTTY! If you have any questions or run into issues, feel free to ask.

# container:-
A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

(in other and simple words )

Containers are an abstraction at the app layer that packages code and dependencies together. Multiple containers can run on the same machine and share the OS kernel with other containers, each running as isolated processes in user space. Containers take up less space than VMs (container images are typically tens of MBs in size), can handle more applications and require fewer VMs and Operating systems



# NGINX:-
NGINX is a high-performance web server and reverse proxy server that is widely used for serving web applications, handling HTTP and HTTPS requests, and load balancing traffic. It is known for its speed, efficiency, and ability to handle a large number of concurrent connections with low resource usage.

![image](https://github.com/user-attachments/assets/5651c9ee-4025-46dd-9ff7-0b01eeb7314d)


# HOW TO INSTALL NGINX :-
In this tutorial, we’ll show you how to install NGINX on Linux.

# Open your Linux machine and run an update using the command below:
sudo apt-get update
Next, run this command:

sudo apt-get install nginx
# Then, enable your firewall with the following:
sudo ufw enable
# To verify NGINX is installed, run the following:
nginx -v
# You can run the command below to find out if NGINX is running:
sudo ufw status
After running this command, you should see the following:

status: active

# To check whether your NGINX server is working fine, run the following:
sudo systemctl status nginx
# USING EC2 IN AWS:-
First open aws search EC2 then Launch Instance and there select keypair in putty then download it

after that Launch it and run putty and paste public id on HOST NAME and open that downloaded key pair for putty in SSH then Auth then Credentials and open there

# after that run it and write username as ubuntu as selected os and then type following commands
sudo apt update
sudo apt install apache2
# to install a web server on ip then
sudo su
# for convert $ into # for getting admin role then
cd /var/www/html/
##then

ls
# for list of html file in it
# then copy that html file name and write
rm index.html
rm means remove command
vi index.html
# this will open a notepad like and write html code there like (vi is editor) -
# then press ctrl+c then shift+colon then write wq and enter
# now copy your public ip and paste it on browser you will see the texts written by you (by using html above)
# congratulations you got it 👏🏻 🎉
# USING CONTAINER IN VM and adding nginx server by Docker:-
First open aws search EC2 then Launch Instance and there select keypair in putty then download it

after that edit network setting and click on add security group rule and select TCP,UDP,ALL TRAFFIC AND SELECT EVERYWHERE SOURCE TYPE IN THEM then Launch it and run putty and paste public id on HOST NAME and open that downloaded key pair for putty in SSH then Auth then Credentials and open there

after that run it and write username as ubuntu as selected os and then type following commands

curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
# this will install and run docker in your vm
newgrp docker
# this command will help us to use docker
docker ps
# this will list docker
docker --version
# this will display the version of docker installed
# now installing nginx
docker pull nginx
# You can download Nginx from a pre-built Docker image, with a default Nginx configuration, by above command. This downloads all the necessary components for the container.
docker run --name docker-nginx -p 80:80 nginx
# Nginx installed, you can configure the container so that it’s publicly accessible as a web server.
# run is the command to create a new container
# The --name flag is how you specify the name of the container. If left blank, a generated name like nostalgic_hopper will be assigned.
# -p specifies the port you are exposing in the format of -p local-machine-port:internal-container-port. In this case, you are mapping port :80 in the container to port :80 on the server.
# nginx is the name of the image on Docker Hub.
# now this will show this on your public ip
Screenshot_2024_0923_210801

# In your terminal, enter CTRL+C to stop the container from running.
docker ps -a
# verify the container status with this command
docker rm docker-nginx
# Remove the existing container
docker run --name docker-nginx -p 80:80 -d nginx
# Create a new, detached Nginx container,By attaching the -d flag, you are running this container in the background.
docker ps
# this will obtain info about your container
docker stop docker-nginx
# Stop the container
docker rm docker-nginx
# remove the container
# Building a Web Page to Serve on Nginx
mkdir -p ~/docker-nginx/html
# Create a new directory for your website content within the home directory
cd ~/docker-nginx/html
# by this you navigate into this
vi index.html
# now press i and write your code in html like
Screenshot_2024_0923_211405

# then press ctrl+c then shift+colon then write wq and enter
docker run --name docker-nginx -p 80:80 -d -v ~/docker-nginx/html:/usr/share/nginx/html nginx
Linking the Container to the Local Filesystem

# open your public ip in browser you will see as the content as your html code
# here you go 👏🏻
# Using Your Own Nginx Configuration File
cd ~/docker-nginx
docker cp docker-nginx:/etc/nginx/conf.d/default.conf default.conf
# Copy the Nginx config directory into your project folder
docker stop docker-nginx
docker rm docker-nginx
# to rebuild the container stop the container then remove it
docker run --name docker-ngir
# This command links the custom website pages to the container.
docker restart docker-nginx
# you need to restart your container to reflect changes on the associated pages.

# ORCHESTRATION:-
In cloud computing, orchestration is the process of coordinating and automating the management of applications, tools, and infrastructure  across multiple clouds

# Kubernestes :-
Kubernetes (sometimes shortened to K8s with the 8 standing for the number of letters between the “K” and the “s”) is an open source system to deploy, scale, and manage containerized applications anywhere.

Kubernetes has built-in commands to handle a lot of the heavy lifting that goes into application management, allowing you to automate day-to-day operations. You can make sure applications are always running the way you intended them to run.

![image](https://github.com/user-attachments/assets/caf3c1c5-b62f-447b-8da2-01048bbbc9b0)


# Minikube:-
Minikube is a tool that sets up a Kubernetes environment on a local PC or laptop. This tool provides an easy means of creating a local Kubernetes environment on any Linux, Mac, or Windows system, where you can experiment with and test Kubernetes deployments.



# USING MINIKUBE IN AWS
##First open aws search EC2 ,and download your passkey then Launch Instance and select 22.04 AMI then select t2.xlarge instance type then select keypair then configure storage to 30 GB then enable all traffic in network and Launch.

##Launch PuTTY and add the IP address from instance and add key pair file and open the PuTTY terminal.

## Now connect it with putty and login into it by writing ubuntu
# Now put some commands
curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
# it will install docker
sudo usermod -aG docker $USER
newgrp docker
# it will Add your local user to docker group so that your local user run docker commands
sudo snap install kubectl --classic
# it will intall kubernetes
kubectl version --client
# it checks the version
# Installing Minikube
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
minikube version
# it checks its version
# Starting Minikube with Docker Driver
minikube start --driver=docker
# If you encounter root privileges error, run:
minikube start --driver=docker --force
minikube status
# it checks its status
kubectl cluster-info
# it checks cluster info
kubectl config view
# it will show the config
kubectl get nodes
# it will display nodes in it
kubectl get pods
# it will show pods in it
kubectl create deployment nginx-web --image=nginx
kubectl expose deployment nginx-web --type NodePort --port=80
kubectl get deployment,pod,svc

# it will deploy a sample nginx deployment
minikube addons list
It will display all addons
minikube addons enable dashboard
minikube addons enable ingress
# this enables these addons
minikube dashboard --url**
# it will get the url and run the dashboard of MiniKube
kubectl proxy --address='0.0.0.0' --disable-filter=true &
# This will enable port :8001 to access it on your public ip
http://server_ip:8001/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/#/workloads?namespace=default
# in browser replace server ip with public ip
# Now go to above link and replace server_ip with your public ip and it will show you like :
Screenshot_2024_0923_213426
# KVM:- Kernel-based Virtual Machine
It is a technology that allows you to run multiple operating systems on a single physical machine. It turns the Linux kernel into a hypervisor, enabling virtual machines (VMs) to operate as if they were separate computers.

Screenshot_2024_1104_185025

# Openstack :-
OpenStack is an open-source platform that lets you create and manage cloud computing services. It allows users to control computing power, storage, and networking in a data center through a web interface. Essentially, it helps organizations build their own private or public clouds, making it easier to deploy and manage applications.

![image](https://github.com/user-attachments/assets/379c2be0-0e75-46b0-b4ce-e4d58721dadb)


# QEMU
QEMU is an open-source emulator and virtualization tool that allows you to run different operating systems on a host machine.

![image](https://github.com/user-attachments/assets/81f285be-3cbb-4406-a63f-90bab3d7ce37)


# VPC
•Go to VPC and create a VPC then we have to create 4 subnets , where 2 subnets are private and other two are public .




# create gateways:-
1st create INTERNET GATWAY , whic is to be connected to your VPC which is created earliy.

Screenshot_2024_1104_181831

•2nd we have to create VPG virtual privaye gate, and connect to VPC .

# create route tables
•Now we have to go to the route table and create 2 route table , one for IGW and another for VGW .

Screenshot_2024_1104_181847

•Now we have to connect two public subnet in myigw and on other we have to add the private subnets .

Screenshot_2024_1104_182425

# create instances
* now we have to create two instnaces where we have to enable the public IPv4 .

•then on both instance we have to downlaod the web server here i have downlaoded the apache2 server

-- after that i chech that my instances are working or not .

Screenshot_2024_1104_182258

# now we have to create the load balancer
--where we have to give vpc, aviablity zone of the ec2 instance

•then we have to create the target group where we have to select the two insatance we have create then we have to go to helath check edited option which was present below the load balancer is create ,then edit it as given below image

Screenshot_2024_1104_182902

•after that come to load balancer where we have to select the target group which we have created then make the load balancer , it will look like the given image below .

Screenshot_2024_1104_183106

Screenshot_2024_1104_183126

now put on any one instance write following commands in putty -

htop
seq 999999999999999999999999999999999999999999999999999999999 > /dev/null &
htop
Screenshot_2024_1104_183758

# book link for reference of VPC given below (page 55 )
{

