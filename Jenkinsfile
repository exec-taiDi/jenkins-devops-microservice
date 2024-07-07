//scripted
pipeline {
	agent any
//	agent { docker { image 'maven:3.6.3'}}
//	agent { docker { image 'node:latest'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}

	stages {
		stage('Build') {
			steps {
				sh "mvn --version"
				sh "docker version"
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