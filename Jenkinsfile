// pipeline {
//     agent any
//     environment {
//         JAVA_OPTS = "-Dhudson.plugins.git.GitSCM.ALLOW_LOCAL_CHECKOUT=true"
//     }
//     stages {
//         stage('Build') { 
//             steps {
//                 sh 'npm install' 
//             }
//         }
//         stage('Test') {
//             steps {
//                 sh './jenkins/scripts/test.sh'
//             }
//         }
//     }
// }

node {
    def localCheckoutAllowed = System.getProperty('hudson.plugins.git.GitSCM.ALLOW_LOCAL_CHECKOUT')
    echo "Local Checkout Allowed: ${localCheckoutAllowed}"
    
    stage('Build') {
        // Langkah-langkah build
        sh 'npm install'
    }
    
    stage('Test') {
        // Langkah-langkah pengujian
        sh './jenkins/scripts/test.sh'
    }
}
