pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Ashaikh609/demo1.git'
            }
        }

        stage('Verify Java Version') {
            steps {
                sh 'java -version'
            }
        }

    stage('Build Application') {
            steps {
                sh "mvn clean package"
            }
        }

    stage('Docker Build Image') {
            steps {
                sh "docker build -t ALS ."
                sh "docker tag ALS altamash212/demoapp2"
                sh "docker push altamash212/demoapp2"
            }
        }      
        
    }
}