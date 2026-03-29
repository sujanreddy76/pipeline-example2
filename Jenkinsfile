//tools
pipeline {
    agent {
        label 'java-label'
    }
    tools{
        maven 'Maven_3.8.9' //this name should match to the name created under Manage jenkins->tools section
    }
    stages{
        stage('Maven version') {
            steps {
                echo 'Welcome to tools demo'
                sh 'mvn --version'
            }
        }
    }
}
