
pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'techysambvimit/examsam'
        IMAGE_TAG = "${BUILD_NUMBER}"
    }

    stages {
        stage('Checkout') {
    steps {
        checkout scm
    }
}

        stage('Show Commit ID') {
            steps {
                bat 'git rev-parse HEAD'
            }
        }
stage('Build with Maven') {
    steps {
        bat 'mvn clean package -DskipTests'
    }
}
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t my-app .'
            }
        }
    }
}
