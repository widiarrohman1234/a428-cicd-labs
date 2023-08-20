pipeline {
    agent {
        docker {
            image 'node:16-buster-slim' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                // sh 'npm cache clean -f'
                // sh 'npm install -D @pmmmwh/react-refresh-webpack-plugin react-refresh'
                sh 'npm install'
            }
        }
        stage('Test'){
            steps{
                sh './jenkins/scripts/test.sh'
            }
        }
        stage('Manual Approval'){
            steps{
                input message: 'Lanjutkan ke tahap Deploy?'
            }
        }
        stage('Deploy'){
            steps{
                sleep 60
            }
        }
    }
}
