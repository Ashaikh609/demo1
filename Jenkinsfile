pipeline {
    agent any
    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Ashaikh609/demo1.git'
            }
        }
        stage('Build Application') {
            steps {
                sh "mvn clean package"
                 }
                }
        stage('Docker image build') {
            steps {
                sh "docker build -t demoapp ."
                 }
                }
        stage('Push Docker image') {
            steps {
                sh "docker tag demoapp altamash212/demoapp"
                sh "docker push altamash212/demoapp:latest"
                 }
                }
    }    
}
