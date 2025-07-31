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
                sh 'echo "Simulating build..."'
                // Uncomment to simulate failure
                // sh 'exit 1'
            }
        }
    }
    post {
        failure {
            // Simple 'mail' step, configured in Manage Jenkins -> Configure System (basic mail)
            mail to: 'manesankett@gmail.com',
                 subject: "FAILURE: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
                 body: "Build failed! Check details at: ${env.BUILD_URL}"
        }
    }
}


