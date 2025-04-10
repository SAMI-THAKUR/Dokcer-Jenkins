pipeline { 
    agent any 
    environment {
        GIT_CREDENTIALS = 'GitHub-Credentials' // Ensure this matches your credentials ID in Jenkins
    }
    stages { 
        stage('Checkout Code') { 
            steps { 
                git credentialsId: "${GIT_CREDENTIALS}", branch: 'main', url: 'https://github.com/SAMI-THAKUR/Dokcer-Jenkins'
            } 
        } 
        
        stage('Build Docker Image') { 
            steps { 
                dir('DockerJenkinsExperiment') { 
                    sh 'ls -l'  // Debugging: List files to check if Dockerfile exists
                    sh 'docker build -t my-docker-webapp .'  // Build Docker Image
                } 
            } 
        } 
        
        stage('Run Docker Container') { 
            steps { 
                sh 'docker run -d -p 8081:80 my-docker-webapp'
            } 
        } 
    }
}
