//environment: environment block can be specified at the the pipeline level or stage level
pipeline {
    agent {
        label 'java-label'
    }
    environment{
        NAME="Sujan"
        COURSE="k8s"
        CLOUD="GCP"
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
