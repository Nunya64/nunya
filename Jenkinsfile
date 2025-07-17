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
    }
}
