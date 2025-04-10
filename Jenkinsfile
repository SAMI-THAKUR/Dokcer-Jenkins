pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    bat 'docker build -t sepm .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {

                    
                    // Run the container with a specified name and port mapping
                    bat 'docker run -d -p 8080:80 --name my-container sepm'
                    
                    echo 'Application is now accessible at http://localhost:8080'
                }
            }
        }
    }
}