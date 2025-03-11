pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ PES1UG22CS148-1.cpp -o YOUR_SRN-1'
            }
        }
        stage('Test') {
            steps {
                sh './YOUR_SRN-1'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
