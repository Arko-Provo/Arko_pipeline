pipeline { 
    agent any 
    stages {
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
