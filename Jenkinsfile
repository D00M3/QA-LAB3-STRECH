pipeline {
    agent any
    stages {
        stage("Stage 1"){
            steps {
                sh "docker rm -f $(docker ps -a -q) || true"
            }
        }
        stage("Stage 2"){
            steps {
                sh "docker build -t jenkins ."
            }
        }
        stage("Stage 3"){
            steps {
                sh "docker run -d -t --name jenkins jenkins2""
            }
        }
    }
}

