pipeline {
    agent any

    environment {
        GIT_SSH_COMMAND = "ssh -i /var/jenkins_home/.ssh/jenkins_nunya"
        IMAGE_NAME = "nunya64/hello-docker"
    }

    stages {
        stage('Clone Repo') {
            steps {
                sh 'rm -rf nunya || true'
                sh 'git clone -b main git@github.com:Nunya64/nunya.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                dir('nunya') {
                    sh 'docker build -t $IMAGE_NAME .'
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run --rm $IMAGE_NAME'
            }
        }
    }
}
