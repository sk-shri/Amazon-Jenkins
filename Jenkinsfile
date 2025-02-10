pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/sk-shri/Amazon-Jenkins.git'
            }
        }

        stage('Build & Package') {
            steps {
                sh 'mvn clean install'
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully'
        }
        failure {
            echo 'Build failed'
        }
    }
}

