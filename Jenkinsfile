pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output PES1UG23CS803-1.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh 'invalid_command_here'  // Intentional error
                    sh './output'  // Run the compiled binary
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}