pipeline {
agent any
    stages {
        stage('Build') {
            steps {
                sh "docker build dockerfile ."
            }
        }
        stage('Integration Test') {
            steps {
                sh "docker-compose -f docker-compose.yml up --force-recreate --abort-on-container-exit"
                sh "docker-compose -f docker-compose.yml down -v"
            }
        }
    }
}