pipeline {
    agent any  

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the C++ program...'
                    sh 'g++ -o PES1UG22AM177-1 main.cpp'  
                }
            }
        }

        stage('Test') {
        steps {
            script {
                echo 'Running tests...'
                sh './non_existent_binary'  // Intentional error: this file does not exist
            }
        }
    }


        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying application (Simulated)...'
                    echo 'Deployment Successful!'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed'  
        }
    }
}
