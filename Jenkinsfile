pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/kunalpro379/jenkins.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'dir' // Windows equivalent of ls -l
                bat 'docker build -t my-docker-webapp .' // Build Docker image from root
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8081:80 my-docker-webapp' // Run container in detached mode
            }
        }
    }
}
