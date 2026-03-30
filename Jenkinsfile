pipeline {
    agent{
        label 'java-label'
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
            }
        }
    }
}
