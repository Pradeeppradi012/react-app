pipeline {
    agent any
    stages {
        stage('Gitpull') {
            steps {
                sh 'git pull https://github.com/Pradeeppradi012/react-app.git'
            }
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t pradeep87987/react-app'
            }
        }
        
    }
}