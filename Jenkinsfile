pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS306-1 main.cpp' // Compiling the C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS306-1' // Running the compiled file
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Add deployment steps if required
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
