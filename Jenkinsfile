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
    }
}
