pipeline {
    agent any

    stages {
        stage('List Files') {
            steps {
                sh 'ls'
            }
        }

        stage('Execute shell') {
            steps {
                sh '''
                    whoami
                '''
            }
        }

        stage('Execute Ansible Playbook') {
            steps {
               ansiblePlaybook(
                   credentialsId: 'ansible_ssh_key',
                   disableHostKeyChecking: true,
                   installation: 'Ansible',
                    inventory: 'inventory',
                    playbook: 'application_deployment.yaml'
              )
            }
        }
    }
}

