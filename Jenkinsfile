//Declarative
pipeline {
	agent any
	// agent { docker { image 'maven:latest'} }
	// agent {
	// 	docker { 
	// 		image 'node:16.13.1-alpine'
	// 	}
	// } 
	stages {
		stage('Build'){
			steps {
				// sh 'mvn --version'
				// sh 'node --version'
				echo 'New Build'
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"

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
			echo 'Im awesome . I run always'
		}
		success {
			echo 'I run when you successfull'
		}
		failure {
			echo ' i run when you fail'
		}
	}
			
	
}