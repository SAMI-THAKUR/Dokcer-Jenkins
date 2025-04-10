pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Run Docker build inside WSL
                    sh 'wsl docker build -t my-image .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    // Run Docker container inside WSL
                    sh 'wsl docker run -d my-image'
                }
            }
        }
    }
}
