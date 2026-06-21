pipeline {
    agent {
        docker {
            image 'python:3.12-slim'
            args '--user root'
            reuseNode true
        }
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Run') {
            steps {
                sh 'python3 --version'
                sh 'ls -la'
                sh 'cat hello.py'        // 파일 내용 확인용
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