pipeline {
    agent any
      environment {
        variable1 = 'true'
    }

    stages {
        stage('Deploy') {
            steps {
                retry(3) {
                   echo " deploying retry"
                    echo "Database engine is ${variable1}"
                    echo "running ${BUILD_ID}"
                }

                timeout(time: 3, unit: 'MINUTES') {
                   echo "wait for timeout"
                }
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
