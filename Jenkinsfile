pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Pearlochani131677/FIRST-JENKINS-GIT.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                dir('webapp') {
                    bat 'docker build -t my-docker-webapp .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8081:80 my-docker-webapp'
            }
        }
    }
}
