pipeline {
    agent any
    stages {
        stage("Stage 1"){
            steps {
                sh "sh deploy.sh"
            }
        }
        stage("Stage 2"){
            steps {
                sh "docker build -t jenkins ."
            }
        }
        stage("Stage 3"){
            steps {
                sh "docker run -d -t --name jenkins jenkins"
            }
        }
    }
}

