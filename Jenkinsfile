pipeline {
    agent any

    environment {
        IMAGE_NAME = 'jbrooks0929/git-tutorial3'
    }

    stages {

        stage('Build Docker image') {
            steps {
                bat 'docker build -t %IMAGE_NAME%:latest .'
            }
        }

        stage('Push DockerHub') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'docker',
                    usernameVariable: 'DOCKER_USER',
                    passwordVariable: 'DOCKER_PASS'
                )]) {
                    bat '''
docker login -u %DOCKER_USER% -p %DOCKER_PASS%
docker push %IMAGE_NAME%:latest
docker logout
'''
                }
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deploying application...'
            }
        }

    }
}
