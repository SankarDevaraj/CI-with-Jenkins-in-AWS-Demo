pipeline {
    agent any

    stages {
       stage('SonarQube analysis 1') {
            steps {
                sh 'mvn clean package sonar:sonar'
            }
        }
    }
}
