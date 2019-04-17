pipeline{
    agent any
    stages{
        stage('Sonar'){
            steps{
                println ("Elvira's Sucess!")
            }
        }
        stage('Build'){
            steps{
                configFileProvider([configFile(fileId: 'SigressOSS', targetLocation: 'settings.xml', variable: 'MAVEN_SETTINGS'), configFile(fileId: 'OSSSettings', targetLocation: 'global.xml', variable: 'MAVEN_GLOBAL_SETTINGS')]) {
                sh """
                mvn clean package -f ./pom.xml -s '${MAVEN_SETTINGS}' -gs '${MAVEN_GLOBAL_SETTINGS}' -Dmaven.test.skip=true
                """
                }
            }
        }
        stage('Testes'){
            steps{
                println("Elvira's Sucess!")
            }
        }
        stage('Upload'){
            steps{
                println("Elvira's Sucess!")
            }
        }
        stage('Deploy'){
            steps{
                println ("Elvira's Sucess!")
            }
        }
    }
}