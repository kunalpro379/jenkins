
pipeline {
 agent any
 stages {
 stage('Checkout Code') {
 steps {
 git branch: 'main', url: 'https://github.com/name/myfirst.git'
 }
 }
 stage('Build Docker Image') {
 steps {
 dir('DockerJenkinsExperiment') { // Ensure Docker build happens in the
right folder
 sh 'ls -l' // Debugging: List files to check if Dockerfile exists
 sh 'docker build -t my-docker-webapp .' // Build Docker Image
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