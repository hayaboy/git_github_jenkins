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
                    apt-get update -y || true
                    apt-get install -y python3
                '''
            }
        }
        
        stage('Run') {
            steps {
                sh 'python3 --version'
                sh 'ls -la'
                sh 'cat hello.py'
                sh 'python3 hello.py'
            }
        }
    }
    
    post {
        always {
            echo '✅ Pipeline 완료'
        }
    }
}