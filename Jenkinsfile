def Variable1, user_input
pipeline{
    agent any
    environment {
        JAVE_HOME = "/usr/lib/jvm/java-11-openjdk-amd64"
    }
    parameters {
  string description: 'This are the environments used for build and please select user', name: 'Environment_Groovy'
  choice choices: ['Development', 'Testing', 'Deploy', 'Release'], description: 'Please Select User', name: 'Users_Groovy'
  booleanParam description: 'Please Select Boolean Valiue', name: 'Boolean Select Groovy'
}
    stages{
        stage("CheckOut Code From Git"){
            when{
                branch 'main'
            }
            steps{
                script{
                    Variable1 = "Sunday" 
                    //echo "${params.Environment_Groovy}"
                    git branch: 'main', url: 'https://github.com/Sailaxmi005/PracticeRepo.git'
                
                    
                }
            }
            
        }
        stage("Execute Maven Goals"){
            steps{
                script{
                     sh 'mvn clean install'
                }
               
            }
            
        }
        stage("List files"){
            steps{
               script{
                     sh 'ls -la'
                }
            }
            
        }
        stage("Archive"){
            steps{
                archiveArtifacts artifacts: 'target/*'
            }
            
        }
        stage("Clean Work Space"){
            steps{
                cleanWs()
            }
        }
    }
}
