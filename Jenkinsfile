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
                     /home/siva/git-files/./script.sh $name
                }
            }    
        }
    }
}
