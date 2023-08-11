pipeline {
    agent {label 'linux_node'}
    
    tools {
        nodejs 'nodejs-16.20.2'
    }
    
    stages {
        stage('Clone repo'){
            steps {
                git 'https://github.com/gurleravindar/react.git'
            }
        }
        stage('Intsall node modules') {
            steps {
                sh 'npm install'
            }
        }
        stage('Start application and to access host-agent-ip:3000'){
            steps {
                sh 'npm start'
            }
        }
         stage('Build'){
            steps {
                sh 'npm build'
            }
        }
         stage('test'){
            steps {
                sh 'npm test'
            }
        }
         stage('eject'){
            steps {
                sh 'npm eject'
            }
        }
    }
}
