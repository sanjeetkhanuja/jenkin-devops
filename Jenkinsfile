pipeline {
	agent { docker { image 'maven:3.6.3' } }
	stages {
		stage('Build') {
			steps {
				echo "Build"
				sh 'mvn --version'
				echo "Path : $PATH"
				echo "Build Number: $env.BUILD_NUMBER"
				echo "Job Name: $env.JOB_NAME"
				echo "Build Tag: $env.BUILD_TAG"
				echo "Build URL: $env.BUILD_URL"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}	
		}
	} 
	post {
		always {
			echo "always"
		}
		success {
			echo "success"
		}
		failure {
			echo "failure"
		}
	}
}
