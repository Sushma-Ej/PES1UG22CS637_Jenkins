pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Sushma-Ej/PES1UG22CS637_Jenkins.git'
            }
        }
        stage('Build application') {
            steps {
                sh 'g++  -o PES1UG22CS637-1 main.cpp'
            }
        }
        stage('Test application') {
            steps {
                sh './PES1UG22CS637-1'
            }
        }
        stage('Deploy application') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}
