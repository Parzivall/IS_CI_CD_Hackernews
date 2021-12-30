pipeline {
    agent any
    enviroment {
        CI = 'true'
    }
    stages 
    {
        stage("Install Project Dependencies"){
            steps{
                sh "npm install"
            }            
        }
    }
}
