pipeline {
    agent any
    tools {
        nodejs 'nodejs'
    }
    stages {
        stage('Pre-build') {
            steps {
                bat 'npm install'
            }
        }
        stage('Pre-test') {
            steps {
                bat 'npm run pretest'
            }
        }
        stage('Test') {
            steps {
                bat 'npm test'
            }
        }  
        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
               bat 'npx pm2 restart prod-deploy'
            }
        }
    }
}