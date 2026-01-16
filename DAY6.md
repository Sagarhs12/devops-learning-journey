# Day 6 – Jenkins Declarative Pipeline (Pipeline as Code)

## Objective
To implement a Jenkins Declarative Pipeline using a Jenkinsfile stored in GitHub and execute a complete CI workflow.

---

## Key Concepts Learned

- Jenkins Pipeline vs Freestyle Job
- Pipeline as Code (Jenkinsfile)
- Declarative Pipeline syntax
- Multi-stage CI pipeline
- GitHub SCM integration
- Build, Test, and Post actions

---

## Jenkinsfile Used

```groovy
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
