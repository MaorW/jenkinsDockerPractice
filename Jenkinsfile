pipeline {
    agent any
    stages {
        stage('node') {
            agent{
                docker {image 'node:16.13.1-alpine'}
            }
            steps {
                sh 'node --version'
            }
        }
        stage('python') {
            agent{
                docker{image 'python'}
            }
            steps {
                sh 'python3 --version'
            }
        }
    }
}