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
                git 'https://github.com/AnilComakeit/testinggitjenikins.git'
                sh '''
                     sh some.sh 
                ''' + $name
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
