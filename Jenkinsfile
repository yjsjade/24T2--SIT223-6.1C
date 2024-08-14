//file type changed to .java for submission to ontrack
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building the code..."
                echo "using automation tool Maven"
            }
        }

        stage('Unit and Integration Test') {
            steps {
                echo 'Running unit tests to ensure code functions as expected'
                echo 'Running integration test to ensure diff components work together as expected'
                echo 'using automation tool JUnit or Katalon'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analyse the code and ensure it meets industry standards'
                echo 'using automation tool SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Perform a security scan on the code using a tool to identify any vulnerabilities'
                echo 'using automation tool OWASP ZAP'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Run integration tests on the staging environment to ensure the application functions as expected in a production-like environment.'
                echo 'using automation tool Protractor'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploy the application to a production server'
                echo 'using automation tool AWS EC2 instance'

            }
        }
    }

    post {
        success {
            echo 'Pipeline finished successfully!'
            mail bcc: '', body: 'Test', subject: 'Test', to: 'jingshii.y@gmail.com'

            emailext(
                subject: "Successful Pipeline ${BUILD_NUMBER}",
                to: 'jingshii.y@gmail.com',
                mimeType: 'text/html',
                body: "The pipeline completed successfully.",
                attachLog: true
            )       
        }
        

        failure {
            echo 'Pipeline failed!'
            emailext(
                subject: "Failed Pipeline ${BUILD_NUMBER}",
                to: 'jingshii.y@gmail.com',
                mimeType: 'text/html',
                body: "Something went wrong. Please check the logs for more details.",
                attachLog: true
            ) 
        }
    }
}