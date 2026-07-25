# Daily-Diary-TRCS-103
# Day 1 – Introduction to Cloud Computing & AWS
## Date: 22/06/2026
# Day 1 Summary
- Fundamentals of Cloud Computing
- Service Models (IaaS, PaaS, SaaS)
- Introduction to AWS
- AWS Account Creation Process
- Common AWS Services
- Basic Linux Commands
- IAM User and Group Management
- Multi-Factor Authentication (MFA)

 # Introduction to Cloud Computing
 Cloud computing is the delivery of computing services, such as servers, storage, databases, networking, software, and analytics, over the internet. Instead of purchasing and maintaining physical hardware, users can access these resources on demand from cloud service providers and pay only for what they use.

 ## Advantages of Cloud Computing
 - Pay-as-you-go pricing
- High scalability
- Global accessibility
- Automatic updates
- Better disaster recovery
- Reduced infrastructure costs

  
# Cloud Service Models
## IaaS (Infrastructure as a Service)
Provides virtual machines, storage, networking, and other infrastructure resources.

**Examples:**
- Amazon EC2
- Microsoft Azure VM
- Google Compute 

 ## PaaS (Platform as a Service)
 Provides a platform for developers to build, test, and deploy applications.
 
 **Examples:**
- AWS Elastic Beanstalk
- Google App Engine
- Heroku

## SaaS (Software as a Service)
Provides software applications through the internet.

**Examples:**
- Spotify
- Gmail
- Microsoft 365
- Google Docs

# Introduction to AWS
Amazon Web Services (AWS) is Amazon's cloud computing platform that provides more than 200 cloud services across computing, storage, networking, databases, analytics, machine learning, and security.

AWS is one of the most widely used cloud platforms because of its scalability, reliability, global reach, and pay-as-you-go pricing model.

## Benefits of AWS
- Global infrastructure
- High availability
- Enhanced security
- Cost optimization
- Elastic scalability
- Large service ecosystem

## Popular AWS Services

|Service   |     Purpose| 
|----------|-----------------|
|EC2	|Virtual Servers|
|S3|	Object Storage|
|IAM|	Identity and Access Management|
|RDS	|Managed Databases|
|VPC	|Virtual Private Cloud|
|Lambda|	Serverless Computing|
|CloudWatch|Monitoring and Logging|

## Steps to Create an AWS Account
1. Open https://aws.amazon.com
2. Click Create an AWS Account.
3. Enter email address, account name, and password.
4. Verify your email.
5. Select Personal or Business account.
6. Enter contact information.
7. Add payment information.
8. Verify phone number using OTP.
9. Choose the Basic Support Plan.
10. Sign in to the AWS Management Console.

# Linux Commands Learned
Linux is a command-line based operating system widely used in cloud environments and AWS servers.

## Basic Commands

| **Command**                  | **Syntax / Example**     | **Description**                                             |
| ---------------------------- | ------------------------ | ----------------------------------------------------------- |
| Current Directory            | `pwd`                    | Displays the present working directory.                     |
| Current User                 | `whoami`                 | Displays the currently logged-in user.                      |
| List Files                   | `ls`                     | Lists files and directories.                                |
| Detailed File List           | `ls -l`                  | Shows file permissions, owner, size, and modification date. |
| Sort by Latest Modified Time | `ls -lt`                 | Lists files sorted by the latest modification time.         |
| Show Hidden Files            | `ls -a`                  | Displays hidden files and directories.                      |
| Display Current Date         | `date`                   | Shows the current system date and time.                     |
| Display Date Format          | `date +%D`               | Shows the date in **MM/DD/YY** format.                      |
| Change Directory             | `cd folder_name`         | Moves into the specified directory.                         |
| Move Back One Directory      | `cd ..`                  | Moves to the parent directory.                              |
| Create Directory             | `mkdir myfolder`         | Creates a new directory named **myfolder**.                 |
| Remove Empty Directory       | `rmdir myfolder`         | Deletes an empty directory.                                 |
| Create File                  | `touch file.txt`         | Creates an empty file named **file.txt**.                   |
| View File Content            | `cat file.txt`           | Displays the contents of a file.                            |
| Copy File                    | `cp file1.txt file2.txt` | Copies **file1.txt** to **file2.txt**.                      |
| Rename/Move File             | `mv old.txt new.txt`     | Renames or moves a file.                                    |
| Delete File                  | `rm file.txt`            | Removes the specified file.                                 |
| Clear Terminal               | `clear`                  | Clears the terminal screen.                                 |
| Display Command Manual       | `man ls`                 | Displays the manual page for the **ls** command.            |

# IAM (Identity and Access Management)
IAM is an AWS service used to manage users, groups, roles, and permissions securely.

 ## Features
- User Management
- Group Management
- Role-Based Access Control
- Permission Policies
- MFA Support

# MFA (Multi-Factor Authentication)
MFA adds an additional security layer by requiring users to verify their identity using a second authentication method such as:
- Authenticator App
- SMS OTP
- Hardware Security Key
 
## Benefits of MFA
- Improved account security
- Protection against password theft
- Reduced unauthorized access



# Day 2 Training Diary – AWS EC2 (Elastic Compute Cloud)
## Date: 23/06/2026

# Introduction to Amazon EC2
- Creating virtual servers in AWS
- AMI and Instance Types
- Key Pair creation
- Security Groups and firewall rules
- Launching an EC2 Instance
- Connecting using Browser and SSH
- Hosting a basic web page
- Accessing the website using Public IP
- Basic EC2 monitoring concepts

# Amazon EC2 (Elastic Compute Cloud)
 Amazon EC2 is one of the most widely used AWS services. It provides virtual servers in the cloud, known as instances, which allow users to run applications without purchasing physical hardware.

EC2 enables users to create, manage, monitor, and scale virtual machines according to their requirements.

## Features of EC2
- Provides virtual servers on demand
- Scalable computing capacity
- Pay-as-you-go pricing
- Supports multiple operating systems
- Easy integration with other AWS services
- Monitoring through Amazon CloudWatch
- Secure access using Key Pairs and Security Groups

# EC2 Terminology
## Instance
A virtual machine running in AWS.

## AMI (Amazon Machine Image)
A template used to launch an EC2 instance.

**Examples:**
- Amazon Linux
- Ubuntu
- Red Hat Enterprise Linux
- Windows Server

