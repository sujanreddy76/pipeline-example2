pipeline {
    agent{
        label 'java-label'
    }
    environment {
        DEPLOY_TO='production'
    }
    stages {
        stage('Bulid') {
            steps {
                echo 'Building the project'
            }
        }
        stage('Sonar') {
            steps {
                echo 'Running Sonar Scan'
            }
        }
        stage('Deploy to Dev Env') {
            steps {
                echo 'Deploying to Dev environment'
            }
        }
        stage('Deploy to QA Env') {
            steps {
                echo 'Deploying to QA environment'
            }
        }
        stage('Deploy to Stage Env') {
            when{
                expression {
                    BRANCH_NAME==/(production|staging)/
                }
            }
            steps {
                echo 'Deploying to Stage environment'
            }
        }
    }
}
