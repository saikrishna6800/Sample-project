pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning from GitHub...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the app...'
                sh 'echo "build complete" > build.log'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'build.log'
            }
        }
    }

    post {
        success {
            echo '✅ Build successful!'
        }
        failure {
            echo '❌ Build failed!'
        }
    }
}
