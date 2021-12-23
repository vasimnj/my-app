pipeline {
    agent any 
    tools { 
        maven 'maven-3.8.4' 
    }
    stages {
        stage('clone repo and clean') { 
            steps {
		sh "mvn clean"	
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test"
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package" 
            }
        }
    }
}
