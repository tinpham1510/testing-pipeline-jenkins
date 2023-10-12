pipeline {
    agent none
    stages {
      	stage('Node Install') {
        	agent {
          	docker {
                image 'node:18.18.0-alpine3.18' 
                args '-p 3000:3000' 
            }
          }
          steps {
          	sh 'npm install'
          }
        }
    }
}
