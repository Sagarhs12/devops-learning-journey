🚀 Day 4 – Jenkins Installation & First CI Job
📌 Objective

The objective of Day 4 was to install Jenkins on AWS EC2, configure it properly, and create the first Continuous Integration (CI) job connected to a GitHub repository.

🔹 What is Jenkins?

Jenkins is an open-source automation server used to:

Automate builds

Run tests

Enable Continuous Integration (CI)

Support CI/CD pipelines

It helps developers detect issues early by automatically building and testing code whenever changes are pushed.

🔹 Why Jenkins in DevOps?

Automates repetitive tasks

Integrates with GitHub, Docker, AWS, etc.

Supports pipelines as code

Improves software delivery speed and reliability

🔹 Jenkins Installation on AWS EC2 (Hands-On)
Step 1: Update System
sudo yum update -y

Step 2: Install Java (Jenkins Requirement)
sudo yum install java-17-amazon-corretto -y
java -version

Step 3: Add Jenkins Repository
sudo wget -O /etc/yum.repos.d/jenkins.repo \
https://pkg.jenkins.io/redhat-stable/jenkins.repo

sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key

Step 4: Install Jenkins
sudo yum install jenkins -y

Step 5: Start & Enable Jenkins
sudo systemctl start jenkins
sudo systemctl enable jenkins
sudo systemctl status jenkins

🔹 Accessing Jenkins UI
Jenkins URL:
http://<EC2-PUBLIC-IP>:8080

Open Port:

Security Group → Inbound rule → Allow TCP 8080

🔹 Unlock Jenkins
Get Initial Admin Password:
sudo cat /var/lib/jenkins/secrets/initialAdminPassword

Steps:

Paste password in browser

Install suggested plugins

Create Admin User

🔹 Jenkins Initial Configuration

Created Admin user

Set Jenkins URL

Completed setup wizard successfully

🔹 First Jenkins CI Job (Freestyle Project)
Job Details:

Job Name: devops-learning-journey-ci

Job Type: Freestyle Project

Source Control: Git

Repository URL:

https://github.com/Sagarhs12/devops-learning-journey.git


Branch: main

🔹 Build Configuration

Enabled Git SCM

No credentials required (public repo)

Manual trigger using Build Now

🔹 First Build Execution

Jenkins successfully cloned the repository

Build executed without errors

Console Output verified

🔹 Issues Faced & Solutions
❌ Jenkins Built-In Node Offline

Reason:
Low /tmp disk space (below Jenkins threshold)

Solution:
Configured Jenkins to use a custom temp directory:

/var/lib/jenkins/tmp


Restarted Jenkins and brought node online successfully.

❌ Build Stuck in Queue

Reason:
Executor offline due to disk safety checks

Solution:
Cleaned temp files and restarted Jenkins service

✅ Key Learnings

Jenkins architecture basics

Java dependency for Jenkins

Jenkins service management

Security group configuration

CI job creation

Troubleshooting Jenkins node issues

🎯 Outcome

By the end of Day 4:

Jenkins was fully installed and running

Admin user configured

First CI job created and executed successfully

Jenkins environment prepared for automation
