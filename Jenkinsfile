pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
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
    
        stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
        }
        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
    }
}


    // image 'node:6-alpine' 
      //      args '-p 3000:3000' 