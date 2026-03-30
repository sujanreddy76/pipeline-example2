pipeline {
    agent {
        label 'java-label'
    }
    stages {
        stage('Build'){
            steps {
                 echo 'Building the project'
            }
        }
        stage('Scans'){
            parallel{
                stage('Sonar'){
                    steps {
                        echo 'Running sonar scan'
                        sleep 10
                    }
                    
                }
                stage('Checkmarx'){
                    steps {
                        echo 'Running checkmarx scan'
                        sleep 10
                    }
                    
                }
                stage('Fortify'){
                    steps {
                        echo 'Running fortify scan'
                        sleep 10
                    }
                    
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the project'
            }
        }
    }
}
