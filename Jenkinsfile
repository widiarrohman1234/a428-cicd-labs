// pipeline {
//     agent any
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
    // Langkah-langkah yang akan dieksekusi dalam node agen Jenkins

    stage('Checkout') {
        // Tahap checkout kode dari repositori
        checkout scm
    }
    
    stage('Build') {
        // Tahap untuk melakukan build (misalnya, kompilasi)
        sh 'npm install'
    }

    stage('Test') {
        // Tahap untuk menjalankan pengujian
        sh './jenkins/scripts/test.sh'
    }

    stage('Deploy') {
        // Tahap untuk menerapkan ke lingkungan produksi (contoh sederhana)
        sh './jenkins/scripts/deploy.sh'
    }
}
