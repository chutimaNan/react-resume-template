pipeline {
    agent {
        docker {
            image 'node:lts-buster-slim' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Checkout Code') { 
            steps {
                git branch: 'master', url: 'https://github.com/chutimaNan/react-resume-template.git'
            }
        }
        stage('Build') {
            steps {
                sh "npm install"
            }
        }
        stage('Build') {
            steps {
                sh "npm test"
            }
        }
        stage('Deliver') {
            steps {
                sh "npm start"
            }
        }
    }
}