pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages 
    {
        stage("Install Project Dependencies"){
            steps{
                sh 'npm install'
            }            
        }
    }
}
