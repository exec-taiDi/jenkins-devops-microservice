//scripted
pipeline {
	agent any
//	agent { docker { image 'maven:3.6.3'}}
//	agent { docker { image 'node:latest'}}
	stages {
		stage('Build') {
			steps {
			//	sh "mvn --version"
			//	sh "node --version"
				echo "Build"
				echo "$PATH"
				echo "Build number - $env.BUILD_NUMBER"
				echo "build id $env.BUILD_ID"
				echo "build tag $env.BUILD_TAG"
				echo "job name $env.JOB_NAME"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
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
			echo 'always statement - awesome maybe?'
		}
		success {
			echo 'success statement?'
		}
		failure {
			echo 'failure statement?'
		}
	}
}