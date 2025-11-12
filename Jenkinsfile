pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Fetching source code...'
                checkout scm  // ✅ Jenkins auto-fetches from correct branch
            }
        }

        stage('Build Docker Images') {
            steps {
                echo 'Building Docker images...'
                sh 'docker-compose build'
            }
        }

        stage('Deploy Containers') {
            steps {
                echo 'Deploying containers...'
                sh 'docker-compose up -d'
            }
        }
    }

    post {
        success {
            echo '✅ Deployment successful!'
        }
        failure {
            echo '❌ Deployment failed!'
        }
    }
}
