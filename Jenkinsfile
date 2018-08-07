pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-u root:root'
        }
    }
    environment {
        CI = 'true' 
    }
    stages {
        stage('Build') { 
            steps {
                //sh'npm cache clean'
                sh 'npm install' 

                //sh 'npm install -g electron --unsafe-perm=true --allow-root'
            }
        }
    }
    stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
     }
}


    // image 'node:6-alpine' 
      //      args '-p 3000:3000' 