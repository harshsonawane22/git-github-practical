pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Build stage started."'
                sh 'test -s README.md'
            }
        }

        stage('Test') {
            steps {
                sh 'grep -q "Git and GitHub practical project" README.md'
                sh 'echo "README check passed."'
            }
        }
    }
}