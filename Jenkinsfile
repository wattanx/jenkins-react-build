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
        
        stage('Build') {
            steps {
                dir ("${env.WORKSPACE}/src") {
                  sh 'npm run build'
                }
            }
        }
    }
}