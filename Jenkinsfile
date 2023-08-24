//DECLARATIVE
pipeline {
    agent { docker { image 'maven:3.6.3'} }
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
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
    }
    post {
        always {
            echo 'yeah I did it , I am awesome'
        }
        success {
            echo 'success'
        }
        failure {
            echo 'failure'
        }
        changes {
            echo ' add lerts in case of change'
        }
    }

}
