pipeline{
agent { label '!windows' }
stages {
    stage('SonarQube') {
    steps{
        script { scannerHome = tool 'SonarQubeScanner' }
        withSonarQubeEnv('SonarQube') {
            sh "${scannerHome}/bin/sonar-scanner -Dsonar.projectKey=OWS"
        }
    }
}
}
}
