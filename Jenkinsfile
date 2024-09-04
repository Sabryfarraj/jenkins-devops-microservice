pipeline {
    agent any // which agent to use
    environment {
        dockerHome = tool 'myDocker'
        mavenHome = tool 'mymaven'
        PATH = "${dockerHome}/bin:${mavenHome}/bin:${env.PATH}"
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version' // Corrected command to 'mvn'
                sh 'docker version'
                echo 'Build'
                echo "PATH - ${env.PATH}"
                echo "BUILD_NUMBER - ${env.BUILD_NUMBER}"
                echo "BUILD_ID - ${env.BUILD_ID}"
                echo "JOB_NAME - ${env.JOB_NAME}"
                echo "BUILD_TAG - ${env.BUILD_TAG}"
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
            echo 'I am smart'
        }
        success {
            echo 'Run successfully'
        }
        failure {
            echo 'Failed!!'
        }
    }
}
