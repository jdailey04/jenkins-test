pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                sh 'echo "Starting build for $BRANCH_NAME service..."'
            }
        }
        stage('Test') {
            steps {
                // This checks every python file in the repo for syntax errors
                sh 'python3 -m py_compile *.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to the dev server...'
            }
        }
    }
}
