pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git ' https://github.com/SaiNimbalkar/event-registration-devops.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t event-registration-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 5000:5000 event-registration-app || true'
            }
        }

    }
}