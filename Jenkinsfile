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
                  }
              }
            }
        }
