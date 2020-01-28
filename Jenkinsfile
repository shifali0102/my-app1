pipeline {
    agent none 
    stages {
        stage('Gradle Version') {
              agent { label 'windows'} 
                steps { 
                     bat 'gradle --version'
                  }
             }
        }
    }
