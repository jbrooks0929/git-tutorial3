pipeline {
    agent any
    stages {
        stage('Check Code') {
            steps{
                git branch: 'main', url: 'https://github.com/jbrooks0929/git-tutorial3.git'
            }
        }
        stage('Build'){
            steps{
                sh 'echo "building app"'
            }
        }
        stage('Test'){
            steps{
                sh 'echo "Running tests"'
            }
        }
        stage('Deploy'){
            steps{
                sh 'echo "deploying"'
            }
        }
    }
}
