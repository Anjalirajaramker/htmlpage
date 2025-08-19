pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // For a simple HTML project, build may just be copying files or running static site generators
                // For now, let's just echo a message
                echo 'Build stage - No build needed for plain HTML'
            }
        }

        stage('Test') {
            steps {
                // If you have tests (like HTML validation), you could run them here
                echo 'Test stage - No tests defined'
            }
        }

        stage('Archive') {
            steps {
                // Archive HTML files so they are available in Jenkins UI
                archiveArtifacts artifacts: '**/*.html', fingerprint: true
            }
        }

        stage('Deploy') {
            steps {
                // You can add deployment steps here, like copying files to a web server
                echo 'Deploy stage - Add deployment commands here'
            }
        }
    }

    
}
