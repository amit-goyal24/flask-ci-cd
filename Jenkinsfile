pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'flask-windows-app'
    }

    stages {
        stage('Clone Code') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t %DOCKER_IMAGE% .'
            }
        }

        stage('Run Container') {
            steps {
                bat '''
                    docker rm -f flask-container || exit 0
                    docker run -d --name flask-container -p 5000:5000 %DOCKER_IMAGE%
                '''
            }
        }
    }

    post {
        always {
            echo 'Pipeline complete. Check http://localhost:5000'
        }
    }
}
