pipeline {
    agent any

    tools {
        maven 'Maven-Local'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/l-rohittt-l/jenkins-demo.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean test'
            }
        }
    }

    post {
        success {
            echo 'Build Successful!'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}