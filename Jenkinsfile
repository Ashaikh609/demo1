pipeline {
    agent any

    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Ashaikh609/demo1.git'
            }
        }

        stage('compile') {
            steps {
                sh "mvn clean compile"
            }
        }
    }    
}
