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
                def SCANNER = tool name: 'SonarQubeScanner', type: 'hudson.plugins.sonar.SonarRunnerInstallation';
            }

            steps {
                 withSonarQubeEnv(installationName: 'sql') {
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


