pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS173-1'
                sh 'g++ pipeline_test_task5.cpp -o output' 
            }
        }
        stage('Test') {
            steps {
                sh './output' 
            }
        }
        stage('Deploy') {
            steps {
                echoo 'Deploying...' 
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
