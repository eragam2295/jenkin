pipeline {
    agent any
    tools {
        jdk 'java'
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
