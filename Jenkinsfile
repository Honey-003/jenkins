pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
               sh 'g++ hello.cpp -o hello_exec' 
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'  // Ensure it's executable or you may need `chmod +x PES2UG23CS827-1`
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
