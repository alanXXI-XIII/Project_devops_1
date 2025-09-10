pipeline {
    agent any
    stages {
        stage('Build Docker image') {
            agent {
                docker {
                    image 'docker:24.0.5' // Official Docker CLI image
                    args '-v /var/run/docker.sock:/var/run/docker.sock'
                }
            }
            steps {
                script {
                    docker.build("testapp:latest")
                }
            }
        }
    }
}
