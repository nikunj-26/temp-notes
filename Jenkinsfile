pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
                bat 'npm run build'
            }
        }
        stage('Docker Stuff') {
            steps {
                bat 'docker pull httpd'
                bat 'docker build -t something .'
                bat 'docker run -dit --name my-running-app -p 8081:80 something'
            }
        }
    }
}