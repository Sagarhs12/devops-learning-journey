🚀 Day 6 – Jenkins Pipeline (Pipeline as Code)
📌 Objective

The objective of Day 6 was to implement Jenkins Pipeline as Code using a Jenkinsfile, enabling a structured, version-controlled CI pipeline with multiple stages.

🔹 What is Jenkins Pipeline?

A Jenkins Pipeline is a suite of plugins that supports implementing and integrating continuous delivery pipelines into Jenkins.

Instead of configuring jobs manually in the UI, pipelines are written as code and stored in a repository.

🔹 Why Pipeline as Code?

Version control for CI/CD logic

Easy collaboration and rollback

Repeatable and reliable builds

Industry best practice for DevOps

🔹 Types of Jenkins Pipelines

Declarative Pipeline (used in this project)

Scripted Pipeline

Declarative pipelines are:

Simpler

More readable

Easier to maintain

🔹 Pipeline Job Creation in Jenkins
Job Type:
Pipeline

Job Name:
devops-learning-journey-pipeline

Pipeline Definition:

Pipeline script from SCM

SCM: Git

Repository URL:

https://github.com/Sagarhs12/devops-learning-journey.git


Branch: main

Script Path:

Jenkinsfile

🔹 Jenkinsfile (Pipeline Code)

The Jenkins pipeline was defined using a Jenkinsfile stored at the root of the repository.

Jenkinsfile Content:
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning GitHub repository...'
                git branch: 'main',
                    url: 'https://github.com/Sagarhs12/devops-learning-journey.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage started'
                sh 'echo Build successful'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage started'
                sh 'echo All tests passed'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully 🎉'
        }
        failure {
            echo 'Pipeline failed ❌'
        }
    }
}

🔹 Initial Issue Faced
❌ Error:
Unable to find Jenkinsfile from git repository

🔍 Cause:

Jenkinsfile was missing in the repository

✅ Solution:

Created Jenkinsfile

Committed and pushed it to GitHub

Re-ran the pipeline job

🔹 Successful Pipeline Execution
Jenkins Console Output Highlights:

Jenkinsfile fetched from GitHub

Repository checked out successfully

All pipeline stages executed:

Checkout

Build

Test

Pipeline finished with SUCCESS

🔹 Stages Executed
Stage	Status
Checkout	✅ Success
Build	✅ Success
Test	✅ Success
Post	✅ Success
🔹 Key Learnings

Jenkins Pipeline fundamentals

Pipeline as Code best practices

Declarative pipeline syntax

Jenkinsfile structure

Troubleshooting missing Jenkinsfile errors

End-to-end CI pipeline creation

🎯 Outcome

By the end of Day 6:

Jenkins Pipeline job was created successfully

CI logic moved from UI to code

Jenkinsfile version-controlled in GitHub

Pipeline executed automatically and reliably
