pipeline {
    agent none
    stages {
        stage('Initialize') {
            def dockerHome = tool 'myDocker'
            env.PATH = "${dockerHome}/bin:${env.PATH}"
        }
        stage('Docker agent') {
            agent {
                docker {
                    image 'node:18.18.0-alpine3.18'
                    label 'agent1'
                    args '-p 3000:3000'
                }
            }
        }
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
