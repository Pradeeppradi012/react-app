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
                sh 'docker build -t pradeep87987/react-app:1.2 .'
            }
        }
        stage('Push Image') {
            steps {
              
                sh 'docker login -u pradeep87987 -p Pradi@012'
                sh 'docker push pradeep87987/react-app:1.2'
            }
        }
        stage('Deploy') {
            steps {
                kubernetesDeploy configs: 'deployment.yaml', kubeConfig: [path: ''], kubeconfigId: 'kubepwd', secretName: '', ssh: [sshCredentialsId: '*', sshServer: ''], textCredentials: [certificateAuthorityData: '', clientCertificateData: '', clientKeyData: '', serverUrl: 'https://']
            }
        }

            
        }
    }

