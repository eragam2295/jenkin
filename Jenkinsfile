pipeline {
    agent any
    tools {
        jdk 'java'
        git 'Default'
        maven 'Maven'
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
        stage('--artifactspush--'){ 
            steps {
                def server = Artifactory.server artifactory
                def uploadSpec = """{
                "files": [{
                "pattern": "/var/lib/jenkins/workspace/MBPipeline_master/target/maven-archetype-quickstart-1.4.jar",
                "target": "jenkins-local"
                }
                }
            }
        ]
    }"""

  server.upload(uploadSpec)            
            }
        }
    }
}
