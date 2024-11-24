pipeline {
    agent any

    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', url: 'git@github.com:Ashaikh609/demo1.git'
            }
        }
         stage('mvn build') {
            steps {
                sh 'mvn clean package'
            }
        }
        }    
}
