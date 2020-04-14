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
	mvn  -Dsonar.analysis.mode=preview -Dsonar.scm.enabled=false -Dsonar.scm-stats.enabled=false -Dsonar.working.directory=/opt/sonar76/.sonar
			sh "${M2_HOME}/bin/mvn package"
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
