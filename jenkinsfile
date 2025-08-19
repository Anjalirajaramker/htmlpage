pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Jenkins automatically checks out the repo when using Pipeline script from SCM,
                // so you usually don't need an explicit git step here.
                echo 'Code checked out automatically.'
            }
        }

        stage('Build') {
            steps {
                echo 'Build step: For static HTML, no build needed.'
            }
        }

        stage('Test') {
            steps {
                script {
                    if (!fileExists('index.html')) {
                        error "index.html not found!"
                    } else {
                        echo "index.html found, test passed."
                    }
                }
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'index.html', fingerprint: true
            }
        }
    }
}
