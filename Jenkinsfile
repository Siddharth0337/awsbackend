pipeline{
    agent any
    tools {
        // Specify the name of the Git installation configured in Jenkins
        git 'MyGitInstallation'
   
    }

    stages{
        stage('Build'){
            steps{
                
                // Get the source code from the git repo
                checkout scm
                //run mvn wrapper commands
                sh "./mvnw clean complie"
                echo 'Building the Project with Maven Complie'
            }
        }
        stage('Test'){
            steps{
                
                //run mvn wrapper commands
                sh "./mvnw clean test"
                echo 'Testing the Project with Maven Test'
               
            }
        }
        stage('Package'){
            steps{
                
                //run mvn wrapper commands
                sh "./mvnw clean package"
                echo 'Packaging the Project with Maven package'
            }
        }



    }
}