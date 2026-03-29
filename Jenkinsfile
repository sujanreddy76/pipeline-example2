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
                    def course = "jenkinsPipeline"
                    if (course == "k8s") 
                         println("Thanks for enrolling in ${course}")
                        // println("Thanks for enrolling in ${course}")
                    else
                        println("Do enroll in ${course}")    
                    sleep 15 //equivalent to: sh 'sleep 15'    

                }
            }
        }
    }
}
