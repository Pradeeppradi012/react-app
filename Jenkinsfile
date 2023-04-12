pipeline {
    agent any
    stages {
        stage('Pull') {
            steps {
                sh 'git pull https://github.com/Pradeeppradi012/react-app.git'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t pradeep87987/react-app .'
            }
        }
    }
}