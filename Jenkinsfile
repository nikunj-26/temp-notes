pipeline {
    agent { dockerfile true }
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
                bat 'npm run build'
            }
        }
        stage('Test') {
            steps {
                bat 'docker build -t something .'
                bat 'docker run -dit --name my-running-app -p 8081:80 something'
            }
        }
    }
}