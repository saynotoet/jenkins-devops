pipeline{
	//agent any
	agent {docker {image 'mvn:3.6.3'}}
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
				//echo 'Build'
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