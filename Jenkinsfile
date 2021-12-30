pipeline {
    agent any
    enviroment {
        CI = 'true'
    }
    stages{
        stage("Install Project Dependencies") {
            steps {
                nodejs(nodeJSInstallationName: 'nodenv'){
                sh "npm install"
                }
            }
        }

        stage('SonarQube Analysis') {
            enviroment{
                def SCANNER = tool 'sonarqube', type: 'hudson.plugins.sonar.SonarRunnerInstallation';
            }

            steps {
                 withSonarQubeEnv(installationName: 'sonarqube') {
                    sh "${SCANNER}/bin/sonar-scanner"
                }
            }
        }

        stage('test') {
            steps {
                sh 'npm run test'
            }
        }
    }
}


