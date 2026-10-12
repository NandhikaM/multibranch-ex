@'
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo "Building branch: ${env.BRANCH_NAME}"
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'java -version'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            when { branch 'main' }
            steps {
                echo 'Deploying from main only...'
            }
        }
    }
}
'@ | Set-Content -Encoding ascii Jenkinsfile