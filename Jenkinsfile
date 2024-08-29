pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // build the code using a build automation tool to compile and package (e.g. Maven)
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration Tests...'
                // unit and Integration Tests - run unit tests to ensure the code functions as expected and run integration tests to ensure the different components of the 
                // application work together as expected. (e.g. JUnit )
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing Code...'
                // integrate a code analysis tool to analyse the code and ensure it meets industry standards. (e.g. SonarQube)
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Running Security Scan...'
                // perform a security scan on the code using a tool to identify any vulnerabilities. (e.g. OWASP Dependency-Check)
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging Environment...'
                // deploy the application to a staging serve (e.g.,AWS EC2 instance)
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running Integration Tests on Staging...'
                // run integration tests on the staging environment to ensure the application functions as expected in a production-like environment.
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production...'
                 // deploy the application to a production serve (e.g.,AWS EC2 instance)
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
