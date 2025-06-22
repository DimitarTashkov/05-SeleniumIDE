pipeline {
    agent any

    stages {
        stage('Checkout the repository') {
            steps {
                checkout scm
            }
        }

        stage('Built the project') {
            steps {
                bat 'dotnet build'
            }
        }


        stage('Test') {
            steps {
                bat 'dotnet test' // Runs your tests
            }

        }

    }

    post {
        always {
            echo 'Pipeline completed.'
        }
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
