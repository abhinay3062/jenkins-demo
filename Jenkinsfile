
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Downloading source code from GitHub'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application'
                sh 'ls -la'
                sh 'test -f index.html'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the HTML application'
                sh "grep -q 'Hello from GitHub!' index.html"
                echo 'HTML test passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment simulation successful!'
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }
        failure {
            echo 'CI/CD Pipeline failed!'
        }
    }
}
