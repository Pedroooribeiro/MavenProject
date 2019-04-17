pipeline{
    agent any
    stages{
        stage('MAVEN'){
            steps{
                println ("Elvira's")
                sh '''
                mvn clean package -f ./pom.xml 
                '''
            }
        }
    }
}