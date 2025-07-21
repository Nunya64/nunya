pipeline {
    agent any
    stages {
        stage('Checkout and Verify') {
            steps {
                git branch: 'main',
                    credentialsId: 'ssh-key-Nunya64',
                    url: 'git@github.com:Nunya64/nunya.git'
                sh 'ls -la'
            }
        }
    }
}
