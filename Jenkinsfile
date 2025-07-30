pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Sanketmane5511/jenkins-demo-pipeline.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Sample build step'
            }
        }
    }
}
