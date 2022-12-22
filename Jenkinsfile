//Declarative
pipeline {
	//agent any
	agent { docker { image 'maven:latest'} }
	stages{
		stage('Build'){
			steps {
				sh 'mvn --version'
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