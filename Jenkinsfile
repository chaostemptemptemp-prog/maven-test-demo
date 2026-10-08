pipeline {
    agent any
    tools {
        maven 'maven3'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '**']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/chaostemptemptemp-prog/maven-test-demo.git']])
            }
        }
        stage('Compile') {
            steps {
                bat 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}