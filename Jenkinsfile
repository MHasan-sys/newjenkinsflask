pipeline {
    agent any

    stages {
        stage('Build & Run Docker') {
            steps {
                script {
                    // Stop any running containers (ignore errors)
                    sh 'docker-compose down || true'

                    // Build and run using docker-compose
                    sh 'docker-compose up -d --build'
                }
            }
        }
    }
    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}
