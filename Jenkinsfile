pipeline {
    agent any
    environment {
        JAVA_HOME = '/usr/lib/jvm/java-11-openjdk' // Ensure the correct Java version is set
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
    }
    stages {
        stage('Git Checkout') {
            steps {
                echo 'Checking out source code from Git...'
                git branch: 'main', url: 'https://github.com/Ashaikh609/demo1.git'
            }
        }
        stage('Build Application') {
            steps {
                echo 'Building the application with Maven...'
                sh 'mvn clean package'
            }
        }
    }
    post {
        always {
            echo 'Cleaning up workspace...'
            cleanWs() // Cleans the workspace after the build
        }
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo 'Build failed. Please check the logs for details.'
        }
    }
}