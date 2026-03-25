pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/rohandhenge/L1-cicd-project'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3000:3000 my-app'
            }
        }
    }
}
