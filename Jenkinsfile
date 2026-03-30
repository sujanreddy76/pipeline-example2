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
                sh 'whoami'
                sh 'pwd'
                //pull nginx and change the name to myOwnName and push to registry
                sh 'docker pull nginx'
                echo '**********Printing the images before changing the tag**********'
                sh 'docker images'
                sh 'docker tag nginx sujanreddy76/nginx:v1'
                echo '**********Printing the images after changing the tag**********'
                sh 'docker images'
                echo '******Docker Login******'
                sh "docker login -u ${DOCKER_CREDS_USR} -p ${DOCKER_CREDS_PSW}"
                echo '**********Pushing the image to repo***********'
                sh 'docker push sujanreddy76/nginx:v1'
            }
        }
    }
}
