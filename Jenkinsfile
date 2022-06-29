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
	/* stage('mvn-sonar') {
            steps {
	        sh 'mvn sonar:sonar -Dsonar.projectKey=Studentapp -Dsonar.host.url=http://34.125.14.47:9000 -Dsonar.login=4f1ff1ab1fa075172cd09d99a150a5e7d0caf0b8'
	    }
	} */
	stage('mvn-package') {
            steps {	
		sh 'mvn package'
	    }
        }
    }
}
