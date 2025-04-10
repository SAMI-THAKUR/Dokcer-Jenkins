pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    powershell 'wsl docker build -t my-image .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    powershell 'wsl docker run -d my-image'
                }
            }
        }
    }
}