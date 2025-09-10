pipeline {
    agent any
    stages {
        stage('Build Docker image') {
            steps {
                script {
                    docker.build("testapp:latest")
                }
            }
        }
    }
}
