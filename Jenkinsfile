pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                cleanWs()
                checkout scm
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t test-image .'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed! Check SCM configuration or Docker setup.'
        }
        success {
            echo 'Docker image built successfully!'
        }
    }
}
