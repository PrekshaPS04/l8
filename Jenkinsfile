pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch : 'main',url : 'https://github.com/PrekshaPS04/l8.git'
            }
        }

        stage('build image') {
            steps {
                bat 'docker build -t l8 .'
            }
        }
        stage('Run') {
            steps {
                bat 'docker run -d -p 80:80 --name l8c l8'
            }
        }
    }
}