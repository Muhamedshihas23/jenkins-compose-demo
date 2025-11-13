pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Images') {
            steps {
                echo "Building Docker images..."
                sh 'docker compose build'
            }
        }

        stage('Deploy Containers') {
            steps {
                echo "Deploying containers..."
                sh 'docker compose up -d'
            }
        }
    }

    post {
        failure {
            echo "❌ Deployment failed!"
        }
        success {
            echo "✅ Deployment successful!"
        }
    }
}
