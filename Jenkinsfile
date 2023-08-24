//DECLARATIVE
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Build Docker '
            }
            agent {
                docker {
                    image 'maven:3.6.3'
                    // Run the container on the node specified at the
                    // top-level of the Pipeline, in the same workspace,
                    // rather than on a new node entirely:
                    reuseNode true
                }
            }
            steps {
                sh 'mvn --version'
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
        changed {
            echo ' add lerts in case of change'
        }
    }

}
//[always, changed, fixed, regression, aborted, success, unsuccessful, unstable, failure, notBuilt, cleanup]
