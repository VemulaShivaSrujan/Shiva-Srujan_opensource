pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                echo 'Build completed'
            }
        }

        stage('Test') {
            steps {
        bat 'test.bat'
    }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                echo 'Deployment successful'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded 🎉'
        }
        failure {
            echo 'Pipeline failed ❌'
        }
        always {
            archiveArtifacts artifacts: '*.txt', allowEmptyArchive: true
        }
    }
}

 
