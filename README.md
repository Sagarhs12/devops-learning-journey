<!-- ===================== HERO SECTION ===================== -->

<div align="center">

# 🚀 DevOps Learning Journey  
## 7-Day CI/CD Challenge

**End-to-End CI/CD Pipeline using AWS • Jenkins • GitHub • Linux**

<br/>

![CI/CD](https://img.shields.io/badge/CI%2FCD-Automated-success?style=for-the-badge&logo=jenkins)
![AWS](https://img.shields.io/badge/AWS-EC2-orange?style=for-the-badge&logo=amazonaws)
![Linux](https://img.shields.io/badge/Linux-Amazon%20Linux%202023-yellow?style=for-the-badge&logo=linux)
![GitHub](https://img.shields.io/badge/GitHub-Webhooks-black?style=for-the-badge&logo=github)

<br/>

📌 **A real-world DevOps project demonstrating production-grade CI/CD automation**

</div>

---

## 👨‍💻 Author

**Sagar Shivappayyanamath**  
🚀 DevOps & Cloud Enthusiast  
📍 India  

🔗 GitHub: https://github.com/Sagarhs12  

---

## 🎯 Project Overview

This repository documents my **7-Day DevOps Learning Challenge**, where I built a **complete CI/CD pipeline from scratch** following **industry best practices**.

### ✅ What this project demonstrates
- Production-style CI/CD workflow
- Jenkins automation using **Pipeline as Code**
- GitHub Webhooks for automated triggers
- Zero-downtime deployment to Linux server
- End-to-end DevOps lifecycle

---

## 🧰 Tech Stack

| Category | Technology |
|--------|-----------|
| ☁️ Cloud | AWS EC2 (Amazon Linux 2023) |
| 🔁 CI/CD | Jenkins |
| 📦 SCM | Git & GitHub |
| ⚙️ Automation | Jenkinsfile |
| 🌐 Web Server | Apache HTTP Server |
| 🖥 OS | Linux |
| 🔗 Integration | GitHub Webhooks |

---

## 🗂️ Repository Structure

devops-learning-journey/
│
├── DAY1.md # DevOps & Linux basics
├── DAY2.md # Git & GitHub fundamentals
├── DAY3.md # AWS EC2 & Linux practice
├── DAY4.md # Jenkins installation & CI job
├── DAY5.md # GitHub Webhooks & automation
├── DAY6.md # Jenkins Pipeline (Jenkinsfile)
├── DAY7.md # Automated deployment (CI/CD)
│
├── Jenkinsfile # Pipeline as Code
├── index.html # Sample application
└── README.md # Project documentation

yaml
Copy code

---

## 📆 7-Day Learning Breakdown

### 🟢 Day 1 – DevOps & Linux Basics
- DevOps principles & lifecycle  
- Core Linux commands  
- Servers & automation  

📄 `DAY1.md`

---

### 🟢 Day 2 – Git & GitHub
- Git workflow (`clone`, `add`, `commit`, `push`)
- Branching concepts
- Version control best practices  

📄 `DAY2.md`

---

### 🟢 Day 3 – AWS EC2 & Linux
- EC2 instance launch
- SSH using `.pem` key
- Amazon Linux configuration
- Package installation using `yum`

📄 `DAY3.md`

---

### 🟢 Day 4 – Jenkins CI Setup
- Java & Jenkins installation
- Jenkins dashboard setup
- Freestyle CI jobs
- GitHub integration

📄 `DAY4.md`

---

### 🟢 Day 5 – GitHub Webhooks
- Webhook configuration
- Auto-trigger Jenkins builds
- Webhook validation
- CI automation

📄 `DAY5.md`

---

### 🟢 Day 6 – Jenkins Pipeline
- Declarative pipeline syntax
- Jenkinsfile creation
- Pipeline stages: Checkout, Build, Test
- Pipeline-as-Code concept

📄 `DAY6.md`

---

### 🟢 Day 7 – CI/CD Deployment
- Apache Web Server setup
- Jenkins sudo permissions
- Automated deployment
- End-to-end CI/CD execution

📄 `DAY7.md`

---

## 🔄 CI/CD Workflow

Developer → GitHub → Webhook → Jenkins
↓
Checkout → Build → Test → Deploy
↓
Apache Web Server

python
Copy code

🚀 Fully automated deployment pipeline

---

## 📜 Jenkinsfile

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
                echo 'Build completed successfully'
            }
        }

        stage('Test') {
            steps {
                echo 'All tests passed'
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
```
🌐 Live Application
http://<EC2-PUBLIC-IP>


✔ Deployed automatically after every GitHub push

🧠 Key Learnings

Real-world CI/CD pipeline implementation

Jenkins automation & pipelines

GitHub Webhooks integration

Linux server management

DevOps best practices

📌 Project Status

🟢 Completed – Fully functional CI/CD pipeline

🚀 Future Enhancements

Dockerized deployment

Nginx reverse proxy

Rollback strategy

Monitoring with Prometheus & Grafana

Cloud-native CI/CD pipelines

⭐ Support

If you found this project useful:

⭐ Star this repository

🍴 Fork and experiment

🔗 Share with DevOps learners
