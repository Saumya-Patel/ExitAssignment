pipeline {
    agent any
    tools {
        maven "MAVEN_HOME"
    }
    environment {
        JAVA_HOME = 'C:\\Program Files\\OpenLogic\\jdk-21.0.3.1-hotspot'
        PATH = "${env.JAVA_HOME}\\bin;${env.PATH}"
    } 
    stages {
        stage('Clean') {
            steps {
                // Clean up any temporary files or resources
                bat 'mvn clean'
            }
        }
        stage('Build') {
            steps {
                // Clean and build the Maven project
                bat 'mvn build'
            }
        }
        stage('Test') {
            steps {
                // Run tests
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                // Placeholder for deployment steps
                // Replace this with your deployment script or commands
                echo 'Deploying the application...'
            }
        }
        stage('Clean Up') {
            steps {
                // Clean up any temporary files or resources
                bat 'mvn clean'
            }
        }
    }
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
