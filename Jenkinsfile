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
