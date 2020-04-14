pipeline {
	agent any
	stages {
		stage ('Code Quality Analysis'){
            environment {
                scannerHome = tool 'SonarQube'
            }
            steps{
                withSonarQubeEnv('SonarQube') {
			//def M2_HOME = tool name: 'maven-3', type:'maven'
			sh "${M2_HOME}/bin/mvn package"
                    //sh 'mvn clean package sonar:sonar'
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
