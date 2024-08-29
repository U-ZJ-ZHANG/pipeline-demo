pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add build steps here (e.g., using Maven or Gradle)
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration Tests...'
                // Add testing steps here (e.g., using JUnit or another testing framework)
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing Code...'
                // Add code analysis steps here (e.g., using SonarQube)
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Running Security Scan...'
                // Add security scanning steps here (e.g., using OWASP Dependency-Check)
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging Environment...'
                // Add deployment steps here (e.g., deploying to AWS EC2 or another staging environment)
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running Integration Tests on Staging...'
                // Add integration test steps for the staging environment
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production...'
                
            }
        }
    }

     post {
        success {
            echo 'Pipeline succeeded!'
            mail bcc: '',
                body: "Build Successful! Check Jenkins for details.",
                subject: "Jenkins Pipeline Success: ${currentBuild.fullDisplayName}",
                to: 'yamamotorgb@gmail.com'
        }
        failure {
            echo 'Pipeline failed!'
            mail bcc: '',
                body: "Build Failed! Check Jenkins for details.",
                subject: "Jenkins Pipeline Failure: ${currentBuild.fullDisplayName}",
                to: 'yamamotorgb@gmail.com'
        }
    }
}
