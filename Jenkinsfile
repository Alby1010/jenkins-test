pipeline {
    agent any

    stages {
        stage('Build and deploy') {
            steps {
                sh 'ls'
                sh 'docker build -t nodejs:latest .'
                sh 'docker stop nodejs'
                sh 'docker run --name nodejs -p 80:3000 nodejs:latest'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}