pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS144-1'
                script {
                    def compileResult = sh(script: 'g++ main.cpp -o output', returnStatus: true)
                    if (compileResult != 0) {
                        error 'Compilation failed'
                    }
                }
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
