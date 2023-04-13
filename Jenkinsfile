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
            steps {
                withCredentials([string(credentialsId: 'dockerpwd', variable: 'dockerhublogin')]) {
    // some block
}
                sh 'docker login -u pradeep87987 -p ${dockerhublogin}'
                sh 'docker push pradeep87987/react-app:1.1'
            }
        }

            
        }
    }

