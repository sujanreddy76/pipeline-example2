pipeline {
    agent{
        label 'java-label'
    }
    environment {
        DEPLOY_TO='xyz'
    }
    stages{
        stage('Build'){
            when{
                environment name: 'DEPLOY_TO', value: 'production'
            }
            steps {
                echo 'Building the project'
            }
        }
    }
}
