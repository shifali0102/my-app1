pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                retry(3) {
                   echo " deploying retry"
                }

                timeout(time: 3, unit: 'MINUTES') {
                   echo "wait for timeout"
                }
            }
        }
    }
}
