Automated Deployment using Jenkins Pipeline (CI/CD)
# Day 7 – Automated Deployment using Jenkins Pipeline (CI/CD)

## 🎯 Objective
To complete the CI/CD pipeline by automatically deploying a web application to an Apache web server on an AWS EC2 instance using Jenkins Pipeline.

---

## 🛠 Tools & Technologies Used
- AWS EC2 (Amazon Linux 2023)
- Jenkins
- Git & GitHub
- Jenkins Pipeline (Jenkinsfile)
- Apache HTTP Server (httpd)
- Linux (Amazon Linux)
- GitHub Webhooks

---

## 📁 Project Structure


devops-learning-journey/
├── DAY1.md
├── DAY2.md
├── DAY3.md
├── DAY4.md
├── DAY5.md
├── DAY6.md
├── DAY7.md
├── Jenkinsfile
├── README.md
└── index.html


---

## 🚀 Steps Performed

### 1️⃣ Installed Apache Web Server
```bash
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd

2️⃣ Created Application File

Created a modern index.html file to be deployed automatically by Jenkins.

3️⃣ Configured Jenkins Pipeline (Jenkinsfile)

Added a Deploy stage to copy the application file to Apache’s web directory.

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
                echo 'Deploying application to Apache web server'
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

4️⃣ Configured Sudo Access for Jenkins

Allowed Jenkins to run deployment commands without password prompts.

sudo visudo


Added:

jenkins ALL=(ALL) NOPASSWD: ALL

5️⃣ Triggered Pipeline via GitHub Push

Any push to the GitHub repository now automatically:

Pulls code

Builds

Tests

Deploys to Apache

✅ Final Result

Jenkins Pipeline executed successfully

Application deployed automatically

Website accessible via EC2 public IP

http://<EC2-PUBLIC-IP>
