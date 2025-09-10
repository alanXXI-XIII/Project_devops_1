pipeline {
    agent any
    stages {
        stage('Build Docker image') {
            steps {
                // Use host Docker via mounted socket
                sh 'docker --version'
                sh 'docker build -t testapp:latest .'
                sh 'docker images'
            }
        }
    }
}
