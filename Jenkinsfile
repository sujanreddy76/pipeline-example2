pipeline {
    agent{
        label 'java-label'
    }
    environment{
        DOCKER_CREDS=credentials('Dockerhub_Creds') //We will get username and password(OURVARNAME_USR,OURVARNAME_PSW)
    }
    stages{
        stage('DockerBP') {
            steps {
                echo 'Deploying from main branch'
            }
        }
    }
}
