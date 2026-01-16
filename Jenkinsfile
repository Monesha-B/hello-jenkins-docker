pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t hello-jenkins-docker .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run --rm hello-jenkins-docker'
            }
        }
    }
}

