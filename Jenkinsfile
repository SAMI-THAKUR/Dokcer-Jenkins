pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    bat 'docker build -t my-image .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    bat 'docker run -d my-image'
                }
            }
        }
    }
}