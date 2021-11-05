pipeline {
    agent any
    
    tools { nodejs "node" }
    stages {
        
        stage('Install') {
            steps {
                dir ("${env.WORKSPACE}/src") {
                  sh 'npm install'
                }
            }
        }

        stage('Test') {
            steps {
                dir ("${env.WORKSPACE}/src") {
                  sh 'CI=true npm run test'
                }
            }
        }
        
        stage('Build') {
            steps {
                dir ("${env.WORKSPACE}/src") {
                  sh 'CI=true npm run build'
                }
            }
        }
    }
}