pipeline {
    agent any
	
    stages {
        stage('Build and Scan') {
		environment {
			scannerHome = tool 'sonar scanner'
    	    	}
		steps {
                	withSonarQubeEnv('sonar') {
            	     	sh 'mvn clean package sonar:sonar'
       			}
            	}
    	}
    }
}
