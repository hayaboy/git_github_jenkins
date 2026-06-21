pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install Python') {
            steps {
                sh 'apt-get update && apt-get install -y python3'
            }
        }
        stage('Run') {
            steps {
                sh 'python3 hello.py'
            }
        }
    }
}