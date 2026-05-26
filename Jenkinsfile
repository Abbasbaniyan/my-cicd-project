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
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 9091:80 --name mycontainer myapp'
            }
        }

    }
}