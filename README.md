# Daily-Diary-TRCS-103
# Day 1 – Introduction to Cloud Computing & AWS
**Date: 22/06/2026**
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

 # Advantages of Cloud Computing
 - Pay-as-you-go pricing
- High scalability
- Global accessibility
- Automatic updates
- Better disaster recovery
- Reduced infrastructure costs

  
# Cloud Service Models
# IaaS (Infrastructure as a Service)
Provides virtual machines, storage, networking, and other infrastructure resources.

**Examples:**
- Amazon EC2
- Microsoft Azure VM
- Google Compute 

 # PaaS (Platform as a Service)
 Provides a platform for developers to build, test, and deploy applications.
 
 **Examples:**
- AWS Elastic Beanstalk
- Google App Engine
- Heroku

# SaaS (Software as a Service)
Provides software applications through the internet.

**Examples:**
- Spotify
- Gmail
- Microsoft 365
- Google Docs

# Introduction to AWS
Amazon Web Services (AWS) is Amazon's cloud computing platform that provides more than 200 cloud services across computing, storage, networking, databases, analytics, machine learning, and security.

AWS is one of the most widely used cloud platforms because of its scalability, reliability, global reach, and pay-as-you-go pricing model.

# Benefits of AWS
- Global infrastructure
- High availability
- Enhanced security
- Cost optimization
- Elastic scalability
- Large service ecosystem

# Popular AWS Services

|Service   |     Purpose| 
|----------|-----------------|
|EC2	|Virtual Servers|
|S3|	Object Storage|
|IAM|	Identity and Access Management|
|RDS	|Managed Databases|
|VPC	|Virtual Private Cloud|
|Lambda|	Serverless Computing|
|CloudWatch|Monitoring and Logging|

# Steps to Create an AWS Account
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

## IAM (Identity and Access Management)
IAM is an AWS service used to manage users, groups, roles, and permissions securely.

# Features
- User Management
- Group Management
- Role-Based Access Control
- Permission Policies
- MFA Support
## MFA (Multi-Factor Authentication)
MFA adds an additional security layer by requiring users to verify their identity using a second authentication method such as:

- Authenticator App
- SMS OTP
- Hardware Security Key
 
# Benefits of MFA
- Improved account security
- Protection against password theft
- Reduced unauthorized access
