pipeline {
	agent any
	stages {
		stage ('Code Quality Analysis'){
            environment {
                scannerHome = tool 'SonarQube'
            }
            steps{
                withSonarQubeEnv('SonarQube') {
                    sh 'mvn clean package sonar:sonar'
		}
	    }
		}
stage('Build') { 
 steps {
            sh 'pwd'
	    sh 'ls -l'
	    sh 'javac HelloWorld.java'
	    sh "java HelloWorld"
	    }
	    }
	    stage('Test') {
	    steps {
	     sh 'javac TCS.java'
	     sh 'java TCS'
	     }
	     }
	     }
	     }
