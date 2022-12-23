//Declarative
pipeline {
	//agent any
	//agent { docker { image 'maven:latest'} }
	agent {
		docker { 
			image 'node:16.13.1-alpine'
		}
	} 
	stages {
		stage('Build'){
			steps {
				//sh 'mvn --version'
				sh 'node --version'
				echo 'Build'
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