//Declarative
pipeline {
	agent any
	// agent { docker { image 'maven:latest'} }
	// agent {
	// 	docker { 
	// 		image 'node:16.13.1-alpine'
	// 	}
	// } 
	environment { 
		dockerHome = tool 'MyDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages {
		stage('Build'){
			steps {
				sh 'mvn --version'
				sh 'docker version'
				echo 'New Build'
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"

			}
		}
		stage('Compile') {
			steps {
				sh "mvn clean compile"
			}
		}
		stage('Test') {
			steps {
				sh "mvn test"
			}
		}
		stage('Integration Test') {
			steps {
				sh "mvn failsafe:integration-test failsafe:verify"
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