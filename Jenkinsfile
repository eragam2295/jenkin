pipeline {
    agent any
    tools {
        jdk 'openjdk 1.8'
        git 'Default'
        maven 'maven'
    }
    stages {
        stage('---clean---') {
            steps {
                sh "mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package"
            }
    }
}
    
}
