pipeline {
    agent any
    stages {
        stage("List Files") {
            steps {
                sh "ls -la"
            }
        }
        stage("Test Docker") {
            steps {
                sh "docker --version"
            }
        }
        stage("Build and Run Docker") {
            steps {
                sh "docker build -t nunya-app ."
                sh "docker run nunya-app"
            }
        }
    }
}
