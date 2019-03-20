pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat(/"${M3}\bin\mvn" -Dmaven.test.failure.ignore clean/)       
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                bat(/"${M3}\bin\mvn" -Dmaven.test.failure.ignore test/)
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                bat(/"${M3}\bin\mvn" -Dmaven.test.failure.ignore deploy/)
            }
        }
        stage('install') {
            steps {
                echo 'Deploying....'
                bat(/"${M3}\bin\mvn" -Dmaven.test.failure.ignore install/)
            }
        }
    }
}
