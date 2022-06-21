pipeline {
    agent any
    stages {
        stage('git-clone') {
            steps {
               git credentialsId: 'git', url: 'https://github.com/glk02/Studentapp.git'
            }	
	}	
        stage('mvn-clean') {
            steps {
                sh 'mvn clean'
            }	
	}	
	stage('mvn-compile') {
            steps {
	        sh 'mvn compile'
	    }
	}	
	stage('mvn-package') {
            steps {	
		sh 'mvn package'
	    }
        }
    }
}
