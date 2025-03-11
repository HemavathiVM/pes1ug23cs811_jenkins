pipeline {
    agent any  // Runs on any available Jenkins agent

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'g++ -o hello_exec hello.cpp'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './hello_exec'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully! ✅'
        }
        failure {
            echo 'Pipeline failed ❌'
        }
    }
}
