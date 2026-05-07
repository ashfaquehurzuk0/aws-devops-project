pipeline {
    agent any
    environment {
        IMAGE_NAME = "ashfaquehurzuk0/flask-app"
    }
    stages {
        stage('Clone') { steps { checkout scm } }
        stage('Build') {
            steps { sh "docker build -t ${IMAGE_NAME}:${BUILD_NUMBER} ." }
        }
        stage('Push') {
            steps {
                sh "docker push ${IMAGE_NAME}:${BUILD_NUMBER}"
            }
        }
        stage('Deploy') {
            steps {
                sh "docker stop flask-app || true"
                sh "docker rm flask-app || true"
                sh "docker run -d -p 5000:5000 --name flask-app ${IMAGE_NAME}:${BUILD_NUMBER}"
            }
        }
    }
}
