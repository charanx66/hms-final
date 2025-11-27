pipeline {
    agent any
    environment {
        DOCKER_COMPOSE_VERSION = '1.29.2'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Docker Images') {
            steps {
                script {
                    sh 'docker-compose build'
                }
            }
        }
        stage('Run Tests') {
            steps {
                script {
                    // Add test commands for backend/frontend if available
                    echo 'Add your test scripts here.'
                }
            }
        }
        stage('Deploy (Optional)') {
            steps {
                script {
                    echo 'Add deployment steps here.'
                }
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
