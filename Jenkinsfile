pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

    stage('Syntax Check') {
        steps {
            sh '''
            #!/bin/bash
            which shellcheck || sudo apt-get install -y shellcheck
            find . -name "*.sh" -exec shellcheck {} +
            '''
        }
    }
    stage('Secure Execution') {
        steps {
            echo "Executing shell script securely..."
        }
    }
