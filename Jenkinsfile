pipeline {
    agent any

    stages {
        stage('1. Maven Compile & Package') {
            steps {
                echo ' Jenkins is starting the Maven Build Phase...'
                bat 'mvn clean package'
            }
        }
        stage('2. Deploying App (Ansible Step)') {
            steps {
                echo ' Maven build successful! Simulating Ansible Deployment...'
                // This simulates Ansible copying the file to a production folder
                bat 'mkdir C:\\production-deployment-dir || exit 0'
                bat 'copy target\\python-maven-demo-1.0-SNAPSHOT.jar C:\\production-deployment-dir\\app.jar'
                echo ' App deployed successfully to C:\\production-deployment-dir\\app.jar!'
            }
        }
    }
}
