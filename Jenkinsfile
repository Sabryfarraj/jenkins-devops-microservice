//Declarative script
pipeline{
	agent any //which agent to use
	stages{
		stage('Build'){
			steps{
			echo "Build"
			}
		}

		stage('Test'){
			steps{
			echo "Test"
			}
		}
		stage('Integration Test'){
			steps{
			echo "Integration Test"
			}
		}
	}
		post{
			always{
				echo "i am smart"
			}
			success{
				echo "runned succesfuly"
			}
			failure{
				echo "failed!!"
			}
		}
}