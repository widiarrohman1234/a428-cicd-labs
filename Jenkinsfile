pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                // sh 'npm cache clean -f'
                // sh 'npm install -D @pmmmwh/react-refresh-webpack-plugin react-refresh'
                sh 'npm install'
            }
            stage('Test'){
                steps{
                    sh './jenkins/scripts/test.sh'
                }
            }
        }
    }
}
