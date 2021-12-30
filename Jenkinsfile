pipeline {
    agent any
    stages 
    {
        stage("Install Project Dependencies") 
        {
            sh "npm install"
        }
    
        stage('SonarQube Analysis') 
        {
            def SCANNER = tool 'sonarqube';

            steps 
            {
                withSonarQubeEnv(installationName: 'sonarqube') 
                {
                    sh "${SCANNER}/bin/sonar-scanner"
                }
            }
        }
    }
}
