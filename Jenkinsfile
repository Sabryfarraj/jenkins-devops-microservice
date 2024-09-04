//Declarative script
pipeline {
    agent { docker { image 'maven:3.6.3' } } //which agent to use
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
        stage('Integration Test') {
            steps {
                echo 'Integration Test'
            }
        }
    }
    post {
            always {
                echo 'i am smart'
            }
            success {
                echo 'runned succesfuly'
            }
            failure {
                echo 'failed!!'
            }
    }
}
