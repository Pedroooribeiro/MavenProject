pipeline{
    agent any
    stages{
        stage('MAVEN'){
            steps{
                    println ("Elvira's")
                    configFileProvider([configFile(fileId: 'SigressOSS', targetLocation: 'settings.xml', variable: 'MAVEN_SETTINGS'), configFile(fileId: 'OSSSettings', targetLocation: 'global.xml', variable: 'MAVEN_GLOBAL_SETTINGS')]) {
                    sh """
                    mvn clean package -f ./pom.xml -s '${MAVEN_SETTINGS}' -gs '${MAVEN_GLOBAL_SETTINGS}' -Dmaven.test.skip=true
                    """
                }
            }
        }
    }
}