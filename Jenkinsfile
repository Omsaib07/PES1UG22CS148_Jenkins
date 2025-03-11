pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ non_existent_file.cpp -o YOUR_SRN-1'  // Intentional Error
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
