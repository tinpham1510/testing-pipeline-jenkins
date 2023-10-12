pipeline {
    agent none
    stages {
      	stage('Node Install') {
            agent {
              	docker {
                    image 'node:18.18.0-alpine3.18' 
                }
            }
            steps {
          	    sh 'npm install'
            }
        }
    }
}
