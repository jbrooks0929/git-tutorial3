pipeline {
    agent any

    stages {
        stage('Check Code') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/jbrooks0929/git-tutorial3'
            }
        }

        stage('Build') {
            steps {
                bat 'echo Building application...'
            }
        }

        stage('Test') {
            steps {
                bat 'echo Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deploying application...'
            }
        }
    }
}
