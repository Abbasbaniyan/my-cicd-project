pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning code'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 9091:80 --name mycontainer myapp'
            }
        }

    }
}