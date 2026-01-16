.

🚀 Day 3 – AWS EC2 & Linux Server Basics
📌 Objective

The objective of Day 3 was to understand cloud computing fundamentals, launch an AWS EC2 instance, and gain hands-on experience with Linux server basics, which are core skills for DevOps engineers.

🔹 What is Cloud Computing?

Cloud computing allows users to access computing resources like servers, storage, and networking over the internet on a pay-as-you-go basis.

Benefits:

Scalability

Cost efficiency

High availability

On-demand resources

🔹 What is AWS?

Amazon Web Services (AWS) is a leading cloud platform offering services such as:

Compute

Storage

Networking

Databases

DevOps & CI/CD tools

🔹 What is EC2?

Amazon EC2 (Elastic Compute Cloud) provides resizable virtual servers in the cloud.

Key EC2 Concepts:

Instance – Virtual server

AMI – Amazon Machine Image (OS template)

Instance Type – Hardware configuration (CPU, RAM)

Key Pair – Used for secure SSH login

Security Group – Virtual firewall

🔹 EC2 Instance Setup (Hands-On)
Steps Followed:

Logged into AWS Management Console

Navigated to EC2 Dashboard

Launched a new EC2 instance

Selected Amazon Linux 2023 AMI

Chose instance type: t2.micro / t3.micro

Created and downloaded a key pair (.pem)

Configured Security Group

SSH (22) – My IP

HTTP (80) – 0.0.0.0/0

Launched the instance successfully

🔹 Connecting to EC2 via SSH
Key Permissions:
chmod 400 devops-key.pem

SSH Command:
ssh -i devops-key.pem ec2-user@<EC2-PUBLIC-IP>

🔹 Linux Basics Learned
📁 Directory Commands
pwd        # Print working directory
ls         # List files
ls -la     # Detailed list
cd folder  # Change directory
mkdir dir  # Create directory

📄 File Commands
touch file.txt
cat file.txt
nano file.txt
rm file.txt

👤 User & Permission Commands
whoami
sudo command
chmod 400 file.pem

📊 System Commands
df -h      # Disk usage
free -m    # Memory usage
top        # Running processes
uptime

🔹 Package Management (Amazon Linux)
sudo yum update -y
sudo yum install git -y
sudo yum install java -y

🔹 Networking Basics

Public IP vs Private IP

Security Groups act as firewalls

Port 22 → SSH

Port 80 → HTTP

Port 8080 → Jenkins

🔹 Issues Faced & Solutions

❌ SSH permission denied
✅ Fixed using correct .pem file and permissions

❌ Timeout issue
✅ Updated inbound rules in security group

❌ Git not found
✅ Installed Git using yum

✅ Key Learnings

How cloud servers work

EC2 instance lifecycle (start, stop, terminate)

Secure SSH access

Basic Linux command usage

Importance of security groups

Server preparation for DevOps tools

🎯 Outcome

By the end of Day 3, I successfully launched an EC2 instance, connected via SSH, and managed the server using Linux commands—preparing the environment for Jenkins and CI/CD.
