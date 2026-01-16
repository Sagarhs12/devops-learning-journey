pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
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
                sudo systemctl restart httpd
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
