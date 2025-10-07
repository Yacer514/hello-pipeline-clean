pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('hello-jenkins-clean-image')
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    docker.image('hello-jenkins-clean-image').run('-p 3110:80')
                }
            }
        }
    }
}