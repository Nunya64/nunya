pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', credentialsId: 'github-ssh-nunya', url: 'git@github.com:Nunya64/nunya.git'
                sh 'ls -la'
            }
        }
        stage('Test Docker') {
            steps {
                sh 'docker --version'
            }
        }
        stage('Build and Run Docker') {
            steps {
                sh 'docker build -t nunya-app .'
                sh 'docker run nunya-app'
            }
        }
    }
}
