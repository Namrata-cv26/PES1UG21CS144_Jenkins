pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                   
                    sh 'g++ working.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Skipping test stage'
                    // Or perform any other necessary actions instead of executing the missing file
                }
            }
        }

        stage('Deploy') {
            steps {
                ech 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}