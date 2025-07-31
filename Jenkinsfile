// pipeline {
//     agent any
//     stages {
//         stage('Checkout') {
//             steps {
//                git branch: 'main', url: 'https://github.com/Sanketmane5511/jenkins-demo-pipeline.git'
//             }
//         }
//         stage('Build') {
//             steps {
//                 echo 'Sample build step'
//             }
//         }
//     }
// }


pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'echo Building...'
                // Uncomment below line to simulate a failure
                // bat 'exit 1'
            }
        }
    }
    post {
        success {
            mail to: 'manesankett@gmail.com',
                 subject: "SUCCESS: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: "Great news, the build succeeded!\n\nDetails: ${env.BUILD_URL}"
        }
        failure {
            mail to: 'manesankett@gmail.com',
                 subject: "FAILURE: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: "Unfortunately, the build failed.\n\nDetails: ${env.BUILD_URL}"
        }
    }
}



