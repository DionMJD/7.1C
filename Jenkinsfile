pipeline {
    agent any
    triggers {
    pollSCM('* * * * *')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile and package the source code using Maven.'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests to ensure the code functions as expected using Junit'
                echo 'Task: Run integration test to ensure different components of the application work together as expected using Postman'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse the source code and ensure it meets industry standards using SonarQube.'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Task: Scan and analyse the code for security vulnerabilities using Snyk.'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the application to a AWS EC2 instance staging server.'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests on the staging environment runs as expected'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the application build to the production AWS EC2 instance environment.'
            }
        }
    }
}
