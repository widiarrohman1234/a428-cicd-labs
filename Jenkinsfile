pipeline {
    agent any
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
                sh './jenkins/scripts/delivery.sh'
                sleep 60
                sh './jenkins/scripts/kill.sh'
            }
        }
    }
}
