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
                sh "echo ${params.STATEMENT}"
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