pipeline {
    agent { dockerfile true }
    stages {
        stage('Test') {
            steps {
                bat 'docker build -t something .'
                bat 'docker run -dit --name my-running-app -p 8081:80 something'
            }
        }
    }
}