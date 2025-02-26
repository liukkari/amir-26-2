pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/liukkari/amir-26-2'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Code Coverage') {
            steps {
                sh 'mvn jacoco:report'
            }
        }
    }
}