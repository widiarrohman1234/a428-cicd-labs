pipeline {
    agent any
    environment {
        JAVA_OPTS = "-Dhudson.plugins.git.GitSCM.ALLOW_LOCAL_CHECKOUT=true"
    }
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
    }
}