pipeline {
    agent any 
    stages {
        stage('input'){
            steps{
                git 'https://github.com/SivaKumarK1/jenkins-integration.git'
                input(message:'Enter Name', ok: 'Submit')
                sh script.sh
            }
        }
    }
}