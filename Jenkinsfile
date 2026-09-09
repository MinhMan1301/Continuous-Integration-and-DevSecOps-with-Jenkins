pipeline {
    agent any
    triggers {
        pollSCM('H/5 * * * *')
    }
    stages {
        stage("Build") {
            steps {
                echo 'Compile & package code. Tool: Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Run unit & integration tests. Tool: JUnit (unit), Selenium (integration)'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyse code quality. Tool: SonarQube'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Scan for vulnerabilities. Tool: OWASP Dependency-Check'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploy to staging server. Tool: AWS EC2'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Test on staging environment. Tool: Postman/Newman'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploy to production server. Tool: AWS EC2'
            }
        }
    }
}