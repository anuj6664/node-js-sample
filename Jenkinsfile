pipeline {
    agent any

    tools {
        nodejs 'nodejs'
    }

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/anuj6664/node-js-sample.git'
            }
        }

        stage('Build') {
            steps {
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                bat 'npm test'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t nodeapp .'
            }
        }

        stage('Docker Run') {
            steps {
                bat 'docker run -d -p 3000:3000 nodeapp'
            }
        }

    }
}