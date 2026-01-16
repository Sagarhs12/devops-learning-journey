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
                sh 'echo "Build successful"'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage started'
                sh 'echo "All tests passed"'
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
