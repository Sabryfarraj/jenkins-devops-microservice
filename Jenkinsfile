pipeline {
    agent any
    environment {
        dockerHome = tool 'myDocker'
        mavenHome = tool 'mymaven'
        PATH = "${dockerHome}/bin:${mavenHome}/bin:${env.PATH}"
    }
    stages {
        stage('Checkout') {
            steps {
                sh 'mvn --version' // Verify Maven version
                sh 'docker version' // Verify Docker version
                echo 'Build'
                echo "PATH - ${env.PATH}"
                echo "BUILD_NUMBER - ${env.BUILD_NUMBER}"
                echo "BUILD_ID - ${env.BUILD_ID}"
                echo "JOB_NAME - ${env.JOB_NAME}"
                echo "BUILD_TAG - ${env.BUILD_TAG}"
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn clean compile' // Perform a clean install
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test' // Run tests
            }
        }

        stage('Integration Test') {
            steps {
                sh 'mvn failsafe:integration-test failsafe:verify' // Run integration tests
            }
        }
    }
    post {
        always {
            echo 'I am bored'
        }
        success {
            echo 'Ran successfully'
        }
        failure {
            echo 'Failed!!!!!!!!!'
        }
    }
}
