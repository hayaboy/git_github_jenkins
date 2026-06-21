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
                sh '''
                    sudo apt-get update -y
                    sudo apt-get install -y python3 python3-pip
                '''
            }
        }
        
        stage('Run') {
            steps {
                sh 'python3 --version'
                sh 'python3 hello.py'
            }
        }
    }
}