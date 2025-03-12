pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Compiling .cpp file'
                sh 'g++ -o PES2UG23CS827-1 src/hello.cpp'  // Adjust the path if necessary
            }
        }
        stage('Test') {
            steps {
                echo 'Running .cpp file'
                sh './PES2UG23CS827-1'  // Ensure it's executable or you may need `chmod +x PES2UG23CS827-1`
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
