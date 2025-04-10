pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Use bat command for Windows instead of sh
                    bat 'wsl docker build -t my-image .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    // Use bat command for Windows instead of sh
                    bat 'wsl docker run -d my-image'
                }
            }
        }
    }
}