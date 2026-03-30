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
                // docker tag nginx i27devopsb6/nginx:b6
                // docker push <url>
            }
        }
    }
}
