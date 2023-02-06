pipeline {
    agent any

    stages {
        stage('SCM') {
            steps {
                git branch: 'main', url: 'https://github.com/angelocho/hello-2048.git'
            }
        }
        stage('TestingDocker') {
            steps {
                sh 'docker-compose config'
            }
        }
        stage('building') {
            steps {
                sh 'docker-compose build'
            }
        }
        stage('starting') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
