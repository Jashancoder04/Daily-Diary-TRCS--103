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


## Step 4: Create a Key Pair 
Click Create New Key Pair and enter:

- Key Pair Name: MyKey
- Key Pair Type: RSA
- File Format: .pem

⬇️ Download the .pem file and keep it safe.

Important: Without this key, you cannot securely connect to your EC2 instance.

## Step 5: Configure Network & Security 
**Network Settings**
Choose:
- VPC
- Subnet
- Enable Auto-Assign Public IP (if internet access is required)

**Security Groups (Virtual Firewall)**
Security Groups control who can access your EC2 instance.

| **Rule** | **Protocol** | **Port** | **Purpose**           |
| -------- | ------------ | -------- | --------------------- |
| SSH      | TCP          | 22       | Secure Remote Login   |
| HTTP     | TCP          | 80       | Website Access        |
| HTTPS    | TCP          | 443      | Secure Website Access |

Example Security Group Rules
-  SSH (Port 22) → My IP
-  HTTP (Port 80) → Anywhere
-  HTTPS (Port 443) → Anywhere


## Step 6: Configure Storage 
Choose the storage size.

**Example:**

- 8 GB General Purpose SSD (gp3)

You can increase the storage later if needed.

## Step 7: Review & Launch 
Review all your settings.

Click:

**Launch Instance**

AWS will create and start your virtual server in a few seconds.

# Instance States
| **State**      | **Short Meaning**   |
| -------------- | ------------------- |
| **Pending**    | Starting up         |
| **Running**    | Active and usable   |
| **Stopping**   | Shutting down       |
| **Stopped**    | Powered off         |
| **Terminated** | Permanently deleted |

# Connecting to the EC2 Instance
## Using EC2 Instance Connect (Browser)
1.Open EC2 Dashboard.
2.Select the running instance.
3.Click Connect.
4.Choose EC2 Instance Connect.
5.Click Connect again.
A browser-based terminal opens.

# Hosting a Web Page on EC2
After connecting to the instance:

**Update Packages**
sudo yum update -y

**Install Apache Web Server**
sudo yum install httpd -y

**Start Apache**
sudo systemctl start httpd

**Enable Apache at Boot**
sudo systemctl enable httpd

**Create Sample Web Page**
echo "<h1>Hello from AWS EC2</h1>" | sudo tee /var/www/html/index.html

# Running the Website on Web Browser
1.Ensure HTTP (Port 80) is allowed in Security Group.
2.Copy the Public IPv4 Address of the instance.
3.Open browser and enter:
http://Public-IP
Example:

http://54.123.45.67
The webpage should display:

Hello from AWS EC2

# Monitoring EC2
AWS provides monitoring through CloudWatch.

Metrics include:

- CPU Utilization
- Network Traffic
- Disk Usage
- Instance Health




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

my-training-bucket
## Object
An object is a file stored inside a bucket.

Examples:

- Images
- Videos
- Documents
- HTML files
- PDFs

# Steps to Create an Amazon S3 Bucket
**Step 1: Login to AWS**
- Open the AWS Management Console.
- Search for S3 and open it.

**Step 2: Create Bucket**
- Click Create Bucket.

**Step 3: Enter Bucket Details**
- Bucket Name: my-first-bucket
- Region: Select your preferred AWS Region (e.g., Mumbai).

**Step 4: Configure Settings**
- Keep Block Public Access enabled.
- Leave other settings as default (or change if needed).

**Step 5: Review**
- Check all the bucket details.

 **Step 6: Create Bucket**
- Click Create Bucket.

As Your Amazon S3 bucket is now ready to store files.

# Upload Files to Amazon S3 (Easy Format)
**Step 1: Login to AWS**
- Open the AWS Management Console.
- Search for S3 and open it.

**Step 2: Open Your Bucket**
- Click on the bucket name where you want to upload files.

**Step 3: Click Upload**
- Click the Upload button.

**Step 4: Add Files**
- Click Add Files or Add Folder.
- Select the file(s) from your computer.

**Step 5: Review**
- Check the selected files and keep the default settings (or change if needed).

**Step 6: Upload**
- Click Upload.

 Your files are now stored in the Amazon S3 bucket.

# Hosting a Static Website Using S3
Amazon S3 can host static websites containing:
- HTML
- CSS
- JavaScript
- Images

**Step 1**
- Create a bucket.

**Step 2**
- Upload website files.

Example:

index.html
style.css
images/

**Step 3**
Enable Static Website Hosting

Navigate to:

Properties → Static Website Hosting
Select:

Enable
Specify:


**Step 4**
Configure Bucket Permissions

Disable Block Public Access (if required).

Add Bucket Policy to allow public read access.

**Step 5**
Open Website Endpoint

AWS generates a website URL:

http://bucket-name.s3-website-region.amazonaws.com
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

