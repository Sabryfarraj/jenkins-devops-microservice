//Declarative script
pipeline {
    agent any //which agent to use
    stages {
        stage('Build') {
            steps {
                echo 'Build'
                echo "$PATH"
                echo "BUILD_NUMBER - $env.BUILD_NUMBER"
                echo "$env.BUILD_ID"
                echo "$enc.JOB_NAME"
                echo "$env.BUILD_TAG"
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
