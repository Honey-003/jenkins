pipeline {
    agent any  // Replace 'docker' with 'any'

    stages {
        stage('Build') {
            steps {
                echo 'Compiling .cpp file'
                sh 'g++ -o PES2UG23CS827-1 hello.cpp'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing .cpp file'
                sh './PES2UG23CS827-1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application'
                // Add deployment steps if applicable
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
