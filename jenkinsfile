pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/<your-username>/jenkins-demo-pipeline.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Sample build step'
            }
        }
    }
}
