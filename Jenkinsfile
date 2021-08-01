pipeline {
    //agent any
    //tools {nodejs "NodeJS"}
    agent {
        def dockerHome = tool 'myDocker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
        docker {
            image 'node:lts-buster-slim' 
            args '--privileged -p 3000:3000' 
        }
    }
    
    stages {
        stage('Checkout Code') { 
            steps {
                git branch: 'master', url: 'https://github.com/chutimaNan/react-resume-template.git'
                sh 'docker -v'
            }
        }
        
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
}
