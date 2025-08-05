

// pipeline {
//     agent any

//     stages {
//         stage('Build') {
//             steps {
//                 echo 'Building...'
//                 // your build logic here
//             }
//         }

//         stage('Test') {
//             steps {
//                 echo 'Testing...'
//                 // your test logic here
//             }
//         }
//     }

//     post {
//         success {
//             emailext(
//                 subject: "SUCCESS: Job '${env.JOB_NAME} [#${env.BUILD_NUMBER}]'",
//                 body: """
//                     Good news!

//                     Job: ${env.JOB_NAME}
//                     Build: #${env.BUILD_NUMBER}
//                     URL: ${env.BUILD_URL}

//                     The build was successful!
//                 """,
//                 to: 'manesankett@gmail.com'
//             )
//         }

//         failure {
//             emailext(
//                 subject: "FAILURE: Job '${env.JOB_NAME} [#${env.BUILD_NUMBER}]'",
//                 body: """
//                     Oh no!

//                     Job: ${env.JOB_NAME}
//                     Build: #${env.BUILD_NUMBER}
//                     URL: ${env.BUILD_URL}

//                     The build failed.
//                 """,
//                 to: 'manesankett@gmail.com'
//             )
//         }
//     }
// }

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat '''
                    mkdir output
                    echo Log contents > output\\build.log
                    echo Report data > output\\report.txt
                    echo Main output > output\\build.txt
                '''
                archiveArtifacts artifacts: 'output\\*.*', fingerprint: true
            }
        }
    }
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
    }
}




