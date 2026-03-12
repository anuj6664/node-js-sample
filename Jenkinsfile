pipeline {
    agent any

    tools {
        nodejs 'nodejs'   // name from Jenkins tools
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

        stage('Deploy') {
            steps {
                echo "Deploy stage"
                bat 'npm start'
            }
        }

    }
}