pipeline {
agent any
    stages {
        stage('Build') {
             steps {
                    sh "docker build -t teeeeeest -f ./bankTest/dockerfile ."
                    }
        }
        stage('Integration Test') {
            steps {
                sh "apt install docker-compose"
                sh "docker-compose -f docker-compose.yml"
                }
        }
        
    }
}