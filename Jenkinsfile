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
				// sh 'mvn --version'
				// sh 'docker version'
				echo 'New Build'
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "BUILD_URL - $env.BUILD_URL"
				git 'https://github.com/Skyler000/odoo15-docker.git'

				

			}
		// }
		// stage('Compile') {
		// 	steps {
		// 		sh "mvn clean compile"
		// 	}
		// }
		// stage('Test') {
		// 	steps {
		// 		sh "mvn test"
		// 	}
		// }
		// stage('Integration Test') {
		// 	steps {
		// 		sh "mvn failsafe:integration-test failsafe:verify"
		// 	}
		// }
		// stage('Package') {
		// 	steps {
		// 		sh "mvn package -DskipTests"
		// 	}
		// }
		// stage('Build Docker Image') {
		// 	steps {
		// 		//"docker build -t skyler000/currency-exchange-devops:$env.BUILD_TAG"
		// 		script { 
		// 			dockerImage = docker.build("skyler000/currency-exchange-devops:${env.BUILD_TAG}")
		// 		}

		// 	}
		// }
		// stage('Push Docker Image') {
		// 	steps {
		// 		script {
		// 			docker.withRegistry('', 'dockerhub') {
		// 				dockerImage.push();
		// 				dockerImage.push('latest');
		// 			}
		// 		}
		// 	}
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
