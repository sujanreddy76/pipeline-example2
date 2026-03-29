pipeline {
    agent {
        label 'java-label'
    }
    stages {
        stage('Build'){
            steps{
                retry(3){
                    echo "welcome to jenkins"
                    error "I will print error message"
                }
                error "Message after 3 times"
                
            }

        }
    }
}
