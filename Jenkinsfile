pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/username/cicd-devops-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cicd-project .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3000:3000 cicd-project'
            }
        }

    }
}