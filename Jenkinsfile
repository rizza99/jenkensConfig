/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'php:8.3.1-alpine3.19' } }
    stages {
        stage('build') {
            steps {
                sh 'php --version'
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}

