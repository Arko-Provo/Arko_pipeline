pipeline { 
    agent any 
    stages {
	     stage('SonarQube analysis') {
    def scannerHome = tool 'SonarScanner 4.0';
    withSonarQubeEnv('SonarQube') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
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
