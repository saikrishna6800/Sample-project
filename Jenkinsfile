pipeline {
    agent any

    parameters {
        string(name: 'APP_VERSION', defaultValue: 'v1.0.0', description: 'Enter app version')
    }

    stages {
        stage('Checkout') {
            steps {
                echo "Cloning repo for version: ${params.APP_VERSION}"
            }
        }

        stage('Build') {
            steps {
                echo "Building application version ${params.APP_VERSION}"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying version ${params.APP_VERSION} to production..."
            }
        }
    }
}
