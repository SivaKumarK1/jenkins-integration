def name = null
pipeline {
    agent none 
    stages {
        stage('input'){
            steps{
                script{
                    name = input(
                        message: 'enter your name', ok: 'Submit', parameters: [string(defaultValue:'Siva' , name:'NAME',trim:true)]               
                    )
                }
            }
        }
        stage('run'){
            agent any
            steps {
                git 'https://github.com/SivaKumarK1/jenkins-integration.git'
                script{
                    echo "Hello, $name"
                }
                sh ''' sh script.sh ''' script{ $name }
            }    
        }
        stage('Result'){
            agent any
            steps{
                echo "Succesful Build of Pipeline !!!"
            }
        }
    }
}
