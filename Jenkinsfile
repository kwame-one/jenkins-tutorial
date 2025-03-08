pipeline {
    agent any
    environment {
        CC = 'clang'
    }
    parameters {
        string(name: 'STATEMENT', defaultValue: 'hello; ls /', description: 'What should I say?')
    }

    stages {
        stage('Example') {
              environment {
                DEBUG_FLAGS = '-g'
            }
            steps {
                sh 'printenv'
                sh 'echo ${STATEMENT}'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}