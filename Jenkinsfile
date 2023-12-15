pipeline{
	agent any
	//agent {docker {image 'maven:3.6.3'}}
	environment{
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
				sh 'docker version'
				echo 'Build'
				echo "PATH - $PATH"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
							
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