pipeline {
    agent {
        docker {
            image 'node:8'
            args '-u root:root'
        }
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
}