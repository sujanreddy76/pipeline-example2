//script-block
pipeline {
    agent {
        label 'java-label'
    }
    stages {
        stage('Build'){
            steps{
                echo 'executing build block'
                sh 'hostname -i'
                
            }

        }
        stage('Scriptblock'){
            steps{
                script{
                    def course = "k8s"
                    if (course == "k8s") 
                        println("Thanks for enrolling in ${course}")
                    else
                        println("Do enroll in ${course}")    

                }
            }
        }
    }
}
