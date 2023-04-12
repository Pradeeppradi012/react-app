pipeline {
    agent any
    stages {
        stage('Gitpull')
        sh 'git pull https://github.com/Pradeeppradi012/react-app.git'

    }
    stages {
        stage('Build')
        sh 'docker build -t pradeep87987/react-app'
    }
}