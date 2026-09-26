pipeline {
    agent { 
        node {
            label 'docker-agent'
            }
    }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                echo 'Build stage complete.'
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo 'Test stage complete.'
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "Build delivered successfully."
                '''
            }
        }
    }
    post {
        success {
            echo '✅ Build and deployment succeeded!'
        }
        failure {
            echo '❌ Build failed. Check logs.'
        }
    }
}
