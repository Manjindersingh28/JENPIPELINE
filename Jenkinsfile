pipeline {
    agent any

    environment {
        DIRECTORY_PATH = '/Users/manjinder/Desktop/Jenkinsfile'
        PRODUCTION_ENVIRONMENT = 'ManjinderSingh'
    }

    stages {
        stage('Build') {
            steps {
                echo "Building the code using Maven"
                // Implement build automation tool (e.g., Maven) here
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo "Running unit tests"
                // Implement test automation tool for unit tests here
                echo "Running integration tests"
                // Implement test automation tool for integration tests here
            }
            
        }

        stage('Code Analysis') {
            steps {
                echo "Performing code analysis"
                // Integrate code analysis tool (e.g., SonarQube) here
            }
        }

        stage('Security Scan') {
            steps {
                echo "Performing security scan"
                // Integrate security scanning tool (e.g., OWASP ZAP) here
            }
            
        }

        stage('Deploy to Staging') {
            steps {
                echo "Deploying application to staging server (e.g., AWS EC2)"
                // Implement deployment to staging server here
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo "Running integration tests on staging environment"
                // Implement integration tests on staging environment here
            }
        }

        stage('Deploy to Production') {
            steps {
                echo "Deploying application to production server (e.g., AWS EC2)"
                // Implement deployment to production server here
            }
        }
    }

    post {
        success {
            emailext(
                    subject: "Pipeline Success",
                    body: "Pipeline ran successfully",
                    to: 'mani28au@gmail.com',
                    attachlog: true
                    )
        }
        failure {
            emailext(
                    subject: "Pipeline Failure",
                    body: "Pipeline failed to run",
                    to: 'mani28au@gmail.com',
                    attachlog: true
            )
        }
    }
}
