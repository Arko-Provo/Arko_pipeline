pipeline { 
    agent any 
    stages {
	     stage('SonarQube analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    // Optionally use a Maven environment you've configured already
                    withMaven(maven:'Maven 3.5') {
                        sh 'mvn clean package sonar:sonar'
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
