pipeline {
    agent{
        label 'java-label'
    }
    environment {
        DEPLOY_TO='xyz'
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
                    branch 'main'
                }
                
            }
            steps {
                echo 'Deploying to Stage environment'
            }
        }
        stage('Deploy to Prod Env') {
            when{
                anyOf {
                    branch 'prod'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo 'Deploying to Production environment'
            }
        }        
    }
}
