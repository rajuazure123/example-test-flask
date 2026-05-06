pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/rajuazure123/example-test-flask.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flask-app:latest .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'kubectl apply -f k8s/'
            }
        }
    }
}
