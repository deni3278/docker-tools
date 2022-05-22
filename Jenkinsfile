pipeline {
    agent any

    stages {
        stage('Stop and remove old container(s)') {
            steps {
                script {
                    try {
                        sh 'docker compose down'
                    } finally {}
                }
            }
        }

        stage('Create and start new container(s)') {
            steps {
                sh 'docker compose up -d'
            }
        }
    }
}