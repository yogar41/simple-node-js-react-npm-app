pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                    sh 'npm install' 
                  }
                }
        stage('Test') {
            steps {
                    sh './jenkins/scripts/test.sh'
                  }
              }
        stage('Deploy') {
            steps {
                    sh './jenkins/scripts/deliver.sh'
                    input message: 'Finished using the web site: (Click "proceed to continue)'
                    sh './jenkins/scripts/kill.sh'
                  }
              }
            }
        }
