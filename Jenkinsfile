pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Vaibhav-2100/CICD-project.git'
            }
        }

        stage('Build Containers') {
            steps {
                dir('app') {
                    sh '/usr/local/bin/docker-compose build'
                }
            }
        }

        stage('Deploy Application') {
            steps {
                dir('app') {
                    sh '/usr/local/bin/docker-compose up -d'
                }
            }
        }

    }
}
