pipeline {
    agent{
        label 'java-label'
    }
    parameters{
        string (name: 'PERSON' , defaultValue: 'Sujan', description: 'Enter your name')
        choice (name: 'COURSE', choices: ['k8s', 'jenkins', 'docker'], description: 'Select the course')
        booleanParam (name: 'CLOUD', defaultValue: true, description: 'Do you want to be certified in GCP??')
    }
    stages{
        stage('Firststage') {
            steps {
                echo "Welcome ${params.PERSON}"
                echo "You are enrolled for ${params.COURSE}"
                echo "You are certified in GCP: ${params.booleanParam}"
            }
        }
    }
}
