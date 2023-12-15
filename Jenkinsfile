pipeline{
	agent any
	stages{
		stage('Build'){
			steps{
				echo 'Build'
			}
		}	
		stage('Test'){
			steps{
				echo 'Test'
			}
		}
		stage('Integration Test'){
			steps{
				echo 'Integration Test'
			}
		}	
	}
	post{
	
		always{
			echo 'Build Completed !!!'
		}
		success{
			echo 'Successfully completed Build'
		}
		failure{
			echo 'Build did not succeed'
		}
	}
}