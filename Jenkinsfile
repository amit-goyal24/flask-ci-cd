pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'flask-app-local'
    }

    stages {
        stage('Clone Repository') {
            steps {
               git branch: 'main', url: 'https://github.com/amit-goyal24/flask-ci-cd.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t ${DOCKER_IMAGE}:latest .'
                }
            }
        }

        stage('Run Locally') {
            steps {
                script {
                    bat 'docker rm -f flask-app || true'
                    bat 'docker run -d --name flask-app -p 5000:5000 ${DOCKER_IMAGE}:latest'
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
        }
    }
}
