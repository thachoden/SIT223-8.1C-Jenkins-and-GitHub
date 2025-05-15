pipeline {
    agent any

    stages {
        stage('trigger') {
            steps {
                echo 'trigger'
            }
        }
        stage('Build') {
            steps {
                echo 'Compile and package the source code into the final artifact.'
                echo 'Used tool: Maven'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Run unit tests to ensure individual code components work correctly, and integration tests to verify that different components work together as expected.'
                echo 'Used tool: TestNG (unit & integration tests)'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analyze the source code to check quality, detect potential issues, and ensure compliance with coding standards.'
                echo 'Used tool: SonarQube'
                }
        }
        
        stage('Security Scan') {
            steps {
                echo 'Scan the source code and dependencies to identify security vulnerabilities and reduce risk of attacks.'
                echo 'Used tool: OWASP Dependency-Check'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploy the application to a staging environment (a testing environment similar to production) for comprehensive testing.'
                echo 'Used tool: AWS EC2 (virtual server)'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Run integration tests in the staging environment to ensure the application works correctly in a production-like setting.'
                echo 'Used tool: Postman/Newman (API testing)'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploy the application to the production environment to serve end users.'
                echo 'Used tool: AWS EC2 (virtual server)'
            }
        }
    }   
}
