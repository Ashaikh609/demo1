pipeline {
    agent any

    environment {
    JAVA_HOME = '/path/to/java-17'
    PATH = "${JAVA_HOME}/bin:${env.PATH}"
}
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
        
    }
}