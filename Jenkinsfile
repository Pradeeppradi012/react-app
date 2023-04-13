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
                sh 'docker build -t pradeep87987/react-app:1.1 .'
            }
        }
        stage('Push Image') {
            environment {
                registryCredential = 'dockerhublogin'
            }
            steps{
                sh 'docker.withRegistry( 'https://registry.hub.docker.com', registryCredential )'
                sh 'docker push pradeep87987/react-app:1.1'
            }
        }
    }
}
