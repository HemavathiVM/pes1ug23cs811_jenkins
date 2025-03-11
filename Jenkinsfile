pipeline {
    agent any
    stages {
        stage('Cleanup') {
            steps {
                sh 'rm -rf *'  // Deletes everything to ensure a fresh checkout
            }
        }
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[url: 'https://github.com/HemavathiVM/pes1ug23cs811_jenkins.git']],
                    extensions: [[$class: 'WipeWorkspace']]
                ])
            }
        }
    }
}
