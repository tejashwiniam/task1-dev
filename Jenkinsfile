pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/tejashwiniam/task1-dev.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'scp target/app.jar user@server:/deploy/path/'
            }
        }
    }
}

