pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    credentialsId: 'ssh-key-Nunya64',
                    url: 'git@github.com:Nunya64/nunya.git'
            }
        }
        stage('List Files') {
            steps {
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
