pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    bat 'docker build -t my-image:${BUILD_NUMBER} .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    // Stop and remove any previous container with the same name
                    bat 'docker stop my-container || echo "No container to stop"'
                    bat 'docker rm my-container || echo "No container to remove"'
                    
                    // Run the container with a specified name and port mapping
                    bat 'docker run -d -p 8080:80 --name my-container my-image:${BUILD_NUMBER}'
                    
                    echo 'Application is now accessible at http://localhost:8080'
                }
            }
        }
    }
}