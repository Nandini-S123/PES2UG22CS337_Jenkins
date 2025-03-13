pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello_exec main/non_existing_file.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline Failed!'
        }
    }
}
