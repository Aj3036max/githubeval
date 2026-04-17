pipeline {
    agent any

    stages {
        stage('Install Docker') {
            steps {
                sh '''
                sudo apt update
                sudo apt install -y docker.io
                sudo systemctl start docker
                sudo systemctl enable docker
                '''
            }
        }

        stage('Check Docker') {
            steps {
                sh 'docker --version'
            }
        }
    }
}
