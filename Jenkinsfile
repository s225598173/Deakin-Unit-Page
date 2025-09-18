pipeline {
    agent any
    
    environment {
        DIRECTORY_PATH = "/path/to/code" 
        TESTING_ENVIRONMENT = "Test-Environment"
        PRODUCTION_ENVIRONMENT = "Aayushree"  
    }
    
    stages {
        stage('Build') {
            steps {
                echo "Fetch the source code from the directory path specified by the environment variable: ${env.DIRECTORY_PATH}"
                echo "Compile the code and generate any necessary artefacts"
            }
        }
        
        stage('Test') {
            steps {
                echo "Unit tests"
                echo "Integration tests"
            }
        }
        
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }

        stage('Security Scan') {
            steps {
                echo "Check the security of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy the application to a testing environment specified by the environment variable: ${env.TESTING_ENVIRONMENT}"
            }
        }
        
        stage('Approval') {
            steps {
                echo "Waiting for manual approval..."
                sleep(time:10, unit:"SECONDS")
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo "Deploying the application to the staging environment"
            }
        }

        stage('Integration Testing') {
            steps {
                echo "Running integration tests in the staging environment"
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploying the application to the production  specified by the environment variables: ${env.PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}

