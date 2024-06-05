pipeline {
    agent any
    
    tools {
        maven 'maven3'
        jdk 'jdk17'
    }
    
    stages {
       
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
        
        stage('Unit Tests') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