## Instance Type
Defines CPU, memory, storage, and networking capacity.

**Examples:**
- t2.micro
- t3.micro
- t3.small

## Key Pair
 Used for secure login to the instance.

- Public Key stored by AWS
- Private Key downloaded by user

## Security Group
Acts as a virtual firewall controlling incoming and outgoing traffic.

# Steps to Create an AWS EC2 Instance (Easy to Learn)
## Step 1: Login to AWS Console
- Open the AWS Management Console.
- In the search bar, type EC2.
- Click EC2 to open the EC2 Dashboard.

## Step 2: Launch a New Instance
Click:
EC2 Dashboard → Launch Instance

This starts the process of creating a new virtual server.

## Step 3: Configure Instance Details
Fill in the following information:

| **Setting**                | **Example**                   |
| -------------------------- | ----------------------------- |
| **Instance Name**          | MyFirstServer                 |
| **Operating System (AMI)** | Amazon Linux 2023             |
| **Instance Type**          | t2.micro (Free Tier Eligible) |

### Step 4: Create Key Pair

Click:

```text
Create New Key Pair
```

Provide:

- Key Pair Name
- Key Pair Type (RSA)
- File Format (.pem)

Download and save the key securely.

### Step 5: Configure Network Settings

Select:

- VPC
- Subnet
- Auto Assign Public IP

Enable public IP if the instance needs internet access.

---

# Security Settings (Security Groups)

Security Groups act as virtual firewalls.

### Common Rules

| Type | Protocol | Port | Purpose |
|--------|----------|------|----------|
| SSH | TCP | 22 | Remote Login |
| HTTP | TCP | 80 | Website Access |
| HTTPS | TCP | 443 | Secure Website Access |

### Example Security Group

Allow:

```text
SSH (22) from My IP
HTTP (80) from Anywhere
HTTPS (443) from Anywhere
```

### Why Security Groups are Important

- Protect instances from unauthorized access
- Control incoming traffic
- Improve cloud security
- Reduce attack surface

---

# Step 6: Configure Storage

Default storage can be used or customized.

Example:

```text
8 GB General Purpose SSD
```

---

# Step 7: Launch Instance

Review all settings and click:

```text
Launch Instance
```

AWS creates the virtual server.

---

# Instance States

| State | Meaning |
|---------|---------|
| Pending | Starting up |
| Running | Active and usable |
| Stopping | Shutting down temporarily |
| Stopped | Powered off |
| Terminated | Permanently deleted |

---

# Connecting to the EC2 Instance

## Using EC2 Instance Connect (Browser)

1. Open EC2 Dashboard.
2. Select the running instance.
3. Click **Connect**.
4. Choose **EC2 Instance Connect**.
5. Click **Connect** again.

A browser-based terminal opens.

---

## Using SSH

Linux/Mac:

```bash
chmod 400 mykey.pem

ssh -i mykey.pem ec2-user@public-ip-address
```

Example:

```bash
ssh -i mykey.pem ec2-user@54.123.45.67
```

---

# Hosting a Web Page on EC2

After connecting to the instance:

## Update Packages

```bash
sudo yum update -y
```

## Install Apache Web Server

```bash
sudo yum install httpd -y
```

## Start Apache

```bash
sudo systemctl start httpd
```

## Enable Apache at Boot

```bash
sudo systemctl enable httpd
```

## Create Sample Web Page

```bash
echo "<h1>Hello from AWS EC2</h1>" | sudo tee /var/www/html/index.html
```

---

# Running the Website on Web Browser

1. Ensure HTTP (Port 80) is allowed in Security Group.
2. Copy the Public IPv4 Address of the instance.
3. Open browser and enter:

```text
http://Public-IP
```

Example:

```text
http://54.123.45.67
```

The webpage should display:

```text
Hello from AWS EC2
```

---

# Monitoring EC2

AWS provides monitoring through CloudWatch.

Metrics include:

- CPU Utilization
- Network Traffic
- Disk Usage
- Instance Health



---

# Summary

Amazon EC2 provides scalable virtual servers in the cloud. During today's session, I learned how to launch an EC2 instance, configure security settings, connect to the server, deploy a simple web page, and access it through a web browser using the instance's public IP address.






# Day 3 Training Diary – AWS S3 (Simple Storage Service)
## Date: 24/06/2026

## Today I Learned
- Introduction to Amazon S3
- Creating and managing S3 buckets
- Uploading files and hosting websites using S3
- S3 Storage Classes
- Lifecycle Configuration
- AWS Snow Family Services

# Amazon S3 (Simple Storage Service)
Amazon S3 (Simple Storage Service) is an object storage service provided by AWS. It is designed to store and retrieve any amount of data from anywhere over the internet.

S3 offers high durability, availability, scalability, and security, making it one of the most popular cloud storage solutions.

