pipeline {
    agent any

tools {
    jdk 'java-17'
}

    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Ashaikh609/demo1.git'
            }
        }