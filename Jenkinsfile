pipeline {
    agent any
    tools {
        nodejs 'nodejs'
    }
    stages {
        stage('Pre-build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Pre-test') {
            steps {
                sh 'npm run pretest'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }  
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
               sh 'npm start'
            }
        }
    }
}