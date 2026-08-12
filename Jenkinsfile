pipeline {
    agent any

    stages {

        stage('Verify Source Code') {
            steps {
                echo 'Checking source code...'
                sh '''
                    echo "Current directory:"
                    pwd

                    echo "Files:"
                    ls -la

                    echo "Git commit:"
                    git log -1 --oneline
                '''
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                sh '''
                    echo "Simple Build Successful"
                '''
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh '''
                    echo "Simple Test Successful"
                '''
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging application...'
                sh '''
                    echo "Simple Packaging Successful"
                '''
            }
        }
    }

    post {
        success {
            echo 'PIPELINE SUCCESSFUL!'
        }

        failure {
            echo 'PIPELINE FAILED!'
        }
    }
}
