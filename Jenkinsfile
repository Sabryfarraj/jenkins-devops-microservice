//Declarative script
pipeline {
    agent any //which agent to use
    stages {
        stage('Build') {
            steps {
                echo 'Build'
                echo "PATH - $PATH"
                echo "BUILD_NUMBER - BUILD_NUMBER - $env.BUILD_NUMBER"
                echo "BUILD_ID - $env.BUILD_ID"
                echo "JOB_NAME - $enc.JOB_NAME"
                echo "BUILD_TAG - $env.BUILD_TAG"
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
