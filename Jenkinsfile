pipeline {
    agent any
    environment {
        DIRECTORY_PATH = 'C:\ProgramData\Jenkins\.jenkins\workspace\pipeline task'  
        TESTING_ENVIRONMENT = 'TestEnv'
        PRODUCTION_ENVIRONMENT = 'MeghanaProd'
    }
    stages {
        stage('Build') {
            steps {
                echo "Fetching the source code from the directory path: ${env.DIRECTORY_PATH}"
                echo "Compile the code and generate necessary artifacts"
            }
        }
        stage('Test') {
            steps {
                echo "Running unit tests"
                echo "Running integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Checking the quality of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the application to the testing environment: ${env.TESTING_ENVIRONMENT}"
            }
        }
        stage('Approval') {
            steps {
                echo "Pausing for manual approval"
                sleep 10  // Simulates manual approval by pausing for 10 seconds
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying the application to the production environment: ${env.PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
