pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages 
    {
        stage('test') {
            steps {
                sh 'npm run test'
            }
        }
    }
}



