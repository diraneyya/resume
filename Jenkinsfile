/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'node:18.17.1-buster' } }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
            }
        }
    }
}