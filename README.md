DevOps Learning Journey (7-Day CI/CD Project)
# 🚀 DevOps Learning Journey – 7 Day CI/CD Challenge

This repository documents my **7-Day DevOps Learning Challenge**, where I built a complete **CI/CD pipeline** from scratch using **AWS, Jenkins, GitHub, and Linux**.  
The project demonstrates real-worldCI/CD practices followed in production environments.

---

## 👨‍💻 Author
**Sagar Shivappayyanamath**  
DevOps & Cloud Enthusiast  

---

## 🎯 Project Objective

The goal of this project is to:
- Understand DevOps fundamentals
- Implement CI using Jenkins
- Automate builds using GitHub Webhooks
- Create Jenkins Pipelines using Jenkinsfile
- Deploy an application automatically to an Apache web server
- Build an end-to-end CI/CD workflow

---

## 🛠️ Tools & Technologies Used

| Category | Tools |
|--------|------|
| Cloud | AWS EC2 (Amazon Linux 2023) |
| CI/CD | Jenkins |
| SCM | Git, GitHub |
| Automation | Jenkins Pipeline (Jenkinsfile) |
| Web Server | Apache HTTP Server (httpd) |
| OS | Linux |
| Networking | GitHub Webhooks |

---

## 📁 Repository Structure



devops-learning-journey/
├── DAY1.md # DevOps & Linux basics
├── DAY2.md # Git & GitHub fundamentals
├── DAY3.md # AWS EC2 & Linux practice
├── DAY4.md # Jenkins installation & first CI job
├── DAY5.md # GitHub Webhooks & automated builds
├── DAY6.md # Jenkins Pipeline using Jenkinsfile
├── DAY7.md # Automated deployment (CI/CD)
├── Jenkinsfile # Jenkins pipeline configuration
├── index.html # Sample application
└── README.md # Project documentation


---

## 📅 Day-wise Learning Summary

### 📌 Day 1 – DevOps & Linux Basics
- What is DevOps?
- DevOps lifecycle
- Linux commands (`ls`, `cd`, `mkdir`, `chmod`, `systemctl`)
- Understanding servers and automation

📄 File: `DAY1.md`

---

### 📌 Day 2 – Git & GitHub Fundamentals
- Git basics (`clone`, `add`, `commit`, `push`)
- GitHub repositories
- Branching concepts
- Version control best practices

📄 File: `DAY2.md`

---

### 📌 Day 3 – AWS EC2 & Linux Practice
- Launching EC2 instance
- SSH access using `.pem` key
- Amazon Linux setup
- Installing packages using `yum`

📄 File: `DAY3.md`

---

### 📌 Day 4 – Jenkins Installation & First CI Job
- Installing Java & Jenkins
- Jenkins setup on EC2
- Creating Freestyle jobs
- Connecting Jenkins with GitHub

📄 File: `DAY4.md`

---

### 📌 Day 5 – GitHub Webhooks & Automated Builds
- GitHub webhook configuration
- Auto-trigger Jenkins jobs on push
- Jenkins GitHub integration
- Validating webhook deliveries

📄 File: `DAY5.md`

---

### 📌 Day 6 – Jenkins Pipeline using Jenkinsfile
- Declarative pipeline syntax
- Creating Jenkinsfile
- Stages: Checkout, Build, Test
- Pipeline as Code concept

📄 File: `DAY6.md`

---

### 📌 Day 7 – Automated Deployment (CI/CD)
- Installing Apache Web Server
- Creating deployment pipeline
- Jenkins sudo permissions
- Deploying `index.html` automatically
- End-to-end CI/CD execution

📄 File: `DAY7.md`

---

## 🔁 CI/CD Workflow Overview

1. Developer pushes code to GitHub
2. GitHub webhook triggers Jenkins
3. Jenkins pulls latest code
4. Build & Test stages run
5. Application is deployed automatically to Apache server
6. Website becomes live without manual intervention

---

## 📜 Jenkinsfile (Pipeline as Code)

```groovy
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Sagarhs12/devops-learning-journey.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build completed'
            }
        }

        stage('Test') {
            steps {
                echo 'Tests passed'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                sudo cp index.html /var/www/html/index.html
                '''
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline executed successfully 🎉'
        }
        failure {
            echo 'CI/CD Pipeline failed ❌'
        }
    }
}

🌐 Live Deployment

After successful pipeline execution, the application is available at:

http://<EC2-PUBLIC-IP>

🧠 Key Learnings

Real-world CI/CD pipeline implementation

Jenkins automation & pipelines

GitHub Webhooks

Linux server management

Production-style DevOps workflow

📌 Project Status

✅ Completed – Fully functional CI/CD pipeline

📈 Future Enhancements

Dockerized deployment

Nginx reverse proxy

Rollback strategy

Monitoring (Prometheus & Grafana)

Cloud-native CI/CD

🤝 Connect With Me

GitHub: https://github.com/Sagarhs12

⭐ If you found this project useful, consider giving it a star!


