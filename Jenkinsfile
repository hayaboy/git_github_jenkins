pipeline {
    agent {
        docker {
            image 'python:3.12-slim'   // Python이 미리 설치된 이미지 사용
            args '--user root'         // 권한 문제 해결
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
                sh 'python3 --version'     // Python 버전 확인
                sh 'ls -la'                // 파일 확인
                sh 'python3 hello.py'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline 완료!'
        }
    }
}