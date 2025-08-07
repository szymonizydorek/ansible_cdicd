pipeline {
    agent any

    stages {
        stage('List Files') {
            steps {
                sh 'ls -alh'
            }
        }

        stage('Execute shell') {
            steps {
                sh '''
                    hostname
                '''
            }
        }
    }
}

