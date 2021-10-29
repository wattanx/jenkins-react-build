pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir (./src) {
                  echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                  sh 'npm install'
                }
            }
        }
    }
}