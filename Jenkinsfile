pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh'npm cache clean'
                sh 'npm install' 

                //sh 'npm install -g electron --unsafe-perm=true --allow-root'
            }
        }
    }
}