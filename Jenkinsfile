pipeline{
agent { label '!windows' }
stages {
    stage('SonarQube') {
    step{
        script { scannerHome = tool 'SonarQube Scanner' }
        withSonarQubeEnv('SonarQube') {
            sh "${scannerHome}/bin/sonar-scanner -Dsonar.projectKey=OWS"
        }
    }
}
}
}
