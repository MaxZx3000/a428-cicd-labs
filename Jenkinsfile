// pipeline {
//     agent {
//         docker {
//             image 'node:lts-buster-slim'
//             args '-p 3000:3000'
//         }
//     }
//     environment {
//         CI = 'true'
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
    stage('Agent Docker Intialization'){
        image 'node:lts-buster-slim'
        args '-p 3000:3000'
    }
    stage('Build'){
        sh 'npm install'
    }
    stage("Test"){
        sh './jenkins/script/test.sh'
    }
}