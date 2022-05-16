pipeline {
    agent any

    stages {
        stage('Build and deploy') {
            steps {
                sh 'ls'
                sh 'whoami'
                sh 'docker build -t nodejs:latest .'
                sh 'docker stop  nodejs   && docker rm nodejs'
                sh 'docker run --name nodejs -p 80:3000 -d nodejs:latest'
            }
        }

    }
}
