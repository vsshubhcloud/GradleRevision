pipeline {
	agent any
	
	tools {
		gradle 'GRADLE'
		jdk 'JDK'
	}
	
	stages {
		stage('Checkout') {
			steps {
				git branch:'master', url:'https://github.com/vsshubhcloud/GradleRevision.git'
			}
		}
		
		stage('Build') {
			steps {
				sh 'gradle build'
			}
		}
		
		stage('Test') {
			steps {
				sh 'gradle test'
			}
		}					
		
		stage('Run') {
			steps {
				sh 'gradle run'
			}
		}
	}
	
	post {
		success {
			echo "Pipeline Successfull!"
		}
		failure {
			echo "Pipeline failed!"	
		}
	}												
