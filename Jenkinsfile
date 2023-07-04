/* scripted
    node {
	stage('Build') {
		echo "Build"
	}
	stage('Test') {
		echo "Test"
	}
	stage('Integration')
	{
		echo "Integration"
	}
}*/
//declarative 
pipeline {
	//agent any
	agent {docker { image 'maven:3.6.3' } }
	stages{
		stage('Build'){
			steps{
				echo "Build"
				//sh 'maven --version' //shell scripting for version as output
				echo "Build"
				echo "$PATH" //to find the path 
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAM - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
			}
		}
		stage('Test'){
			steps{
				echo "Test"
			}
		}	
		stage("Integration testing")	{
			steps{
				echo "Integration steps"
			}
		}
	}post{
		always{
			echo  'I run always'
		}
		success{
			echo 'I run when I am successful'
		}
		failure {
			echo 'I run when you fail'
		}
	}

}
