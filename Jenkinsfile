pipeline {
	agent any
	stages {
		stage ('Code Quality Analysis'){
			steps{
              
				script{
					scannerhome = tool 'sonar_scanner'
				}
				withSonarQubeEnv('SonarQube') {
					sh """
					${scannerhome}/opt/sonar76 \
					-Dsonar.projectKey=Sonar_Arko \
					-Dsonar.sources=. \
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
