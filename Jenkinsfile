pipeline {
    agent {
        label 'java-label'
    }
    parameters {
        choice (name: 'deployToProd',
                choices: 'no\nyes'
                description: 'Deploy to Production'
        )

    }
    stages {
        stage('Build'){
            steps{
                echo 'Building the application'
            }

        }
        stage('DeployToProd'){
            when {
                expression {
                    params.deployToProd == 'yes'
                }
            }
            steps{
               echo 'Deploying to production'

            }
        }
    }
}
