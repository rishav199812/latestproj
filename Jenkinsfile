pipeline {
    agent { docker { image 'python:3.10.7-alpine' } }
    stages {
        stage('Initialize'){
        def dockerHome = tool 'mydocker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
    }
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
}