## Features of S3
- Unlimited object storage
- Highly scalable
- 99.999999999% (11 9's) durability
- Secure data storage
- Versioning support
- Lifecycle management
- Static website hosting

## Common Uses of S3
- File storage
- Backup and recovery
- Static website hosting
- Media storage
- Data archiving
- Application data storage

# S3 Terminology
**Bucket**
A bucket is a container used to store objects (files) in Amazon S3.

**Bucket Naming Rules**
- Bucket names must be globally unique.
- Must contain only lowercase letters, numbers, and hyphens.
- Cannot contain spaces or uppercase letters.

Example:

```text
my-training-bucket
```

## Object

An object is a file stored inside a bucket.

Examples:

- Images
- Videos
- Documents
- HTML files
- PDFs

---

# Steps to Create an S3 Bucket

### Step 1

Open AWS Management Console.

### Step 2

Search for:

```text
S3
```

### Step 3

Click:

```text
Create Bucket
```

### Step 4

Enter:

- Bucket Name
- AWS Region

Example:

```text
Bucket Name: my-training-bucket
Region: ap-south-1 (Mumbai)
```

### Step 5

Configure bucket settings:

- Versioning (Optional)
- Encryption
- Public Access Settings

### Step 6

Click:

```text
Create Bucket
```

The bucket is now ready to store files.

---

# Uploading Files to S3

### Step 1

Open the bucket.

### Step 2

Click:

```text
Upload
```

### Step 3

Select files from your computer.

### Step 4

Review permissions and storage class.

### Step 5

Click:

```text
Upload
```

The files will now be stored in Amazon S3.

---

# Hosting a Static Website Using S3

Amazon S3 can host static websites containing:

- HTML
- CSS
- JavaScript
- Images

### Step 1

Create a bucket.

### Step 2

Upload website files.

Example:

```text
index.html
style.css
images/
```

### Step 3

Enable Static Website Hosting

Navigate to:

```text
Properties → Static Website Hosting
```

Select:

```text
Enable
```

Specify:

```text
Index Document: index.html
```

### Step 4

Configure Bucket Permissions

Disable Block Public Access (if required).

Add Bucket Policy to allow public read access.

### Step 5

Open Website Endpoint

AWS generates a website URL:

```text
http://bucket-name.s3-website-region.amazonaws.com
```

The website can now be accessed through a web browser.
# S3 Storage Classes
Storage classes help optimize cost based on how frequently data is accessed.
| **Storage Class**                 | **Use Case**                                    |
| --------------------------------- | ----------------------------------------------- |
| **S3 Standard**                   | Frequently accessed data                        |
| **S3 Intelligent-Tiering**        | Automatic cost optimization                     |
| **S3 Standard-IA**                | Infrequently accessed data                      |
| **S3 One Zone-IA**                | Infrequent access in a single Availability Zone |
| **S3 Glacier Instant Retrieval**  | Archived data with quick retrieval              |
| **S3 Glacier Flexible Retrieval** | Long-term backup and archive                    |
| **S3 Glacier Deep Archive**       | Lowest-cost archival storage                    |

# Lifecycle Configuration
Lifecycle Configuration automatically manages objects throughout their lifecycle.

It helps reduce storage costs by moving data to cheaper storage classes or deleting old files.

**Example Lifecycle Rule**
After:

- 30 days → Move to Standard-IA
- 90 days → Move to Glacier
- 365 days → Delete Object
- 
**Benefits**
- Cost optimization
- Automated storage management
- Reduced manual effort
- Better compliance management

## AWS Snow Family
AWS Snow Family is a group of physical devices used to transfer large amounts of data between on-premises systems and AWS.

It is useful when internet bandwidth is limited or data transfer over the network would take too long.

### Snowcone
Smallest device in the Snow Family.

**Features**
- Portable
- Lightweight
- Edge computing support
- Suitable for remote locations
- 
### Snowball Edge
Used for large-scale data migration and edge computing.

**Features**
- Large storage capacity
- Secure data transfer
- Local processing capability

### Snowmobile
A truck-sized data transfer service used for transferring exabytes of data.

**Features**
- Extremely large-scale migration
- Secure transportation
- Suitable for enterprise-level data transfers

## Advantages of AWS Snow Family
- Faster migration of large datasets
- Secure data transfer
- Reduced network dependency
- Supports edge computing
- Useful in remote environments


# Training Diary – AWS VPC (Virtual Private Cloud)
### Date: 25/06/2026
## Today I Learned
- Introduction to Amazon VPC
- Components of a VPC
- Public and Private Subnets
- Internet Gateway
- Route Tables
- Network ACL (Access Control List)
- NAT Gateway
- Why EC2 and RDS should not be connected directly
- Steps to create a VPC
- Launching an EC2 instance inside a VPC

# Amazon VPC (Virtual Private Cloud)
Amazon VPC (Virtual Private Cloud) is a service that allows users to create a private and isolated virtual network within AWS. It gives complete control over networking, including IP address ranges, subnets, routing, and security.

A VPC enables you to securely launch AWS resources such as EC2 instances, RDS databases, and Load Balancers in a logically isolated environment.

# Why Do We Need a VPC?
A VPC provides:

- Network isolation
- Better security
- Controlled internet access
- Secure communication between AWS services
- Custom networking configuration
- Flexible IP address management

# Components of a VPC
## 1. Subnet
A subnet is a smaller section of a VPC.

There are two main types:

### Public Subnet
- Connected to the Internet Gateway
- Used for web servers and public applications
- Can be accessed from the internet

### Private Subnet
- Not directly accessible from the internet
- Used for databases and backend services
- Provides enhanced security

## 2. Internet Gateway (IGW)
An Internet Gateway connects a VPC to the internet.

Functions:

- Allows inbound internet traffic
- Allows outbound internet traffic
- Required for resources in public subnets

## 3. Route Table
A Route Table contains rules that determine where network traffic should be directed.

Example:
| **Destination** | **Target**       |
| --------------- | ---------------- |
| Local VPC       | Local            |
| 0.0.0.0/0       | Internet Gateway |
Without a route table, network traffic cannot reach its destination correctly.

## 4. Network ACL (Access Control List)
A Network ACL is an optional firewall that controls traffic entering and leaving a subnet.

Characteristics:

- Works at subnet level
- Supports Allow and Deny rules
- Stateless (both inbound and outbound rules must be configured)

Example Rules:

- Allow HTTP (Port 80)
- Allow HTTPS (Port 443)
- Allow SSH (Port 22)
- Deny unwanted traffic

## 5. NAT Gateway

A NAT (Network Address Translation) Gateway allows instances in a private subnet to access the internet without exposing them to incoming internet traffic.

Uses:

- Software updates
- Downloading packages
- Accessing AWS services securely

Benefits:

- Secure outbound internet access
- Keeps private instances hidden
- Improves network security

---

# Why Not Connect EC2 and RDS Directly?

In a secure AWS architecture, the database should not be publicly accessible.

### Recommended Architecture

```text
Internet
     │
Internet Gateway
     │
Public Subnet
     │
 EC2 Instance
     │
Private Subnet
     │
 RDS Database
```

### Reasons

- Better security
- Prevent unauthorized database access
- Reduced attack surface
- Separation of application and database layers
- Easier compliance with security best practices

In this setup:

- Users access the EC2 instance.
- The EC2 instance communicates with the RDS database privately inside the VPC.
- The RDS database is never directly exposed to the internet.

---

# Steps to Create a VPC

### Step 1

Open the AWS Management Console.

Search for:

```text
VPC
```

### Step 2

Click:

```text
Create VPC
```

### Step 3

Enter:

- VPC Name
- IPv4 CIDR Block

Example:

```text
Name: MyVPC

CIDR Block:
10.0.0.0/16
```

### Step 4

Create Subnets

Example:

Public Subnet

```text
10.0.1.0/24
```

Private Subnet

```text
10.0.2.0/24
```

### Step 5

Attach an Internet Gateway.

### Step 6

Create Route Tables.

Associate:

- Public Route Table → Public Subnet
- Private Route Table → Private Subnet

### Step 7

Configure Network ACLs and Security Groups.

---

# Creating an EC2 Instance in a VPC

1. Open EC2 Dashboard.
2. Click **Launch Instance**.
3. Select the desired AMI.
4. Choose an Instance Type.
5. Select the VPC created earlier.
6. Choose the Public Subnet (or Private Subnet if required).
7. Create or select an existing Key Pair.
8. Configure the Security Group.
9. Review all settings.
10. Launch the instance.

The EC2 instance will now be deployed inside your custom VPC.

---

# Best Practices

- Place web servers in Public Subnets.
- Place databases in Private Subnets.
- Use Security Groups for instance-level security.
- Use Network ACLs for subnet-level security.
- Enable NAT Gateway for private subnet internet access.
- Follow the principle of least privilege.

---



# Summary

Amazon VPC is the foundation of networking in AWS. It provides a secure environment where AWS resources can communicate safely while controlling internet access through components such as subnets, Internet Gateway, Route Tables, NAT Gateway, and Network ACLs. Proper VPC design improves security, scalability, and overall application architecture.



# Training Diary – Weekly Revision

**Date:** 26/06/2026

## Today I Learned

Today was dedicated to revising all the AWS concepts covered during the first week of training. We reviewed the fundamental cloud computing concepts, Linux commands, IAM, EC2, S3, and VPC to strengthen our understanding and clear any doubts.

---

# Weekly Revision Topics

## 1. Cloud Computing

### Important Points

- Cloud computing is the delivery of IT resources over the internet.
- Resources are available on demand.
- Pay only for the resources used.
- Highly scalable and reliable.

### Cloud Service Models

| Model | Description | Example |
|--------|-------------|---------|
| IaaS | Infrastructure as a Service | Amazon EC2 |
| PaaS | Platform as a Service | AWS Elastic Beanstalk |
| SaaS | Software as a Service | Gmail, Spotify |

---

# 2. AWS Basics

### AWS Benefits

- Global Infrastructure
- High Availability
- Elastic Scalability
- Secure Services
- Pay-as-you-go Pricing

### Important AWS Services

- EC2
- S3
- IAM
- VPC
- RDS
- Lambda
- CloudWatch

---

# 3. Linux Commands Revision

| Command | Purpose |
|----------|----------|
| `pwd` | Show current directory |
| `whoami` | Display logged-in user |
| `ls` | List files |
| `ls -l` | Detailed file list |
| `ls -lt` | Sort files by latest modification |
| `ls -a` | Show hidden files |
| `cd` | Change directory |
| `mkdir` | Create directory |
| `rmdir` | Remove empty directory |
| `touch` | Create file |
| `cat` | Display file contents |
| `cp` | Copy files |
| `mv` | Move or rename files |
| `rm` | Delete files |
| `date` | Display system date |
| `clear` | Clear terminal |

---

# 4. IAM (Identity and Access Management)

### Key Concepts

- Create Users
- Create Groups
- Assign Permissions
- Roles
- Policies
- Multi-Factor Authentication (MFA)

### Why IAM?

- Secure AWS resources
- Control user permissions
- Prevent unauthorized access

---

# 5. Amazon EC2

### Important Concepts

- Virtual Server
- Amazon Machine Image (AMI)
- Instance Types
- Key Pair
- Security Group
- Public IP Address

### EC2 Instance Creation Steps

1. Launch Instance
2. Select AMI
3. Choose Instance Type
4. Create Key Pair
5. Configure Network
6. Configure Security Group
7. Launch Instance

### Security Group Ports

| Port | Purpose |
|------|---------|
| 22 | SSH |
| 80 | HTTP |
| 443 | HTTPS |

---

# 6. Amazon S3

### Important Concepts

- Bucket
- Object
- Bucket Policy
- Static Website Hosting
- Versioning
- Lifecycle Rules

### Storage Classes

- S3 Standard
- Intelligent-Tiering
- Standard-IA
- One Zone-IA
- Glacier Instant Retrieval
- Glacier Flexible Retrieval
- Glacier Deep Archive

### Uses of S3

- File Storage
- Website Hosting
- Backup
- Archive
- Media Storage

---

# 7. Amazon VPC

### Components

- VPC
- Public Subnet
- Private Subnet
- Internet Gateway
- Route Table
- Network ACL
- NAT Gateway
- Security Group

### Best Practice Architecture

```text
Internet
    │
Internet Gateway
    │
Public Subnet
    │
EC2 Instance
    │
Private Subnet
    │
RDS Database
```

### Why Keep RDS Private?

- Better security
- Prevent direct internet access
- Reduced attack surface
- Secure communication through EC2

---

# Important Interview Questions Revised

### Q1. What is Cloud Computing?

Delivery of computing resources over the internet on a pay-as-you-go basis.

### Q2. Difference between IaaS, PaaS, and SaaS?

- IaaS provides infrastructure.
- PaaS provides a development platform.
- SaaS provides ready-to-use software.

### Q3. What is IAM?

IAM is used to manage users, groups, roles, and permissions securely in AWS.

### Q4. What is an EC2 Instance?

A virtual server running in AWS.

### Q5. What is an S3 Bucket?

A logical container used to store files (objects) in Amazon S3.

### Q6. What is VPC?

A private virtual network that securely hosts AWS resources.

### Q7. Difference between Security Group and Network ACL?

| Security Group | Network ACL |
|---------------|-------------|
| Works at Instance level | Works at Subnet level |
| Stateful | Stateless |
| Supports Allow rules


# Training Diary – Introduction to Docker

**Date:** 29/06/2026

## Today I Learned

- Introduction to Docker and Containers
- Difference between Virtual Machines and Containers
- Steps to install Docker
- Docker Images
- Basic Docker Commands
- Docker Containers
- Docker Hub

---



# Introduction to Docker

Docker is an open-source containerization platform that enables developers to build, package, and run applications in lightweight, portable containers.

Unlike virtual machines, Docker containers share the host operating system's kernel, making them faster and more efficient.

## Advantages of Docker

- Lightweight and fast
- Platform independent
- Easy application deployment
- Efficient resource utilization
- Faster startup time
- Simplified application management

---

# What is a Container?

A container is a lightweight, standalone package that contains everything needed to run an application, including:

- Application code
- Runtime
- Libraries
- Dependencies
- Configuration files

Containers ensure that applications run consistently across different environments.

---

# Virtual Machine vs Docker Container

| Virtual Machine | Docker Container |
|-----------------|------------------|
| Runs on a Hypervisor | Runs on Docker Engine |
| Includes a complete Guest OS | Shares Host OS Kernel |
| Heavyweight | Lightweight |
| Slower startup | Starts in seconds |
| Uses more RAM and Storage | Uses fewer resources |
| Better isolation | Faster deployment |

---

# Steps to Install Docker

### On Ubuntu/Linux

### Step 1

Update packages.

```bash
sudo apt update
```

### Step 2

Install Docker.

```bash
sudo apt install docker.io -y
```

### Step 3

Start Docker service.

```bash
sudo systemctl start docker
```

### Step 4

Enable Docker at boot.

```bash
sudo systemctl enable docker
```

### Step 5

Check Docker version.

```bash
docker --version
```

### Step 6

Verify installation.

```bash
docker run hello-world
```

---

# Docker Images

A Docker Image is a read-only template used to create containers.

It contains:

- Application
- Dependencies
- Libraries
- Environment settings

Popular Images:

- Ubuntu
- Nginx
- MySQL
- Redis
- Python
- Node.js

---

# Docker Hub

Docker Hub is the official online repository where Docker images are stored.

It allows users to:

- Download images
- Upload custom images
- Share applications
- Search for official images

Website:

https://hub.docker.com

---

# Basic Docker Commands

## Check Docker Version

```bash
docker --version
```

## Display Docker Information

```bash
docker info
```

## Download an Image

```bash
docker pull ubuntu
```

## List Downloaded Images

```bash
docker images
```

## Search Images

```bash
docker search nginx
```

---

# Docker Container Commands

## List Running Containers

```bash
docker ps
```

## List All Containers

```bash
docker ps -a
```

## Run a Container

```bash
docker run ubuntu
```

## Run Container in Background

```bash
docker run -d nginx
```

## Run a Named Container

```bash
docker run --name mycontainer ubuntu
```

## Start a Container

```bash
docker start mycontainer
```

## Stop a Container

```bash
docker stop mycontainer
```

## Restart a Container

```bash
docker restart mycontainer
```

## Inspect a Container

```bash
docker inspect mycontainer
```

Displays detailed information about the container in JSON format.

## View Container Logs

```bash
docker logs mycontainer
```

## Execute Commands Inside a Running Container

```bash
docker exec -it mycontainer bash
```

## Delete a Stopped Container

```bash
docker rm mycontainer
```

## Delete an Image

```bash
docker rmi ubuntu
```

---

# Docker Workflow

```text
Dockerfile
      │
      ▼
Docker Image
      │
      ▼
Docker Container
      │
      ▼
Running Application
```

---

# Key Points

- Docker uses containers instead of virtual machines.
- Images are templates used to create containers.
- Containers are lightweight and portable.
- Docker Hub stores official and custom Docker images.
- Docker simplifies application deployment across different envir


# Training Diary – Docker Hub, Docker Images & Port Binding

**Date:** 30/06/2026

## Today I Learned

- Docker Hub and its features
- Docker Images
- Pulling images from Docker Hub
- Port Binding in Docker
- Running containers using Docker Hub images
- Accessing Docker applications through the browser

---

# Docker Hub

Docker Hub is the official cloud-based repository for Docker images. It allows developers to store, share, and download container images.

Docker Hub contains:

- Official Images
- Community Images
- Private Repositories
- Public Repositories

Website:

```text
https://hub.docker.com
```

## Advantages of Docker Hub

- Easy image sharing
- Access to official images
- Version management using tags
- Secure image storage
- Supports CI/CD integration

---

# Docker Images

A Docker Image is a read-only template used to create Docker containers.

An image contains:

- Application code
- Runtime
- Libraries
- Dependencies
- Environment variables

Popular Images available on Docker Hub:

- Ubuntu
- Nginx
- Apache
- MySQL
- Redis
- Python
- Node.js
- MongoDB

---

# Searching for Images

Search for an image:

```bash
docker search nginx
```

Download an image:

```bash
docker pull nginx
```

View downloaded images:

```bash
docker images
```

---

# Steps to Run an Image from Docker Hub

### Step 1

Open Docker Hub and search for the required image.

Example:

```text
Nginx
```

### Step 2

Copy the Docker pull command.

Example:

```bash
docker pull nginx
```

### Step 3

Verify that the image has been downloaded.

```bash
docker images
```

### Step 4

Run the image as a container.

```bash
docker run nginx
```

### Step 5

View the running container.

```bash
docker ps
```

---

# Port Binding

Port Binding maps a port inside the Docker container to a port on the host machine.

Syntax:

```bash
docker run -p <host-port>:<container-port> <image-name>
```

Example:

```bash
docker run -p 8080:80 nginx
```

Here:

- **8080** → Host machine port
- **80** → Container port

This allows users to access the application running inside the container through the host machine.

---

# Running an Nginx Container with Port Binding

Run the container:

```bash
docker run -d -p 8080:80 --name my-nginx nginx
```

Explanation:

- `-d` → Run in detached (background) mode.
- `-p 8080:80` → Bind host port 8080 to container port 80.
- `--name my-nginx` → Assign a custom name.
- `nginx` → Docker image.

---

# Accessing the Application

After the container starts, open your web browser and visit:

```text
http://localhost:8080
```

If running on an AWS EC2 instance, use the public IP:

```text
http://<EC2-Public-IP>:8080
```

The default Nginx welcome page should appear.

> **Note:** If using AWS EC2, ensure that port **8080** is allowed in the EC2 Security Group.

---

# Useful Docker Commands

## List Running Containers

```bash
docker ps
```

## List All Containers

```bash
docker ps -a
```

## Stop a Container

```bash
docker stop my-nginx
```

## Start a Container

```bash
docker start my-nginx
```

## Restart a Container

```bash
docker restart my-nginx
```

## Remove a Container

```bash
docker rm my-nginx
```

## Remove an Image

```bash
docker rmi nginx
```

---



# Summary

Docker Hub provides a centralized platform for storing and sharing Docker images. By pulling images from Docker Hub and using port binding, applications can be quickly deployed and accessed from a local machine or a cloud server. Understanding Docker images and port mapping is essential for building and deploying containerized applications.

# Training Diary – Creating and Publishing Docker Images

**Date:** 01/07/2026

## Today I Learned

- Creating a custom Docker image
- Writing a Dockerfile in Visual Studio Code
- Building an image using Docker
- Running a container from the custom image
- Tagging a Docker image
- Pushing a Docker image to Docker Hub

---

## Training Notes

![Day 8 Notes](images/day8-notes.jpg)

---

# What is a Docker Image?

A Docker Image is a read-only template that contains everything required to run an application, including:

- Application source code
- Runtime environment
- Libraries
- Dependencies
- Configuration files

Images are used to create Docker containers.

---

# What is a Dockerfile?

A **Dockerfile** is a text file containing a set of instructions that Docker uses to automatically build an image.

Common Dockerfile Instructions:

| Instruction | Purpose |
|-------------|---------|
| `FROM` | Specifies the base image |
| `WORKDIR` | Sets the working directory |
| `COPY` | Copies files into the image |
| `RUN` | Executes commands while building the image |
| `EXPOSE` | Exposes a container port |
| `CMD` | Specifies the default command to run |

---

# Creating a Dockerfile in VS Code

### Step 1

Open **Visual Studio Code**.

### Step 2

Create a new project folder.

Example:

```text
docker-demo
```

### Step 3

Inside the folder, create:

```text
Dockerfile
```

Example Dockerfile:

```dockerfile
FROM nginx:latest

COPY . /usr/share/nginx/html

EXPOSE 80
```

Save the file.

---

# Building a Docker Image

Open the terminal inside VS Code and navigate to the project folder.

Run:

```bash
docker build -t my-nginx-image .
```

Explanation:

- `docker build` → Builds the image
- `-t` → Assigns a name (tag)
- `.` → Uses the current directory as the build context

---

# Checking Available Images

```bash
docker images
```

This command lists all Docker images available on your system.

---

# Running the Custom Image

Run the image as a container:

```bash
docker run -d -p 8080:80 --name mycontainer my-nginx-image
```

Explanation:

- `-d` → Detached mode
- `-p` → Port binding
- `--name` → Assign container name
- `my-nginx-image` → Image name

---

# Testing the Application

Open a browser and visit:

```text
http://localhost:8080
```

If running on AWS EC2:

```text
http://<Public-IP>:8080
```

The application should load successfully.

---

# Creating a Docker Hub Repository

### Step 1

Login to Docker Hub.

### Step 2

Click:

```text
Create Repository
```

### Step 3

Enter:

- Repository Name
- Visibility (Public or Private)

Example:

```text
username/my-nginx-image
```

---

# Login to Docker Hub from Terminal

```bash
docker login
```

Enter your:

- Docker Hub Username
- Password

---

# Tagging an Image

Before pushing an image to Docker Hub, it must be tagged.

Syntax:

```bash
docker tag <local-image> <dockerhub-username>/<repository-name>:latest
```

Example:

```bash
docker tag my-nginx-image username/my-nginx-image:latest
```

---

# Pushing an Image to Docker Hub

Upload the image:

```bash
docker push username/my-nginx-image:latest
```

Docker uploads the image layers to your Docker Hub repository.

---

# Verifying the Upload

Visit your Docker Hub account.

Open your repository.

The uploaded image will now be visible.

---

# Complete Docker Workflow

```text
Create Project
      │
      ▼
Create Dockerfile
      │
      ▼
Build Docker Image
      │
      ▼
Run Docker Container
      │
      ▼
Test Application
      │
      ▼
Tag Docker Image
      │
      ▼
Login to Docker Hub
      │
      ▼
Push Image
      │
      ▼
Image Available on Docker Hub
```

---

# Important Docker Commands

Build Image

```bash
docker build -t myimage .
```

List Images

```bash
docker images
```

Run Container

```bash
docker run -d -p 8080:80 myimage
```

Login to Docker Hub

```bash
docker login
```

Tag Image

```bash
docker tag myimage username/myimage:latest
```

Push Image

```bash
docker push username/myimage:latest
```

Pull Image

```bash
docker pull username/my

# Summary

Dockerfiles automate the process of creating Docker images, ensuring consistent application environments. By building images locally and publishing them to Docker Hub, developers can easily share and deploy applications across different systems, making Docker an essential tool for modern software development and DevOps.


# Day 9 Training Diary – Docker Volumes & Dockerizing a React Project

**Date:** 02/07/2026

## Today I Learned

- Introduction to Docker Volumes
- Why Docker Volumes are used
- Creating and managing Docker Volumes
- Dockerizing a React application
- Creating a Dockerfile for a React project
- Using a `.dockerignore` file
- Building and running a Docker image for a React application

---



# Docker Volumes

Docker Volumes are used to store data outside the Docker container. They allow data to persist even if a container is stopped or deleted.

Volumes are managed by Docker and are the recommended way to store persistent application data.

## Advantages of Docker Volumes

- Persistent data storage
- Data is not lost when containers are removed
- Easy data sharing between containers
- Better performance than bind mounts
- Easy backup and restore

---

# Why Use Docker Volumes?

Without volumes:

- Container data is deleted when the container is removed.

With volumes:

- Data remains safely stored.
- New containers can reuse the same data.

Example:

```text
Container
      │
      ▼
Docker Volume
      │
Persistent Data
```

---

# Basic Docker Volume Commands

## Create a Volume

```bash
docker volume create myvolume
```

## List All Volumes

```bash
docker volume ls
```

## Inspect a Volume

```bash
docker volume inspect myvolume
```

## Remove a Volume

```bash
docker volume rm myvolume
```

## Run a Container with a Volume

```bash
docker run -d -v myvolume:/app/data nginx
```

Here,

- `myvolume` → Docker volume
- `/app/data` → Directory inside the container

---

# Dockerizing a React Project

Dockerizing means packaging a React application into a Docker image so that it can run consistently on any system.

---

# Steps to Dockerize a React Application

### Step 1

Create a React application.

```bash
npx create-react-app my-react-app
```

### Step 2

Open the project in Visual Studio Code.

### Step 3

Create a file named:

```text
Dockerfile
```

inside the project folder.

---

# Sample Dockerfile

```dockerfile
FROM node:18

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm","start"]
```

### Explanation

- `FROM` → Base image
- `WORKDIR` → Working directory
- `COPY` → Copies project files
- `RUN` → Installs dependencies
- `EXPOSE` → Opens port 3000
- `CMD` → Starts the React application

---

# Creating a .dockerignore File

A `.dockerignore` file tells Docker which files and folders should not be copied into the image.

Example:

```text
node_modules
.git
.gitignore
README.md
```

## Benefits

- Smaller image size
- Faster build process
- Cleaner Docker image
- Improved security

---

# Build the Docker Image

Navigate to the project directory and run:

```bash
docker build -t react-app .
```

---

# Verify the Image

```bash
docker images
```

---

# Run the React Container

```bash
docker run -d -p 3000:3000 --name react-container react-app
```

Explanation:

- `-d` → Run in background
- `-p 3000:3000` → Port binding
- `--name` → Container name
- `react-app` → Image name

---

# Access the React Application

Open your browser and visit:

```text
http://localhost:3000
```

If using an AWS EC2 instance:

```text
http://<EC2-Public-IP>:3000
```

Ensure port **3000** is allowed in the EC2 Security Group.

---

# Useful Docker Commands

Build Image

```bash
docker build -t react-app .
```

Run Container

```bash
docker run -d -p 3000:3000 react-app
```

View Running Containers

```bash
docker ps
```

Stop Container

```bash
docker stop react-container
```

Start Container

```bash
docker start react-container
```

Remove Container

```bash
docker rm react-container
```

---


# Summary

Docker Volumes provide persistent storage for containerized applications, while Dockerizing a React project ensures that the application runs consistently across different environments. Using a Dockerfile and `.dockerignore` simplifies application deployment and follows best practices for containerized development.


# Training Diary – AWS CloudWatch & Weekly Revision

**Date:** 03/07/2026

## Today I Learned

- Introduction to Amazon CloudWatch
- Features of CloudWatch
- Monitoring AWS resources
- CloudWatch Metrics, Logs, and Alarms
- Creating CloudWatch Alarms
- Revision of Docker and AWS concepts covered during the week

---

# Amazon CloudWatch

Amazon CloudWatch is a monitoring and observability service provided by AWS. It helps monitor AWS resources, applications, and infrastructure by collecting metrics, logs, and events in real time.

CloudWatch allows users to monitor the health and performance of AWS services and receive alerts whenever predefined conditions are met.

---

# Features of CloudWatch

- Real-time monitoring
- Collects performance metrics
- Stores application logs
- Creates alarms and notifications
- Dashboard visualization
- Event monitoring
- Integration with AWS services

---

# CloudWatch Components

## 1. Metrics

Metrics are numerical data collected over time to measure the performance of AWS resources.

Examples:

- CPU Utilization
- Network In
- Network Out
- Disk Read/Write Operations
- Memory Usage (using CloudWatch Agent)

---

## 2. Logs

CloudWatch Logs store log files generated by applications and AWS services.

Examples:

- EC2 system logs
- Application logs
- Lambda logs
- Web server logs

Benefits:

- Easier troubleshooting
- Centralized log management
- Performance analysis

---

## 3. CloudWatch Alarms

CloudWatch Alarms monitor metrics and perform actions when thresholds are reached.

Example:

If CPU Utilization becomes greater than **80%**, CloudWatch can:

- Send an email notification
- Trigger an Auto Scaling action
- Invoke an AWS Lambda function

---

# Steps to Create a CloudWatch Alarm

### Step 1

Open the AWS Management Console.

### Step 2

Search for:

```text
CloudWatch
```

### Step 3

Select:

```text
Alarms → Create Alarm
```

### Step 4

Choose the metric to monitor.

Example:

```text
EC2 → CPU Utilization
```

### Step 5

Set the threshold.

Example:

```text
CPU Utilization > 80%
```

### Step 6

Configure notification using Amazon SNS (Simple Notification Service).

### Step 7

Review the settings and click **Create Alarm**.

---

# Benefits of CloudWatch

- Monitors resource health
- Detects performance issues
- Sends automatic alerts
- Helps reduce downtime
- Improves application reliability
- Supports automated actions

---

# Weekly Revision

## AWS Services Revised

- IAM
- EC2
- S3
- VPC
- CloudWatch

### Important AWS Concepts

- Cloud Computing
- IAM Users and Groups
- Security Groups
- EC2 Instance Creation
- S3 Buckets and Static Website Hosting
- Storage Classes
- Lifecycle Configuration
- VPC Components
- Internet Gateway
- NAT Gateway
- Route Tables
- Network ACL
- CloudWatch Metrics and Alarms

---

## Docker Revision

### Topics Revised

- Docker Installation
- Docker Images
- Docker Containers
- Docker Hub
- Port Binding
- Dockerfile
- Docker Volumes
- Dockerizing a React Application
- `.dockerignore` File

### Important Docker Commands

```bash
docker images
docker ps
docker ps -a
docker pull nginx
docker run -d -p 8080:80 nginx
docker build -t myimage .
docker stop <container-name>
docker start <container-name>
docker rm <container-name>
docker volume ls
docker volume create myvolume
docker push username/myimage
```

---



# Summary

Amazon CloudWatch is an essential AWS monitoring service that helps track resource performance, collect logs, and generate alerts. The revision session reinforced key concepts from AWS and Docker, providing a solid understanding of cloud infrastructure, monitoring, and containerized application deployment.


# Training Diary – Connecting to EC2 & Installing Web Servers

**Date:** 06/07/2026

## Today I Learned

- Connecting to an AWS EC2 instance using terminal commands
- Secure Shell (SSH) connection
- Introduction to Web Servers
- Apache Web Server
- Nginx Web Server
- Installing Apache on an EC2 instance
- Basic Linux package management commands

---



# Connecting to an EC2 Instance

An EC2 instance can be accessed remotely using SSH (Secure Shell). SSH provides a secure encrypted connection between the local machine and the EC2 instance.

## Prerequisites

- Running EC2 instance
- Public IPv4 Address
- Key Pair (.pem file)
- Port **22 (SSH)** allowed in the Security Group

---

# Connecting Using SSH

Syntax:

```bash
ssh -i <key-name>.pem ubuntu@<public-ip>
```

Example:

```bash
ssh -i mykey.pem ubuntu@13.234.56.78
```

For Amazon Linux:

```bash
ssh -i mykey.pem ec2-user@13.234.56.78
```

---

# Basic Commands After Login

Update package list:

```bash
sudo apt update
```

Upgrade installed packages:

```bash
sudo apt upgrade -y
```

Check current directory:

```bash
pwd
```

List files:

```bash
ls
```

Display current user:

```bash
whoami
```

---

# Web Servers

A web server is software that stores and delivers web pages to users through a web browser using the HTTP or HTTPS protocol.

Popular web servers include:

- Apache HTTP Server
- Nginx

---

# Apache Web Server

Apache is one of the world's most widely used open-source web servers. It is known for its flexibility, reliability, and support for multiple programming languages.

### Features

- Open source
- Cross-platform
- Supports HTTP and HTTPS
- Easy to configure
- Supports modules and extensions

### Install Apache

```bash
sudo apt install apache2 -y
```

### Start Apache

```bash
sudo systemctl start apache2
```

### Enable Apache at Boot

```bash
sudo systemctl enable apache2
```

### Check Apache Status

```bash
sudo systemctl status apache2
```

---

# Nginx Web Server

Nginx is a high-performance web server and reverse proxy server. It is lightweight and capable of handling a large number of simultaneous connections.

### Features

- High performance
- Low memory usage
- Reverse proxy support
- Load balancing
- Fast request handling

### Install Nginx

```bash
sudo apt install nginx -y
```

### Start Nginx

```bash
sudo systemctl start nginx
```

### Enable Nginx

```bash
sudo systemctl enable nginx
```

### Check Nginx Status

```bash
sudo systemctl status nginx
```

---

# Accessing the Web Server

After installing Apache or Nginx:

1. Ensure the EC2 Security Group allows **HTTP (Port 80)**.
2. Copy the Public IPv4 Address of the EC2 instance.
3. Open a web browser.
4. Visit:

```text
http://<EC2-Public-IP>
```

If the installation is successful, the default Apache or Nginx welcome page will be displayed.

---

# Apache vs Nginx

| Apache | Nginx |
|---------|--------|
| Process-based architecture | Event-driven architecture |
| Easy to configure | High performance |
| Good for dynamic websites | Excellent for static content |
| Higher memory usage | Lower memory usage |

---



# Summary

Connecting to an EC2 instance through SSH is an essential skill for managing cloud servers. Installing web servers such as Apache and Nginx enables hosting websites and web applications. Understanding package management and web server configuration forms the foundation of deploying applications on AWS.


# Training Diary – Amazon EBS (Elastic Block Store)

**Date:** 07/07/2026

## Today I Learned

- Introduction to Amazon EBS (Elastic Block Store)
- Features and advantages of EBS
- Types of EBS Volumes
- Creating and attaching an EBS volume
- Mounting an EBS volume on an EC2 instance
- Snapshots and backups
- Difference between EBS and S3

---



# Amazon EBS (Elastic Block Store)

Amazon Elastic Block Store (EBS) is a block-level storage service provided by AWS. It is mainly used with Amazon EC2 instances to provide persistent storage for applications and operating systems.

Unlike instance storage, data stored in an EBS volume remains available even if the EC2 instance is stopped.

---

# Features of Amazon EBS

- Persistent block storage
- High availability
- High performance
- Data encryption support
- Backup using snapshots
- Scalable storage capacity
- Can be attached and detached from EC2 instances

---

# Why Use Amazon EBS?

Amazon EBS is used for:

- Operating system storage
- Databases
- File systems
- Enterprise applications
- Boot volumes
- Backup storage

---

# Types of EBS Volumes

| Volume Type | Use Case |
|--------------|----------|
| General Purpose SSD (gp3/gp2) | Most applications |
| Provisioned IOPS SSD (io1/io2) | High-performance databases |
| Throughput Optimized HDD (st1) | Big data and log processing |
| Cold HDD (sc1) | Infrequently accessed data |

---

# Steps to Create an EBS Volume

### Step 1

Open the AWS Management Console.

### Step 2

Search for:

```text
Elastic Block Store (EBS)
```

### Step 3

Select:

```text
Volumes → Create Volume
```

### Step 4

Configure:

- Volume Type
- Size
- Availability Zone

Example:

```text
Volume Type : gp3
Size : 10 GB
Availability Zone : ap-south-1a
```

### Step 5

Click:

```text
Create Volume
```

---

# Attaching an EBS Volume

1. Select the created volume.
2. Click **Actions**.
3. Choose **Attach Volume**.
4. Select the EC2 instance.
5. Specify the device name (for example `/dev/xvdf`).
6. Click **Attach**.

The volume is now connected to the EC2 instance.

---

# Mounting the EBS Volume

After connecting to the EC2 instance through SSH:

Check available disks:

```bash
lsblk
```

Create a file system:

```bash
sudo mkfs -t ext4 /dev/xvdf
```

Create a mount directory:

```bash
sudo mkdir /data
```

Mount the volume:

```bash
sudo mount /dev/xvdf /data
```

Verify the mounted volume:

```bash
df -h
```

---

# Amazon EBS Snapshots

A snapshot is a backup of an EBS volume stored in Amazon S3.

Snapshots are used for:

- Backup
- Disaster recovery
- Restoring data
- Creating new EBS volumes

### Steps to Create a Snapshot

1. Open **EBS Volumes**.
2. Select the volume.
3. Click **Actions**.
4. Choose **Create Snapshot**.
5. Enter a description.
6. Click **Create Snapshot**.

---

# Advantages of EBS

- Persistent storage
- Reliable performance
- Data encryption
- Easy backup using snapshots
- Flexible storage sizes
- Supports high-performance workloads

---

# Amazon EBS vs Amazon S3

| Amazon EBS | Amazon S3 |
|------------|-----------|
| Block Storage | Object Storage |
| Attached to EC2 | Accessible over the Internet |
| Low latency | Highly scalable storage |
| Used as disk storage | Used for storing files and objects |
| Suitable for operating systems and databases | Suitable for backups, media files, and static websites |

---

# Best Practices

- Take regular snapshots for backup.
- Encrypt sensitive EBS volumes.
- Delete unused volumes to reduce costs.
- Use SSD volumes for high-performance applications.
- Monitor EBS performance using Amazon CloudWatch.

---



# Summary

Amazon EBS is a reliable and scalable block storage service designed for Amazon EC2. It provides persistent storage, supports snapshots for backup and recovery, and is ideal for applications that require low-latency and high-performance storage such as databases, operating systems, and enterprise applications.

