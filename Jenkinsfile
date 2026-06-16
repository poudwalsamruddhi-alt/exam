
pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'techysambvimit/examsam'
        IMAGE_TAG = "${BUILD_NUMBER}"
    }

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/poudwalsamruddhi-alt/exam.git'
            }
        }

        stage('Show Commit ID') {
            steps {
                bat 'git rev-parse HEAD'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-app .'
            }
        }
    }
}
