pipeline {
    agent any
    tools {nodejs "node"}
    
    stages {
        stage('Checkout Code') { 
            steps {
                git branch: 'master', url: 'https://github.com/chutimaNan/react-resume-template.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'npm install'
            }
    }
}
