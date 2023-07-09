pipeline {
    agent {label 'slave'}


    stages {
        stage('Devbranch') {
            steps {
                echo "This is dev branch"
            }
        }
        stage('Checkout') {
            steps {
                git 'https://github.com/iampsrv/batchsevenproject.git'
                sh "ls -ltr"
            }
        }
        stage('Setup') {
            steps {
                sh "pip install -r requirements.txt"
            }
        }
        stage('Test') {
            steps {
                sh "pytest test.py"
            }
        }
    }
}
