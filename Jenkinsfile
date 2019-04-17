pipeline{
    agent any
    stages{
        stage('Checkout SCM'){
            steps {
                print ("Sucess!")
            }
        }
        stage('Maven'){
            sh ''' mvn package 
            java -cp target/hello.jar com.example.hello.hello
            '''
        }
    }
}