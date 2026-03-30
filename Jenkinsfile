pipeline {
    agent {
        label 'java-label'
    }
    environment{
        NAME="Sujan"
        COURSE="k8s"
    }
    stages{
        stage('Build'){
            environment{
                CLOUD="AWS"
            }
            steps {
                echo "Welcome ${NAME}"
                echo "You are enrolled for ${COURSE} course"
                echo "You are certified in ${CLOUD}"
            }
        }
    }
}
