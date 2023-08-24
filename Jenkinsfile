//DECLARATIVE
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Build'
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
            }
        }
        stage('IT Tests') {
            steps {
                echo 'IT Tests'
            }
        }
    } post {
        always {
            echo 'yeah I did it , I am awesome'
        }
        success {
            echo 'success'
        }
        failure {
            echo 'failure'
        }
    }
}
