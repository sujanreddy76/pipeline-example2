//timeout
pipeline {
    agent {
        label 'java-label'
    }
    stages{
        stage('Build') {
            steps {
                timeout(time: 5, unit: 'SECONDS'){
                    echo 'sleep for 60 seconds'
                    sleep 60
                }

            }
        }
    }
}
