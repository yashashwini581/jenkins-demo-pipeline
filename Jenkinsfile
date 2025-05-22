pipeline {
    agent any

    stages {
        stage('Clean Workspace') {
            steps {
                // Clean before checkout to get fresh clone
                deleteDir()
            }
        }

        stage('Checkout') {
            steps {
                // Clone latest code
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Add your build commands here, e.g. npm install, mvn package, etc.
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy commands here
            }
        }
    }
    
    post {
        always {
            echo 'Cleaning up after build...'
            // Optional cleanup steps
        }
    }
}
