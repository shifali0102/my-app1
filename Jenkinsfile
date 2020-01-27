pipeline {
    agent any
      environment {
        variable1 = 'true'
    }

    stages {
        stage('Deploy') {
             environment { 
                DEBUG_FLAGS = '-g'
            }
            steps {
                retry(3) {
                   echo " deploying retry"
                    echo "Database engine is ${variable1}"
                    echo "running ${env.BUILD_ID}"
                    echo "${DEBUG_FLAGS}"
                    echo "${JOB_NAME} 	${BUILD_TAG} ${EXECUTOR_NUMBER} ${NODE_NAME} ${WORKSPACE} ${JENKINS_HOME} ${JENKINS_URL} ${BUILD_URL} ${JOB_URL}"
                    echo ${BRANCH_NAME}
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
