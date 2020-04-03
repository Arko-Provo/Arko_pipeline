pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps { 
                sh 'pwd'
                sh 'ls -l'
                sh 'javac HelloWorld.java'
                sh "cd Arko_pipeline & java HelloWorld"
            }
        }
    }
}
