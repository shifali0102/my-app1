pipeline {
    agent none 
    stages {
        stage('Gradle Version') {
              agent { label 'master'} 
                steps { 
                   // git url: 'https://github.com/shifali0102/my-app1.git'
                     bat 'gradle --version'
                  }
             }
        }
    }
