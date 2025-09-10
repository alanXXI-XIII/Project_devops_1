pipeline {
    agent any
    stages {
        stage('Build Docker image') {
            agent {
                docker {
                    image 'docker:24.0.5-dind' // Docker-in-Docker image
                    args '--privileged -v /var/run/docker.sock:/var/run/docker.sock'
                }
            }
            steps {
                sh 'docker build -t testapp:latest .'
            }
        }
    }
}
