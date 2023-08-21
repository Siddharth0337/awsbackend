pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                //get source codefrom rep
                git 'https://github.com/Siddharth0337/estore_backend.git'
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