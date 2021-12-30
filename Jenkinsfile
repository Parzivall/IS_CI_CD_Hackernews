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

        stage('SonarQube Analysis') {
        enviroment{
            def SCANNER = tool name: 'sonarqube', type: 'hudson.plugins.sonar.SonarRunnerInstallation';
        }

        steps {
            withSonarQubeEnv(installationName: 'sonarqube') {
                sh "${SCANNER}/bin/sonar-scanner"
            }
        }
    }
}



