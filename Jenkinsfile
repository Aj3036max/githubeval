pipeline {
    agent any

    stages {

        stage('Clean Workspace') {
            steps {
                deleteDir()
            }
        }

        stage('Checkout SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/Aj3036max/githubeval.git'
            }
        }

        stage('Pull Nginx Image') {
            steps {
                sh 'sudo docker pull nginx'
            }
        }

        stage('Check Image') {
            steps {
                sh 'sudo docker images'
            }
        }
    }
}
