pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *')  // Poll GitHub every 2 minutes
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application using Maven...'
                echo 'Tool: Maven'
                // Example (commented out): sh 'mvn clean install'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests using JUnit and TestNG...'
                echo 'Tools: JUnit, TestNG'
                // Example: sh 'mvn test'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analyzing code with SonarQube...'
                echo 'Tool: SonarQube'
                // Example: sh 'sonar-scanner'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing security scan using OWASP Dependency-Check...'
                echo 'Tool: OWASP Dependency-Check'
                // Example: sh './dependency-check/bin/dependency-check.sh --project SIT753-Project --scan .'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging server (e.g., AWS EC2)...'
                echo 'Tool: AWS CLI or Ansible'
                // Example: sh 'ansible-playbook deploy_staging.yml'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging using Postman...'
                echo 'Tool: Postman'
                // Example: sh 'newman run tests.postman_collection.json'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production server (e.g., AWS EC2)...'
                echo 'Tool: AWS CLI or Ansible'
                // Example: sh 'ansible-playbook deploy_production.yml'
            }
        }
    }
}
