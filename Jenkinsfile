pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
               git branch: 'main', url: 'https://github.com/Sanketmane5511/jenkins-demo-pipeline.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Sample build step'
            }
        }
    }
}

pipeline {
    // ... your pipeline stages ...
    post {
        success {
            // e.g., emailext body: 'Success', ...
        }
        failure {
            // e.g., emailext body: 'Failure', ...
        }
    }
}

