pipeline {
    agent none 
    stages {
        stage('Gradle Version') {
              agent { 
                    node{
            label 'master' 
            customWorkspace 'C:\\Users\\shifali.srivastava\\Desktop\\INFOSYS\\JANUARY\\Jenkins\\workspace'
                       } 
                    } 
                steps { 
                    git url: 'https://github.com/shifali0102/my-app1.git'
                     bat 'gradle --version'
                  }
             }
        stage('Gradle Version node') {
              agent { 
            label 'windows' 
                     } 
                steps { 
                   // git url: 'https://github.com/shifali0102/my-app1.git'
                     bat 'gradle --version'
                  }
             }
        }
    }
