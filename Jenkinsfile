pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Scan') {
	        environment {
        	    scannerHome = tool 'sonar scanner'
    	    }
            steps {
                withSonarQubeEnv('sonar') {
            	     sh "${scannerHome}/bin/sonar-scanner"
        	    }
            }
        }
    }
}
