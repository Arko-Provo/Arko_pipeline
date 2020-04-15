pipeline {
	agent any
	stages {
		stage ('Code Quality Analysis'){
//environment {
  //      scannerHome = tool 'SonarQubeScanner'
    //}
    steps {
	    def scannerHome = tool 'SonarQubeScanner'
        withSonarQubeEnv('SonarQube') {
            sh "${scannerHome}/bin/sonar-scanner"
        }
        timeout(time: 10, unit: 'MINUTES') {
            waitForQualityGate abortPipeline: true
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
